# vue2-touch for Vue.js 2.x

> This is a directive wrapper for Hammer.js 2.0, ~~small size(just 22.7k).

## Install

``` bash
# install dependencies
npm install https://github.com/LYDZYL/vue2-touch.git    --save
或 yarn add https://github.com/LYDZYL/vue2-touch.git   
```

## Usage

### ES6

``` javascript
import Vue2Touch from 'vue2-touch'
Vue.use(Vue2Touch)
```

### Using the v-touch directive

``` html
<a v-touch:tap="callback">Tap me!</a>
<button v-touch:tap="callback.bind(this,111,222,...)" >tapBtn</button>
<div v-touch:swipe="callback">Swipe me!</div>

methods: {
			callback(arg1,arg2,evt) {
				console.log('arg',arg1)//输出=> 111
				console.log('args',arg2)//输出=> 222
				console.log('evt',evt)//输出=> tap
				console.log('event',event)// 输出=> PointerEvent{...}
			}
      }
```


### callback
Callback is a name of function with two args(can use any name, but type must be a funciton);the first argument can return a touch type(swipeleft,tap ...), and the second argument can return a callback event.

## More Details
See [Hammer.js document](http://hammerjs.github.io/)

## License
[MIT](https://opensource.org/licenses/MIT)
