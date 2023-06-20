# Vite Pozitron starter App
vite starter template Pozitron + JSX

[Pozitron](https://github.com/NesCafe62/pozitron) is ultra-minimalistic reactive library

jsx support provided by [vite-plugin-pozitron](https://github.com/NesCafe62/vite-plugin-pozitron)

## install
```sh
$ cd project-path
$ git clone https://github.com/NesCafe62/vite-pozitron-starter .
$ npm install
```

start for development
```sh
$ npm start
```

build project. results saved to `./dist`
```sh
$ npm run build
```

preview production build
```sh
$ npm run serve
```

## jsx
```jsx
import { signal } from 'pozitron-js';
import { render } from 'pozitron-js/render';

function Counter() {
    const [count, setCount] = signal(0);

	function increment() {
		setCount(count() + 1);
	}

	return (
		<button onClick={increment}>Count: {count}</button>
	);
}

render(Counter, document.getElementById('app'));
```

## hyperscript
```js
import { signal } from 'pozitron-js';
import { h, render } from 'pozitron-js/render';

function Counter() {
    const [count, setCount] = signal(0);

	function increment() {
		setCount(count() + 1);
	}

	return h('button', {on: {click: increment}}, ['Count: ', count]);
}

render(Counter, document.getElementById('app'));
```
