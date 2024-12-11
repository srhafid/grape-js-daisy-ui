# grape-js-daisy-ui

`grape-js-daisy-ui` is a library that integrates DaisyUI components directly into GrapesJS, allowing developers to use Tailwind CSS components with the `dy-` prefix to easily design and customize user interfaces.

## Features

- **DaisyUI Compatibility**: All DaisyUI components are available in GrapesJS.
- **Ease of Installation**: You only need to install this library and configure TailwindCSS.

## Installation

### Prerequisites

1. Have a project set up with GrapesJS.
2. Have TailwindCSS installed in your project.
3. Have the `grapesjs` and `grapesjs-tailwind-ui-components` libraries installed, as they are required for the correct functioning of `grape-js-daisy-ui`.

Base configuration example:

```javascript
import grapesjs from "grapesjs";
import grapesJsTailwindUiComponents from
 'grapesjs-tailwind-ui-components';
import { daisyUI } from "./blocksElements/daisyUI";

const editor = grapesjs.init("#gjs");

const components = [...daisyUI];

grapesJsTailwindUiComponents(editor, components);
```

### Step 1: Install the Library

Install the library using npm:

```bash
npm install grape-js-daisy-ui
```

### Step 2: Configure TailwindCSS

Ensure that TailwindCSS is configured in your project and that DaisyUI is included as a plugin in your `tailwind.config.js` file:

```javascript
module.exports = {
  content: [
    './src/**/*.{html,js}',
    './node_modules/grape-js-daisy-ui/**/*.js',
  ],
  theme: {
    extend: {},
  },
  plugins: [
    require('daisyui'),
  ],
  daisyui: {
    prefix: 'dy-', // Use the "dy-" prefix for DaisyUI components
  },
};
```

### Step 3: Import the Library into GrapesJS

Import and use the library in your main file where GrapesJS is configured:

```javascript
import grapesjs from 'grapesjs';
import grapeJsDaisyUi from 'grape-js-daisy-ui';

const editor = grapesjs.init({
  container: '#gjs',
  plugins: [grapeJsDaisyUi],
  pluginsOpts: {
    grapeJsDaisyUi: {}, // Additional configuration if needed
  },
});
```

## Usage

1. Start GrapesJS in your project.
2. DaisyUI components will be available in the component editor with the `dy-` prefix.
3. Drag and drop components from the block list onto the canvas to create your design.

### Usage Example

Here is a simple example of how to use a DaisyUI component in GrapesJS:

```html
<div class="dy-btn dy-btn-primary">Primary Button</div>
```

## Contributions

If you want to contribute to this project, please:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with your changes.

## Credits

This project would not be possible without the following technologies and their respective communities:

- **[DaisyUI](https://daisyui.com/)**: A TailwindCSS plugin that simplifies UI component design.
- **[TailwindCSS](https://tailwindcss.com/)**: A highly configurable CSS framework.
- **[GrapesJS](https://grapesjs.com/)**: A visual web editor for creating and managing web pages without writing code.

## License

This project is licensed under the MIT License. You can refer to the `LICENSE` file for more details.

---

Thank you for using `grape-js-daisy-ui`! If you encounter any issues or have suggestions, feel free to open an issue in the official repository.