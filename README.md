# FeatherJS

**FeatherJS** is a lightweight, modular JavaScript library designed for modern web applications. It offers efficient DOM manipulation, AJAX requests, utilities, event handling, and animations in a small, fast package.

## Features

- 🔥 **Lightweight**: Minimal footprint, making it perfect for fast-loading applications.
- ⚡ **Fast and Efficient**: Optimized for performance, offering faster alternatives to heavier libraries.
- 🧩 **Modular Design**: Each component is standalone, and you can import only what you need.
- 🌍 **Cross-Browser Support**: Works seamlessly across modern browsers.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [DOM Manipulation](#dom-manipulation)
  - [AJAX/HTTP Requests](#ajaxhttp-requests)
  - [Utilities](#utilities)
  - [Event Handling](#event-handling)
  - [Animations](#animations)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Using NPM
```bash
npm install featherjs
```

### Using a CDN
You can directly include FeatherJS via a CDN:

```html
<script src="https://cdn.your-cdn.com/featherjs.min.js"></script>
```

### Manual Download
You can download the latest release from [Releases](https://github.com/yourusername/featherjs/releases) and include it in your project:

```html
<script src="path/to/featherjs.min.js"></script>
```

## Usage

Once FeatherJS is included in your project, you can easily start using its features. Below are some examples to get you started.

### DOM Manipulation

```javascript
// Select elements
const element = FeatherJS.$('.my-element');
const elements = FeatherJS.$$('.my-elements');

// Add and remove class
FeatherJS.addClass(element, 'active');
FeatherJS.removeClass(element, 'active');

// Set or get attributes
FeatherJS.attr(element, 'data-id', '123');
const id = FeatherJS.attr(element, 'data-id');
```

### AJAX/HTTP Requests

```javascript
FeatherJS.http('https://api.example.com/data', {
    method: 'GET',
    headers: { 'Authorization': 'Bearer token' }
})
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

### Utilities

- **Debounce**

```javascript
const resizeHandler = FeatherJS.debounce(() => {
    console.log('Resize event debounced');
}, 300);

window.addEventListener('resize', resizeHandler);
```

- **Throttle**

```javascript
const scrollHandler = FeatherJS.throttle(() => {
    console.log('Scroll event throttled');
}, 200);

window.addEventListener('scroll', scrollHandler);
```

- **Deep Clone**

```javascript
const original = { a: 1, b: { c: 2 } };
const clone = FeatherJS.deepClone(original);
console.log(clone);
```

- **Merge Objects**

```javascript
const merged = FeatherJS.merge({ a: 1 }, { b: 2 }, { c: 3 });
console.log(merged); // { a: 1, b: 2, c: 3 }
```

### Event Handling

```javascript
FeatherJS.on(document, 'click', '.button', function (event) {
    console.log('Button clicked!', this);
});
```

### Animations

```javascript
const box = FeatherJS.$('.box');

FeatherJS.animate((progress) => {
    box.style.transform = `translateX(${progress * 100}px)`;
}, 1000);
```

## API Reference

### DOM Methods
- **$**: Select the first matching element.
- **$$**: Select all matching elements.
- **addClass**: Add a class to an element.
- **removeClass**: Remove a class from an element.
- **attr**: Get or set an attribute on an element.

### AJAX/HTTP Requests
- **http(url, options)**: Make HTTP requests using the `fetch` API with a simple interface.

### Utilities
- **debounce(fn, delay)**: Debounce a function call.
- **throttle(fn, limit)**: Throttle a function call.
- **deepClone(obj)**: Create a deep clone of an object.
- **merge(target, ...sources)**: Merge multiple objects into the target.

### Event Handling
- **on(parent, eventType, selector, handler)**: Event delegation for easy event binding.

### Animations
- **animate(callback, duration)**: Perform animations using `requestAnimationFrame`.

## Contributing

We welcome contributions from the community! Here's how you can get involved:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/my-feature`).
3. Make your changes.
4. Push to your branch (`git push origin feature/my-feature`).
5. Open a Pull Request.

Make sure to write unit tests and document your changes. See [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

## License

FeatherJS is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

### Additional Files for the Repo

1. **`CONTRIBUTING.md`**:
   Provide guidelines for contributing, like testing, code style, etc.

2. **`LICENSE`**:
   Include an MIT license file.

---
