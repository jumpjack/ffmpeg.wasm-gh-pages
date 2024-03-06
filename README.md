# Vanilla / Browser Examples

## Tests
- [Test 1](https://jumpjack.github.io/ffmpeg.wasm-gh-pages/public/transcode.html) - video transcode
- [Test 2](https://jumpjack.github.io/ffmpeg.wasm-gh-pages/public/f2e.html) - fisheye to equirect

## Downloads

### Compressed

- [FFmpeg](https://registry.npmjs.org/@ffmpeg/ffmpeg/-/ffmpeg-0.12.7.tgz) 
- [Utils](https://registry.npmjs.org/@ffmpeg/util/-/util-0.12.0.tgz) 
- FFMpeg Core:
    - [Single thread](https://registry.npmjs.org/@ffmpeg/core/-/core-0.12.5.tgz)
    - [Multithread](https://registry.npmjs.org/@ffmpeg/core-mt/-/core-mt-0.12.5.tgz)

### Upacked

- [FFmpeg](https://github.com/jumpjack/ffmpeg.wasm-gh-pages/blob/main/ffmpeg/umd/ffmpeg-0-12-6-patched.js)  (patched to fix error of 814.ffmpeg.js file not f ound
- [Utils](https://unpkg.com/@ffmpeg/util@0.12.0/dist/umd/index.js) 
- FFMpeg Core:
    - [Single thread](https://unpkg.com/@ffmpeg/core@0.12.6/dist/umd/ffmpeg-core.js)
    - [Multithread](https://unpkg.com/@ffmpeg/core-mt@0.12.6/dist/umd/ffmpeg-core-mt.js)

## Workaround to overcome missing 814.ffmpeg.js

Source: [link](https://github.com/ffmpegwasm/ffmpeg.wasm/issues/694)

In **ffmpeg/package/dist/umd/ffmpeg.js** instead of:

    new Worker(new URL(e.p + e.u(814), e.b),{ type: void 0 })
    
use:

    new Worker(getWorkerURL(new URL(e.p + e.u(814), e.b)),{ type: void 0 })

and getWorkerURL function:

    function getWorkerURL(e) {
        const t = `importScripts( "${e}" );`;
        return URL.createObjectURL(new Blob([t], { type: "text/javascript" }));
    }


-------------

## Setup

You need to download assets from npm before running the examples:

```bash
$ npm run download
```

## Run

To run this example, execute:

```bash
$ npm start
```

Visit http://localhost:8080 to check available examples.

## Examples

| Example | Description |
| ------- | ----------- |
| transcode.html | Transcoding example |
| transcode-mt.html | Transcoding example using multi-thread |
| transcode.esm.html | Transcoding example using module |
| trim.html | Video trimming example |
| concatDemuxer.html | Video concat example |
