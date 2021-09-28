Challenge: How can we help Royal Netherlands Army to safeguard trust within its own ranks and within the broader defense system (government – army – people) and our Allies by using blockchain methodology by the populace (producers) when identifying and debunking desinformation (with regards to security policies, grand strategy and military information) instead of spreading more desinformation?

# Write a plugin

A plugin is simply a function that takes `hook` as an argument. The hook supports handling of asynchronous tasks.

## Full configuration

```js
window.$docsify = {
  plugins: [
    function(hook, vm) {
      hook.init(function() {
        // Called when the script starts running, only trigger once, no arguments,
      });

      hook.beforeEach(function(content) {
        // Invoked each time before parsing the Markdown file.
        // ...
        return content;
      });

      hook.afterEach(function(html, next) {
        // Invoked each time after the Markdown file is parsed.
        // beforeEach and afterEach support asynchronous。
        // ...
        // call `next(html)` when task is done.
        next(html);
      });

      hook.doneEach(function() {
        // Invoked each time after the data is fully loaded, no arguments,
        // ...
      });

      hook.mounted(function() {
        // Called after initial completion. Only trigger once, no arguments.
      });

      hook.ready(function() {
        // Called after initial completion, no arguments.
      });
    }
  ]
};
```

!> You can get internal methods through `window.Docsify`. Get the current instance through the second argument.

## Example

#### footer