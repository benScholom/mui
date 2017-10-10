React Buttons


## Default buttons
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>
          <Button>button</Button>
          <Button color="primary">button</Button>
          <Button color="danger">button</Button>
          <Button color="accent">button</Button>
        </div>
        <div>
          <Button disabled={true}>button</Button>
          <Button color="primary" disabled={true}>button</Button>
          <Button color="danger" disabled={true}>button</Button>
          <Button color="accent" disabled={true}>button</Button>
        </div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Flat buttons
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>
          <Button variant="flat">button</Button>
          <Button variant="flat" color="primary">button</Button>
          <Button variant="flat" color="danger">button</Button>
          <Button variant="flat" color="accent">button</Button>
        </div>
        <div>
          <Button variant="flat" disabled={true}>button</Button>
          <Button variant="flat" color="primary" disabled={true}>button</Button>
          <Button variant="flat" color="danger" disabled={true}>button</Button>
          <Button variant="flat" color="accent" disabled={true}>button</Button>
        </div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```
## Raised
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>
          <Button variant="raised">button</Button>
          <Button variant="raised" color="primary">button</Button>
          <Button variant="raised" color="danger">button</Button>
          <Button variant="raised" color="accent">button</Button>
        </div>
        <div>
          <Button variant="raised" disabled={true}>button</Button>
          <Button variant="raised" color="primary" disabled={true}>button</Button>
          <Button variant="raised" color="danger" disabled={true}>button</Button>
          <Button variant="raised" color="accent" disabled={true}>button</Button>
        </div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Floating action buttons
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>
          <Button variant="fab">+</Button>
          <Button variant="fab" color="primary">+</Button>
          <Button variant="fab" color="danger">+</Button>
          <Button variant="fab" color="accent">+</Button>
        </div>
        <div>
          <Button variant="fab" disabled={true}>+</Button>
          <Button variant="fab" color="primary" disabled={true}>+</Button>
          <Button variant="fab" color="danger" disabled={true}>+</Button>
          <Button variant="fab" color="accent" disabled={true}>+</Button>
        </div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Button sizes
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Button from 'muicss/lib/react/button';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>
          <Button size="small" color="primary">button</Button>
          <Button size="small" color="primary" variant="flat">button</Button>
          <Button size="small" color="primary" variant="raised">button</Button>
          <Button size="small" color="primary" variant="fab">+</Button>
        </div>
        <div>
          <Button color="primary">button</Button>
          <Button color="primary" variant="flat">button</Button>
          <Button color="primary" variant="raised">button</Button>
          <Button color="primary" variant="fab">+</Button>
        </div>
        <div>
          <Button size="large" color="primary">button</Button>
          <Button size="large" color="primary" variant="flat">button</Button>
          <Button size="large" color="primary" variant="raised">button</Button>
          <Button size="large" color="primary" variant="fab">+</Button>
        </div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```