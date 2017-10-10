React Checkbox

## Basic Example
Use the name and label attributes to add form input variable names and labels.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Checkbox from 'muicss/lib/react/checkbox';

class Example extends React.Component {
  render() {
    return (
      <form>
        <Checkbox name="inputA1" label="Option one" defaultChecked={true} />
        <Checkbox name="inputA2" label="Option two" />
        <Checkbox name="inputA3" label="Option three is disabled" disabled={true} />
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Controlled Component
To use <Checkbox> as a controlled component you can use the onChange handler to detect DOM changes and the checked property to update the component's value.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Checkbox from 'muicss/lib/react/checkbox';

class Example extends React.Component {
  state = {
    checked: true
  };

  onChange(ev) {
    this.setState({checked: ev.target.checked});
  }

  render() {
    return (
      <Checkbox
        label="Click me"
        checked={this.state.checked}
        onChange={this.onChange.bind(this)}
      />
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Uncontrolled Component
To use <Checkbox> as an uncontrolled component you can use the controlEl attribute to access the instance's inner DOM control element.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';
import Checkbox from 'muicss/lib/react/checkbox';

class Example extends React.Component {
  onSubmit(ev) {
    ev.preventDefault();  // prevent form submission
    alert(this.input.controlEl.checked);
  }

  render() {
    return (
      <form onSubmit={this.onSubmit.bind(this)}>
        <Checkbox label="Click me" ref={el => { this.input = el; }} />
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