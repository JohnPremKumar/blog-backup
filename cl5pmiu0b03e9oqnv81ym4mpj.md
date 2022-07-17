## How to generate favicons like a pro in Vite 3!

[Vite 3](https://vitejs.dev/) has been launched with super cool built-in features to make web development faster and easier. Being relatively new, it is obvious that it would take some time to adapt to things especially when it comes to plugin libraries in contrast to Webpack. While looking for plugins to automatically create favicons in Vite 3, it was found that were not many options available since the only available existing [plugin](https://www.npmjs.com/package/vite-plugin-favicon) was not working anymore. So, I decided to make one!

Since, when it comes to web application development, adding favicons to our website is one of the crucial aspects of Search Engine Optimization(SEO) and User Experience. Generating the favicons for all the platforms with different resolutions and adding them to your web pages would be a tiresome process especially if you have multiple static HTML files.

### Generating Favicons

First, we need to install the below package,

```
npm install vite-plugin-favicons-inject -D
``` 

Next, open your `vite.config.js` file import the package,

```
import vitePluginFaviconsInject from 'vite-plugin-favicons-inject';
``` 

At last, configure the plugin in your existing Vite configuration file as shown below,
```
export default defineConfig({
  plugins: [
    ...
    vitePluginFaviconsInject('./src/assets/logo.svg'), // change the path accordingly
    ...
  ]
});
```
This it! this will automatically generate 50+ different favicons variants for different platforms, and resolutions and will inject them into all the HTML files.

More details about the advanced configurations are provided in the [documentation](https://www.npmjs.com/package/vite-plugin-favicons-inject).

Feel free to post your comments!




