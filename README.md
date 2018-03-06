Just planning things, and creating a markdown here..


# NEWREBEL.PIXI.Awesome.Filters

I've created this repository to `force` myself ;-) making it easier and possible to start adding some awesome PIXI 4 Filters, based on <i>(custom)</i> GLSL-Fragment and vertex-shaders. Codes that I've created over the years. At the moment these kinds of filters don't seem to exist for PIXI as something like a simple integratable plugin. Also, on various forums I see people struggling width certain aspects regarding for example the (varying) vTextureCoord (uv) that can be off in Pixi4. You'd be amazed that it's possible to create 3D (mimic) filters in PIXI's 2D environment. And how usable the most outrages crazy (texture) effects can be. 

Think about this, test it! 
1. Play the song 'Africa' by Toto (lame) on a rather loud volume. Then, after 30 seconds stop it, LEAVE YOUR VOLUME AS IT IS!! Then play either a Linkin Park song or even better 'God Hates us all' by Slayer. 
2. Go buy a pair of jeans. But try to find one that's perfectly blue... The most expensive and trendy jeans are aged, damaged! 
3. Check out Fender strat guitars. Brand new ones - expensive ones are scratched, aged, worn, damaged. And the real awesome players play on these kinds of guitars.

Even heard of the the word 'RELIC'?? 

Conclusion: 
For example: WHEN YOU CREATE A GLITH FILTER... IT HAS TO FEEL LIKE SLAYER, TRENDY JEANS, A RELIC FENDER STRAT...  And not like a polished lame effect straight out of something like Windows Moviemaker or Apple's Final Cut. It has to be real! 

Soon you will see what I mean by this, if you don't understand it.

*Combining audio (soundcloud) and shaders isn't difficult. I will also show that.

I'm currently working on a webpage to demonstrate these filters. I'll add them here!

<a href="https://github.com/webpack/webpack">
<img width="100%" height="auto" src="http://revolution-webdesign.nl/newrebel_logo/newrebel-simple-on-black.jpg">
</a>
<br>
<img width="90" height="20" alt="passing" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI5MCIgaGVpZ2h0PSIyMCI+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4Mj0iMCIgeTI9IjEwMCUiPjxzdG9wIG9mZnNldD0iMCIgc3RvcC1jb2xvcj0iI2JiYiIgc3RvcC1vcGFjaXR5PSIuMSIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1vcGFjaXR5PSIuMSIvPjwvbGluZWFyR3JhZGllbnQ+PHJlY3Qgcng9IjMiIHdpZHRoPSI5MCIgaGVpZ2h0PSIyMCIgZmlsbD0iIzU1NSIvPjxyZWN0IHJ4PSIzIiB4PSIzNyIgd2lkdGg9IjUzIiBoZWlnaHQ9IjIwIiBmaWxsPSIjNGMxIi8+PHBhdGggZmlsbD0iIzRjMSIgZD0iTTM3IDBoNHYyMGgtNHoiLz48cmVjdCByeD0iMyIgd2lkdGg9IjkwIiBoZWlnaHQ9IjIwIiBmaWxsPSJ1cmwoI2EpIi8+PGcgZmlsbD0iI2ZmZiIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZm9udC1mYW1pbHk9IkRlamFWdSBTYW5zLFZlcmRhbmEsR2VuZXZhLHNhbnMtc2VyaWYiIGZvbnQtc2l6ZT0iMTEiPjx0ZXh0IHg9IjE5LjUiIHk9IjE1IiBmaWxsPSIjMDEwMTAxIiBmaWxsLW9wYWNpdHk9Ii4zIj5idWlsZDwvdGV4dD48dGV4dCB4PSIxOS41IiB5PSIxNCI+YnVpbGQ8L3RleHQ+PHRleHQgeD0iNjIuNSIgeT0iMTUiIGZpbGw9IiMwMTAxMDEiIGZpbGwtb3BhY2l0eT0iLjMiPnBhc3Npbmc8L3RleHQ+PHRleHQgeD0iNjIuNSIgeT0iMTQiPnBhc3Npbmc8L3RleHQ+PC9nPjwvc3ZnPg=="><br>

NEWREBEL<sup>®</sup> GLSL Audio-Texture
===========

This will create a [ShaderToy®](https://www.shadertoy.com/) <em>(-like)</em> Audio Texture intended for use to send audio-data to a WebGL GLSL (Fragment) Shader. But there are probably more things you can use it for, that's for you and your creativity to decide. 

The texture is no bigger then 2 pixels high and 512 pixels wide. It contains all audio-data you need to create any visualization, or such. With just one <em>sampler2D</em> uniform you can send all data to your shader, which could provide a nice performance advantage in comparison to sending all that data in numerous uniforms after having to create separate values and outputs. The texture updates itself as the audio plays.

The audio-source can be either any [Soundcloud](https://soundcloud.com/) url, as a self-hosted <em>.mp3</em> or <em>.wav</em> file.  

The texture contains two horizontal rows. The top row (1 pixel) is the waveform which provides i.e. total peak-levels. The second row, also 1 pixel contains the spectrum FFT data providing 512 frequencies. A High-cut is auto-integrated in such way that everything works as should. <em>I use to be a professional musician and know what frequencies you don't need. </em>

> Initially it is created to function as kind of like a plugin for [Pixi.js](http://www.pixijs.com/). Tested with v4.0 - v4.7.0. But I have Included both a <em>WebGL</em> as <em>canvas</em> version, which you optionally can use to connect, render or bind in any way you like. <em>*Might you still work with Pixi v3, then you could choose to use one of these two alternate versions to render as a renderTexture</em>.

Audiofiles play instantly, the texture will be created instantly. It uses both the WebAudio API as HTML5 Audio in combination. There's no pre-load time or anything.

<h2>Install this <u>Plugin</u></h2>

Install with npm:
```bash
npm install --save-dev GLSL-audio-texture
```
Install with yarn:
```bash
yarn add GLSL-audio-texture--dev
```
Then you simply do:
```bash
npm install
```
To build:
```bash
npm run build
```
To run it on a dev server (webpack):
```bash
npm run start
```
After build you can do:
```bash
import AudioTexture from 'GLSL-audio-texture'
```
It's also possible to simply use:
```bash
<script>/dist/GLSL-audio-texture.min.js</script>
and upload /dist/GLSL-audio-texture.min.js.map in the same dir.
```
<em>in the package: webpack, babel etc.</em>

<h2>Introduction</h2>

### Get Started


