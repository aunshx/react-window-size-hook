# React Window Size Simple

[![NPM version](https://img.shields.io/npm/v/react-window-size-simple.svg?style=flat)](https://www.npmjs.com/package/react-window-size-simple)
![NPM license](https://img.shields.io/npm/l/react-window-size-simple.svg?style=flat)
[![NPM total downloads](https://img.shields.io/npm/dt/react-window-size-simple.svg?style=flat)](https://npmcharts.com/compare/react-window-size-simple?minimal=true)
[![NPM monthly downloads](https://img.shields.io/npm/dm/react-virtualized.svg?style=flat)](https://npmcharts.com/compare/react-virtualized?minimal=true)

A very simple react hook which generates the browsers height and width whether or not it is changed.
Useful for making websites responsive or triggering events based on size of browser.

Example:

```javascript
import React from 'react';
import useWindow from 'react-window-size-simple';

const App = () => {

    // Extract the height and width values from the hook 
    const { width, height } = useWindow()

    return (
      <>
        The browser width is {width} and height is {height}
      </>
    );

}

export default App;
```

An example of the usefulness of the hook is given below.

example: Align the divs vertically if the browser width is less than 400px or else align them horizontally

```javascript
import React from 'react';
import useWindow from 'react-window-size-simple';

const App = () => {

    const { width, height } = useWindow()

    return (
      <>
        <div style={width < 400 ? { display: 'flex', alignItems: 'center', flexDirection: 'column' } : { display: 'flex', alignItems: 'center', justifyContent: 'center' }} >
            <div>
                useWindow Functionality
            </div>
            <div>
                By aunsh.com
            </div>
            <div>
                03/04/2022
            </div>
        </div>
      </>
    );

}

export default App;
```
