## ���
5 ���Ӵ�0�һ��ng2��Ŀdemo
https://angular.io/docs/js/latest/quickstart.html

## ���岽��
�ٶ����Ѿ��߱���nodejs������
* �½�Ŀ¼�ṹ
   angular2-quickstart
        |----app
        |    |----app.component.js
        |    |----boot.js
        |----index.html
        |----package.json
* �޸�[package.json](#package.json)(npm ��أ������������������������עnodejs)
* ��װ����
    `npm install` ��package.jsonͬ��Ŀ¼��ִ�У��Ҽ�װ�㲻֪��������ִ�У�
    ִ�е�ʱ������к�ɫ����ľ��棬�������ǣ�����ɹ���
* �޸�[app.component.js](#app.component.js)
* �޸�[boot.js](#boot.js)
* �޸�[index.html](#index.html)

��ʱ�㷢�����Ŀ¼�����node_modules������һЩĿ¼��
����`npm start`�����Ĭ����������һ��ҳ�棬http://localhost:3000 ,���û�У�������ϵ�ң�

��ϲ�㣡��ܰ������˰ɣ���Ϣ�ᣬ�Ժ�������ϸ�ľ���ϸ��!


##�����嵥
<code id="package.json">package.json</code>
```
{
  "name": "angular2-quickstart",
  "version": "1.0.0",
  "scripts": {
    "start": "npm run lite",
    "lite": "lite-server"
  },
  "license": "ISC",
  "dependencies": {
    "angular2": "2.0.0-beta.0",
    "systemjs": "0.19.6",
    "es6-promise": "^3.0.2",
    "es6-shim": "^0.33.3",
    "reflect-metadata": "0.1.2",
    "rxjs": "5.0.0-beta.0",
    "zone.js": "0.5.10"
  },
  "devDependencies": {
    "lite-server": "^1.3.1"
  }
}
```
<code id="app.component.js">app.component.js</code>
```
(function (app) {
    app.AppComponent = ng.core
        .Component({
            selector: '.my-app',//�򵥵�CSSѡ����
            template: '<h1>My First Angular 2 App</h1>'
        })
        .Class({
            constructor: function () {
            }
        });
})(window.app || (window.app = {}));
```
<code id="boot.js">boot.js</code>
```
(function (app) {
    document.addEventListener('DOMContentLoaded', function () {
        ng.platform.browser.bootstrap(app.AppComponent);
    });
})(window.app || (window.app = {}));
```
<code id="index.html">index.html</code>
```
<!DOCTYPE html>
<html>
<head>
    <title>Angular 2 QuickStart</title>

    <!-- 1. Load libraries -->
    <script src="node_modules/angular2/bundles/angular2-polyfills.js"></script>
    <script src="node_modules/rxjs/bundles/Rx.umd.js"></script>
    <script src="node_modules/angular2/bundles/angular2-all.umd.js"></script>

    <!-- 2. Load our 'modules' -->
    <script src='app/app.component.js'></script>
    <script src='app/boot.js'></script>

</head>

<!-- 3. Display the application -->
<body>
<div class="my-app">Loading...</div>
</body>

</html>
```