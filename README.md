# Config JS

ConfigJS is a Form Object class created to make working with forms and validation errors more convenient. This package is automatically installed when using the Preflight PHP Framework.

Installing this package will add a new `config` method to Vue's global scope which can then be accessed through `config` method. The `config` method is used to create a new form object that will provide easy access to error messages, as well as conveniences such as resetting the form state on successful form submission.

## Install

You can install ConfigJS using Node JS package manager. Just run the below command inside your project to install it.

```bash
npm install @cratespace/config-js --save
```

## Usage

To use ConfigJS inside your Vue JS project, import the module and register it as a Vue JS 3 plugin, as shown below.

```javascript
import { createApp } from 'vue';
import Root from './App.vue';
import Config from 'config-js';

const app = createApp(Root);
const configItems = {
    app: {
        name: 'My App'
    }
}
app.use(Config, configItems);
app.mount('#app');
```

You will then be able to use ConfigJS within your Vue components using the `config` method:

```html
<template>
    <div>
        <span>{{ config('app.name') }}</span>
    </div>
</template>
```

### API

```javascript
/**
 * Get the specified configuration value.
 *
 * @param   {String}  key
 * @param   {Any}  defaultValue
 *
 * @return  {Any}
 */
config(key, defaultValue = null);
```

## Contributing

Please read [CONTRIBUTING.md](https://github.com/Thavarshan/ConfigJS/blob/main/.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

-   **Thavarshan Thayananthajothy** - _Initial work_ - [Thavarshan](https://github.com/Thavarshan)

See also the list of [contributors](https://github.com/cratespace/config-js/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/cratespace/config-js/blob/main/LICENSE) file for details
