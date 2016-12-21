# ng2-adsense
[![NPM version][npm-image]][npm-url]

[npm-image]: https://img.shields.io/npm/v/ng2-adsense.svg
[npm-url]: https://npmjs.org/package/ng2-adsense

Demo: https://scttcper.github.io/ng2-adsense/ 

### 1. Install
`npm install ng2-adsense --save`

### 2. Place Code
Use the standard adsense code somewhere on your index.html
```html
<script async src=//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js></script>
```
### 3. Add to NgModule
Add AdsenseModule to the imports of your NgModule
```typescript
import { AdsenseModule } from 'ng2-adsense';
@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule,
    AdsenseModule, // <--- Add to imports
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
### 4. Use
```html
<ng2-adsense
  [adClient]="'ca-pub-7640562161899788'"
  [adSlot]="7259870550">
</ng2-adsense>
```

### SystemJS
If you are using SystemJS, you should also adjust your configuration to point to the UMD bundle.

In your systemjs config file, `map` needs to tell the System loader where to look for `ng2-adsense`:
```js
map: {
  'ng2-adsense': 'node_modules/ng2-adsense/ng2-adsense.umd.js',
}
```
