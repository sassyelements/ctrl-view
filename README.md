# Ctrl View
A vanilla JS plugin for "toggle hide and show" elements.

## Demo
To try out Ctrl View clone this repo and run the following commands.

First install npm packages
```bash
npm install
```

Then run
```bash
npm start

# output
> Ctrl View@1.0.0 start
> parcel index.html

Server running at http://localhost:1234
Built in 1.60s
```

Visit `http://localhost:1234` to see the result. Your port may not be `1234`!

## How to Use Ctrl View?

First you need to get the plugin file `CtrlView.js`. Copy it to your JS directory. You can create a directory called `plugins/` in your JS directory and put the `CtrlView.js` there.

In your index.js file you want to initialize the object as shown in example below:

```javascript
import CtrlView from './js/plugins/CtrlView';

const modal = new CtrlView({
    activateElemCSS: 'elem__active'
});
```

The `CtrlView` object takes an object as an argument which allow you to customize the Ctrl View a little. See the object below to see all the attributes you can customize.

```javascript
const ctrlView = new CtrlView({
    activateElemCSS: 'elem__active',       // CSS class that activates target element
    trigger: 'data-elem-trigger',          // Data attribute for triggers
    id: 'data-elem-id'                     // Data attribute for element IDs
});
```

The HTML for the triggers and elements could look like following:

```html

<!-- Modal Triggers -->
<div class="elem__triggers">
    <a class="btn btn--default btn--round" href="#" data-elem-trigger="elem-one">Element One</a>
</div>

<!-- Element One -->
<div class="elem__container" data-elem-id="elem-one">
    <div class="elem__backdrop"></div>
    <div class="elem__content">
        <div class="elem__head">
            <h2 class="heading-light heading-2">Element One</h2>
        </div>
        <div class="ctrl-view__body">
            <h3 class="heading-light heading-3">This is the Element body!</h3>
        </div>
    </div>
</div>
```
