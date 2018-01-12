<h2>Welcome to Ng2-Image Viewer</h2>
<section>
    <p>This component uses the <a href="http://ignitersworld.com/lab/imageViewer.html">Image Viewer JS</a> in it's core.</p>
    <p>Ng2-Image Viewer uses MIT license, so you can use it as you wish, feel free to help contributing with the code.</p>
    <p>This component allows you to:</p>
    <ul>
        <li>
            <strong>Show images and PDF files, you can navigate through it;</strong>
        </li>
        <li>
            <strong>Rotate each image as you wish;</strong>
        </li>
        <li>
            <strong>Download images and PDF files (no additional configuration required);</strong>
        </li>
        <li>
            <strong>Zoom in and out;</strong>
        </li>
        <li>
            <strong>Fullscreen your files;</strong>
        </li>
    </ul>
</section>
<h3>Requirements: </h3>
<section>
    <ul>
        <li>
            Jquery;
        </li>
        <li>
            Material Icons (you can use your own icons customizing it on the <code>image-viewer.component.html</code> file);
        </li>
    </ul>
</section>
<h3>How to use it:</h3>
<section>
    <p>The component already have some input references:</p>
    <table>
        <thead>
        <tr>
            <td align="center">Name</td>
            <td align="center">Type</td>
            <td align="center">Required</td>
            <td align="center">Default Value</td>
            <td align="center">Description</td>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td align="center">idContainer</td>
            <td align="center">string</td>
            <td align="center">X</td>
            <td align="center">NULL</td>
            <td align="justify">It is the id of the component on the HTML, this parameter allows you to inject as many components as you wish.</td>
        </tr>
        <tr>
            <td align="center">images</td>
            <td align="center">BASE64[]</td>
            <td align="center"></td>
            <td align="center">NULL</td>
            <td align="justify">It is the array containing the base64 data, the component differs the images and the PDF files, so don't worry.</td>
        </tr>
        <tr>
            <td align="center">rotate</td>
            <td align="center">boolean</td>
            <td align="center"></td>
            <td align="center">true</td>
            <td align="justify">It is the boolean that renders the rotate left and right buttons</td>
        </tr>
        <tr>
            <td align="center">download</td>
            <td align="center">boolean</td>
            <td align="center"></td>
            <td align="center">true</td>
            <td align="justify">It is the boolean that renders the download button</td>
        </tr>
        <tr>
            <td align="center">fullscreen</td>
            <td align="center">boolean</td>
            <td align="center"></td>
            <td align="center">true</td>
            <td align="justify">It is the boolean that renders the fullscreen button</td>
        </tr>
        <tr>
            <td align="center">loadOnInit</td>
            <td align="center">boolean</td>
            <td align="center"></td>
            <td align="center">false</td>
            <td align="justify">It is the boolean that lets you choose if you want to load the component on the OnInit event or on the OnChanges event, It was created because i faced some trouble with the primeNG tab using the change event.</td>
        </tr>
        </tbody>
    </table>
</section>

## Installation

To install this library, run:

```bash
$ npm install ng2-image-viewer --save
```

## Consuming your library

Once you have published your library to npm, you can import your library in any Angular application by running:

```bash
$ npm install ng2-image-viewer
```

and then from your Angular `AppModule`:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

// Import your library
import { ImageViewerModule } from 'ng2-image-viewer';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,

    // Specify your library as an import
    ImageViewerModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Now just add the these codes on your angular-cli.json file:

```json
"styles": [
    "../node_modules/ng2-image-viewer/imageviewer.scss"
],
"scripts": [
    "../node_modules/ng2-image-viewer/imageviewer.js"
],
```

Once your library is imported, you can use its components, directives and pipes in your Angular application:

```xml
<!-- You can now use your library component in app.component.html -->
<h1>
  Image Viewer
</h1>
<app-image-viewer [images]="['iVBORw0KGgoAAAANSUhEUgAAAAUAAAAFCAYAAACNbyblAAAAHElEQVQI12P4//8/w38GIAXDIBKE0DHxgljNBAAO9TXL0Y4OHwAAAABJRU5ErkJggg==']"
[idContainer]="'idOnHTML'"
[loadOnInit]="true"></app-image-viewer>
```

## Development

To generate all `*.js`, `*.d.ts` and `*.metadata.json` files:

```bash
$ npm run build
```

To lint all `*.ts` files:

```bash
$ npm run lint
```

## License

MIT © [brenoprata10](mailto:brenoprata10@gmail.com)