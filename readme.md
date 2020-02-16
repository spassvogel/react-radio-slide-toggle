# react-radio-slide-toggle
A radio slide toggle for react

[![npm version](https://badge.fury.io/js/react-radio-slide-toggle.svg)](https://badge.fury.io/js/react-radio-slide-toggle)

Basically it's a checkbox group that renders as a sliding toggle. The HTML is still a functioning checkbox group so accessability is guaranteed.


## Install

```bash
npm install --save react-radio-slide-toggle 
```
or:

```bash
yarn add react-radio-slide-toggle 
```

## Usage

```jsx
import React from 'react'
import Toggle from 'react-radio-slide-toggle';
import './style.css'

const TurtlePage = () => {
  const setTurtle = (value) => {
    console.log(value);
  }
  return (
    <div>
      <Toggle 
        className="my-slide-toggle"
        selected='mickey'
        onChange={setTurtle}
        options={[{
          value: "mickey",
          label: "Michaelangelo",
        }, {
          value: "leo",
          label: "Leonardo"
        }, {
          value: "raph",
          label: "Raphael"
        }, {
          value: "donnie",
          label: "Donatello"
        }]}
      />
    </div>
  );
}
      
```

This renders the slide toggle unstyled, which is not what you want. So add a stylesheet like so:

```css
.my-slide-toggle {
    background: #E6ECFF;
    border-radius: 40px;
}

.my-slide-toggle label {
    padding: 14px 0;
    text-align: center;
    transition: all 0.4s;
    font-family: 'AvenirBold', sans-serif;
    color: #574d9e;
}

.my-slide-toggle input[type="radio"]:checked+label {
    /* the label that is currently selected */
    color: white;
}

.my-slide-toggle .toggle {
    /* the actual toggle that moves */
    background-color: #584d9f;
    border-radius: 40px;
}
```

Customize as needed.

## License

MIT © [Wouter van den Heuvel](https://github.com/spassvogel)

