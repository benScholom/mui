React Appbar


MUI provides a simple <Appbar> container that automatically adjusts its height based on the viewport dimensions:

48px (phone landscape)
56px (phone portrait)
64px (default)

## Example

```js
import React from 'react';
import ReactDOM from 'react-dom';
import Appbar from 'muicss/lib/react/appbar';

class Example extends React.Component {
  render() {
    return <Appbar></Appbar>;
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```