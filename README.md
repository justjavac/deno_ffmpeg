# deno_ffmpeg [WIP]

[![tag](https://img.shields.io/github/release/justjavac/deno_ffmpeg)](https://github.com/justjavac/deno_ffmpeg/releases)
[![Build Status](https://github.com/justjavac/deno_ffmpeg/workflows/ci/badge.svg?branch=master)](https://github.com/justjavac/deno_ffmpeg/actions)
[![license](https://img.shields.io/github/license/justjavac/deno_ffmpeg)](https://github.com/justjavac/deno_ffmpeg/blob/master/LICENSE)

ffmpeg module for Deno, using wasm.

## Usage

⚠️ not implement

```ts
import { createFFmpeg, fetchFile } from "https://deno.land/x/ffmpeg/mod.ts";

const ffmpeg = createFFmpeg({ log: true });

await ffmpeg.load();
ffmpeg.FS('writeFile', 'test.avi', await fetchFile('./test.avi'));
await ffmpeg.run('-i', 'test.avi', 'test.mp4');
await Deno.writeAll('./test.mp4', ffmpeg.FS('readFile', 'test.mp4'));
```

### License

[deno_ffmpeg](https://github.com/justjavac/deno_ffmpeg) is released under the MIT License. See the bundled [LICENSE](./LICENSE) file for details.