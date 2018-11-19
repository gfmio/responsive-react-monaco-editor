# responsive-react-monaco-editor

A responsive version of [`react-monaco-editor`](https://github.com/superRaytin/react-monaco-editor) that automatically resizes to fit the available space, when the window resizes.

## Usage

For detailed usage instructions, please check the documentation of [`react-monaco-editor`](https://github.com/superRaytin/react-monaco-editor).

This package provides responsive versions of the `MonacoEditor` and `MonacoDiffEditor` components.

If you provide `width` or `height` props, the component will not be responsive, but instead usage the fixed widths provided.

If neither prop is provided, the editor will fill the available space. Once mounted, the component will register a `resize` event handler with the browser window and rerender every time the window gets updated. An additional `rerenderTimeoutAfterResizeInMs` parameter is introduced to the props of both components (default: 100), to make the re-rendering not too resource consuming if the window gets resized.

Additionally, by default, the component will shift focus to the editor after it is mounted and clicking on line numbers will select the line. These options can be replaced using the respective props of `react-monaco-editor`.

```tsx
import React from "react";
import ReactDOM from "react-dom";
import {ResponsiveMonacoEditor} from "responsive-monaco-editor";

ReactDOM.render(
  <ResponsiveMonacoEditor
    value="console.log(\"Hello World\")"
    theme="vscode"
    language="javascript"
    theme="vs-dark"
  />,
  document.getElementById("app")
);
```

## Install

```sh
// NPM
npm install responsive-react-monaco-editor

// Yarn
yarn add responsive-react-monaco-editor
```

## License: MIT

MIT License

Copyright (c) 2018 Frédérique Mittelstaedt

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
