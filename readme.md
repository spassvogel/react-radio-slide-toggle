# react-radio-slide-toggle
A radio slide toggle for react

[![npm version](https://badge.fury.io/js/react-radio-slide-toggle.svg)](https://badge.fury.io/js/react-radio-slide-toggle)

Basically it's a checkbox group that renders as a sliding toggle. The HTML is still a functioning checkbox group so accessability is guaranteed.

![alt test](images/demo.gif)

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


## Properties

Property  | Type | Description
-- | -- | -- | --
options | `Array` | Options to display. Need to be in this format `{ label: 'label', value: 'value'}`
name | `string` | Name of the radio group. Optional.
selected | `string` | Value of the initially selected option. Optional.
onChange | `function` | Function that gets called when value changes. Will get passed the selected `value`. Optional.
className | `string` | Classname to be added to the radio group. Optional.
toggleClassName | `string` | Classname to be added to the toggle element. Optional.

## License

MIT © [Wouter van den Heuvel](https://github.com/spassvogel)

