# react-radio-group
> Radio component for react.


## size:
+ 8.0K	react-radio-group.js
+ 48K	react-radio-group.js.map

## properties:
```javascript
  static propTypes = {
    className: PropTypes.string,
    items: PropTypes.array,
    template: PropTypes.func
  };
```

## usage:
```jsx
class App extends React.Component {
  state = {
    items: [
      {
        val: 1,
        text: '选项1'
      }, {
        val: 2,
        disabled: true,
        text: '选项2'
      }, {
        val: 3,
        text: '选项3',
        selected: true,
      }, {
        val: 4,
        text: '选项4'
      }, {
        val: 5,
        text: '选项5'
      }
    ]
  };

  _template(item,iconEl){
    return (
      <div className="item">
        {item.text} {iconEl}
      </div>
    )
  }

  _change(inEvent) {
    console.log(inEvent.target.value);
  }

  render() {
    return (
      <div className="hello-react-radio-group">
        <ReactRadioGroup items={this.state.items} template={this._template.bind(this)}
                         onChange={this._change.bind(this)}/>
      </div>
    );
  }
}
```



## resource:
+ http://www.cnblogs.com/Kummy/p/4966937.html
+ https://github.com/steven5538/vue-button
+ https://yarnpkg.com/en/docs/install

