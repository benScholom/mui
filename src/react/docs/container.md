React Container

## Fixed Container
To wrap your content in a responsive container use the <Container> element:
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Container from 'muicss/lib/react/container';

class Example extends React.Component {
  render() {
    return (
      <Container>
        {/*

        Container is centered on page with 15px of
        padding on either side. The inner width is
        fluid for small viewports and has a max
        width for larger dimensions:
        
        * 570px (≥ 544px)
        * 740px (≥ 768px)
        * 960px (≥ 992px)
        * 1170px (≥ 1200px)

        */}
      </Container>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```

## Fluid Container
To wrap your content in a fluid container set fluid to true:
```js
import React from 'react';
import ReactDOM from 'react-dom';
import Container from 'muicss/lib/react/container';

class Example extends React.Component {
  render() {
    return (
      <Container fluid={true}>
        {/*

        Container is centered on page with 15px of
        padding on either side. The inner width is
        fluid for all viewport widths.

        */}
      </Container>
    );
  }
}

ReactDOM.render(<Example />, document.getElementById('example'));
```