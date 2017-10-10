React Select

## Basic Example
Use the MUI <Select component to use MUI styling for select input elements.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  render() {
    return (
      <form>
        <Select name="input" label="Select Example" defaultValue="option2">
          <Option value="option1" label="Option 1" />
          <Option value="option2" label="Option 2" />
          <Option value="option3" label="Option 3" />
          <Option value="option4" label="Option 4" />
        </Select>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Controlled Component
To use <Select> as a controlled component you can use the onChange handler to detect DOM changes and the value property to update the component's value.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  state = {
    value: "option2"
  };

  onChange(ev) {
    this.setState({value: ev.target.value});
  }

  render() {
    return (
      <form>
        <Select name="input" value={this.state.value} onChange={this.onChange.bind(this)} >
          <Option value="option1" label="Option 1" />
          <Option value="option2" label="Option 2" />
          <Option value="option3" label="Option 3" />
          <Option value="option4" label="Option 4" />
        </Select>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Uncontrolled component
To use <Select> as an uncontrolled component you can use the controlEl attribute to access the instance's inner DOM control element.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  onSubmit(ev) {
    ev.preventDefault();  // prevent form submission
    alert(this.select.controlEl.value);
  }

  render() {
    return (
      <form onSubmit={this.onSubmit.bind(this)}>
        <Select ref={el => { this.select = el; }} name="input" defaultValue="option2">
          <Option value="option1" label="Option 1" />
          <Option value="option2" label="Option 2" />
          <Option value="option3" label="Option 3" />
          <Option value="option4" label="Option 4" />
        </Select>
        <Button variant="raised">Get value</Button>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Use Default Menu
To use the browser's built-in select menu, use the useDefault property.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  render() {
    return (
      <form>
        <Select name="input" useDefault={true} defaultValue="option2">
          <Option value="option1" label="Option 1" />
          <Option value="option2" label="Option 2" />
          <Option value="option3" label="Option 3" />
          <Option value="option4" label="Option 4" />
        </Select>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```
## Dynamic Options
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  state = {
    options: [
      {value: 'option1', label: 'Option 1'},
      {value: 'option2', label: 'Option 2'},
      {value: 'option3', label: 'Option 3'},
      {value: 'option4', label: 'Option 4'}
    ]
  };

  onClick(ev) {
    let options = this.state.options,
        n = options.length + 1;
    
    options.push({value: 'option' + n, label: 'Option ' + n});
    this.setState({options: options});
  }

  render() {
    return (
      <form onSubmit={ev => { ev.preventDefault(); }}>
        <Select name="input" defaultValue="option2">
          {
            this.state.options.map(function (option, i) {
              return <Option key={i} value={option.value} label={option.label} />;
            })
          }
        </Select>
        <Button variant="raised" onClick={this.onClick.bind(this)}>Add item</Button>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```
## Properties

<select>

Name | DataType | Description | Default
----- | ----- | ----- | ------
defaultValue | String | The value of the selected option | -
disabled | Boolean | If specified, the component will be disabled | false
name | String | Value representing the `name` attribute of the inner DOM element | -
label | String | String value to use when you want to add a label | -
readOnly | Boolean | If specified, component will be read-only | false
required | Boolean | If specified, value will be required for form validation | false
useDefault | Boolean | If specified, component will use browser built-in select menu | false
value | String | The value of the selected option | -

<option>

Name | DataType | Description | Default
----- | ----- | ----- | ------
label | String | Value representing item label | -
value | String | The value of the item | false

