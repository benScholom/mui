React Radio

The MUI <Radio> component provides some basic styling and alignment upgrades to the React built-in <input type="radio"> component.
## Basic Example
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Radio from 'muicss/lib/react/radio';

class Example extends React.Component {
  render() {
    return (
      <form>
        <Radio name="inputA" label="Option one" defaultChecked={true} />
        <Radio name="inputA" label="Option two" />
        <Radio name="inputA" label="Option three is disabled" disabled={true} />
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```
## Controlled component
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Radio from 'muicss/lib/react/radio';

class Example extends React.Component {
  state = {
    selectedOption: 'option2'
  };

  onChange(ev) {
    this.setState({selectedOption: ev.target.value});
  }

  render() {
    return (
      <form>
        <Radio name="inputA" label="Option one" value="option1" checked={this.state.selectedOption === 'option1'} onChange={this.onChange.bind(this)} />
        <Radio name="inputA" label="Option two" value="option2" checked={this.state.selectedOption === 'option2'} onChange={this.onChange.bind(this)} />
        <Radio name="inputA" label="Option three" value="option3" checked={this.state.selectedOption === 'option3'} onChange={this.onChange.bind(this)} />
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Uncontrolled component
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';
import Radio from 'muicss/lib/react/radio';

class Example extends React.Component {
  onSubmit(ev) {
    ev.preventDefault();  // prevent form submission
    alert([
      'option1: ' + this.option1.controlEl.checked,
      'option2: ' + this.option2.controlEl.checked,
      'option3: ' + this.option3.controlEl.checked
    ].join('\n'));
  }

  render() {
    return (
      <form onSubmit={this.onSubmit.bind(this)}>
        <Radio name="inputA" label="Option one" value="option1" ref={el => { this.option1 = el; }} />
        <Radio name="inputA" label="Option two" value="option2" ref={el => { this.option2 = el; }} defaultChecked={true} />
        <Radio name="inputA" label="Option three" value="option3" ref={el => { this.option3 = el; }} />
        <Button variant="raised">Get value</Button>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Properties

Property | DataType | Description | Default
----- | ----- | ----- | ------
checked | Boolean | If specified, state of element will be checked | false
defaultChecked | Boolean | If specified, default state of element will be checked | false
defaultValue | String | Default value of control element | -
disabled | Boolean | If specified, control element will be disabled | false
label | String | String value to use for control element label | -
name | String | Value representing the 'name' attribute of the control element | -
value | String | The value of the control element | -