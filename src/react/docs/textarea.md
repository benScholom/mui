React Textarea

## Basic Example
Use the MUI <Textarea> component to use MUI styling for textarea elements.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Textarea from 'muicss/lib/react/textarea';

class Example extends React.Component {
  render() {
    return (
      <div>
        <Textarea hint="Input 1" />
        <Textarea hint="Input 2" defaultValue="Value on load" />
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Fixed Labels
Use the label attribute to add a fixed label.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Textarea from 'muicss/lib/react/textarea';

class Example extends React.Component {
  render() {
    return (
      <div>
        <Textarea label="Input 1" />
        <Textarea label="Input 2" defaultValue="Value on load" />
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Floating labels
Use floatingLabel={true} to float labels
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Textarea from 'muicss/lib/react/textarea';

class Example extends React.Component {
  render() {
    return (
      <div>
        <Textarea label="Input 1" floatingLabel={true} />
        <Textarea label="Input 2" floatingLabel={true} defaultValue="Value on load" />
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Controlled components
To use <Textarea> as a controlled component you can use the onChange handler to detect DOM changes and the value property to update the component's value.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Textarea from 'muicss/lib/react/textarea';

class Example extends React.Component {
  state = {
    value: "Value on load"
  };

  onChange(ev) {
    this.setState({value: ev.target.value});
  }

  render() {
    return (
      <Textarea
        value={this.state.value}
        onChange={this.onChange.bind(this)}
      />
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Uncontrolled components
To use <Textarea> as an uncontrolled component you can use the controlEl attribute to access the instance's inner DOM control element.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';
import Textarea from 'muicss/lib/react/textarea';


class Example extends React.Component {
  onSubmit(ev) {
    ev.preventDefault();  // prevent form submission
    alert(this.input.controlEl.value);
  }

  render() {
    return (
      <form onSubmit={this.onSubmit.bind(this)}>
        <Textarea ref={el => { this.input = el; }} defaultValue="Value on load" />
        <Button variant="raised">Get value</Button>
      </form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Properties
Name | DataType | Description | Default
----- | ----- | ----- | ------
defaultValue | String | Value used to set the default value for uncontrolled components | -
floatingLabel | Boolean | If specified, use a floating label | false
hint | String | Value to use as a placeholder when control element is empty | -
invalid | Boolean | If specified, will add MUI invalid CSS class | false
label | String | String value to use when you want to add a label | -
name | String | Value representing the `name` attribute of the inner DOM element | -
required | Boolean | If specified, value will be required for form validation | false
row | Number | Number of rows in textarea element | 2
value | String | The value of the inner DOM control element | -