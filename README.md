# CryptPad app

To create a new CryptPad application, you can copy this folder into your CryptPad repo's `www` folder.
You can use `git grep myapp` to find where to put your application name instead of "myapp".
```bash
git grep myapp

myapp/app-myapp.less:&.cp-app-myapp {
myapp/app-myapp.less:        @bg-color: @colortheme_apps[myapp],
myapp/app-myapp.less:    #cp-app-myapp-editor {
myapp/app-myapp.less:        #cp-myapp-content {
myapp/inner.html:    <script async data-bootload="/myapp/inner.js" data-main="/common/sframe-boot.js?ver=1.11" src="/components/requirejs/require.js?ver=2.3.7"></script>
myapp/inner.html:<body class="cp-app-myapp">
myapp/inner.html:    <div id="cp-app-myapp-editor"></div>
myapp/inner.js:    'less!/myapp/app-myapp.less'
myapp/inner.js:        let $container = $('#cp-app-myapp-editor');
myapp/inner.js:        let $content = $(h('div#cp-myapp-content')).appendTo($container);
myapp/inner.js:        contentContainer: '#cp-app-myapp-editor'
```

You'll also need to update several places in CryptPad:
* Enable the app and add a custom icon in `www/common/application_config_internal.js`
  * Change `availablePadTypes` and `applicationsIcon`
* Add a custom color in
  * `customize.dist/src/less2/colortheme.less` and `customize.dist/src/less2/colortheme-dark.less`
* Add a new tanslation key with your applciation pretty name
  * `Messages.type.myapp = "My application";`

