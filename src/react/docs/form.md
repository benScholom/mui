React Form
The MUI <Form> component is a lightweight wrapper around the React <form> component which allows you to style forms quickly.

## Form Titles
If you are using the <Form> component you can use a <legend> element to add a title
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Form from 'muicss/lib/react/form';
import Input from 'muicss/lib/react/input';
import Textarea from 'muicss/lib/react/textarea';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <Form>
        <legend>Title</legend>
        <Input hint="Input 1" />
        <Input hint="Input 2" />
        <Textarea hint="Textarea" />
        <Button variant="raised">Submit</Button>
      </Form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Inline forms
Use inline={true} to inline inputs above the small breakpoint.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Form from 'muicss/lib/react/form';
import Input from 'muicss/lib/react/input';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <Form inline={true}>
        <Input />
        <Button>submit</Button>
      </Form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Select Boxes
Use <Select> elements for MUI style select boxes.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Form from 'muicss/lib/react/form';
import Option from 'muicss/lib/react/option';
import Select from 'muicss/lib/react/select';

class Example extends React.Component {
  render() {
    return (
      <Form>
        <Select defaultValue="option-2">
          <Option value="option-1" label="Option 1" />
          <Option value="option-2" label="Option 2" />
          <Option value="option-3" label="Option 3" />
          <Option value="option-4" label="Option 4" />
        </Select>
      </Form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```
## Form validation
Use required={true} and <Input type="email|url|tel"> to take advantage of built-in HTML5 validation.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Form from 'muicss/lib/react/form';
import Input from 'muicss/lib/react/input';
import Textarea from 'muicss/lib/react/textarea';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <Form>
        <legend>Title</legend>
        <Input label="Required Text Field" required={true} />
        <Input label="Required Email Address" type="email" floatingLabel={true} required={true} />
        <Textarea label="Required Textarea" floatingLabel={true} required={true} />
        <Input label="Email Address" type="email" defaultValue="Validation error" />
        <Button variant="raised">Submit</Button>
      </Form>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```