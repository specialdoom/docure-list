### docure-list

```js
npm i @specialdoom/docure-list
```

### components

#### docure-list

- wrapper for docure-list-item

- attributes:
  - background: background color for list


#### docure-list-item

- item for docure list

- attributes:
  - title:  string, max 30 chars
  - description: string, max 330 chars

- slots:
  - one for displaying something despite the card like buttons or something else

### usage

```html
<docure-list>
  <docure-list-item title="title" description="description">
    <docure-button onClick="test()">Test button</docure-button>
  </docure-list-item>
  <docure-list-item title="title" description="description">
    <docure-button onClick="test()">Test button</docure-button>
  </docure-list-item>
  <docure-list-item title="title" description="description">
    <docure-button onClick="test()">Test button</docure-button>
  </docure-list-item>
</docure-list>
```

### example

![Example](presentation.png)
