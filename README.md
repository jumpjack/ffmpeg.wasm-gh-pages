# Vanilla / Browser Examples

## Tests
- [Test 1](https://jumpjack.github.io/ffmpeg.wasm-gh-pages/public/transcode.html)
- [Test 2](https://jumpjack.github.io/ffmpeg.wasm-gh-pages/public/index.html)

## Downloads

### Compressed

- [FFmpeg](https://registry.npmjs.org/@ffmpeg/ffmpeg/-/ffmpeg-0.12.7.tgz) 
- [Utils](https://registry.npmjs.org/@ffmpeg/util/-/util-0.12.0.tgz) 
- FFMpeg Core:
    - [Single thread](https://registry.npmjs.org/@ffmpeg/core/-/core-0.12.5.tgz)
    - [Multithread](https://registry.npmjs.org/@ffmpeg/core-mt/-/core-mt-0.12.5.tgz)

### Upacked

- [FFmpeg]() 
- [Utils]() 
- FFMpeg Core:
    - [Single thread]()
    - [Multithread]()

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
