React Dividers

## Default Divider
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>Content 1</div>
        <Divider />
        <div>Content 2</div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Top
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>Content 1</div>
        <div className="mui--divider-top">Content 2</div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Top
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div>Content 1</div>
        <div className="mui--divider-top">Content 2</div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Bottom
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <div className="mui--divider-bottom">Content 1</div>
        <div>Content 2</div>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Left
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <span>Content 1&nbsp;</span>
        <span className="mui--divider-left">&nbsp;Content 2</span>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Right
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Divider from 'muicss/lib/react/divider';

class Example extends React.Component {
  render() {
    return (
      <div>
        <span className="mui--divider-right">Content 1&nbsp;</span>
        <span>&nbsp;Content 2</span>
      </div>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```