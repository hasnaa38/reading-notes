# Code 201 - Read 11

In this file, a summary of **Read: 11 - Assorted Topics** will be provided. The read covers two chapters from *HTML & CSS: Design and Build Websites*, written by Jon Duckett. Along with an MDN article.

## Table of contents

* From the Duckett HTML and CSS book

| Chapter      | Topic |
| -----------  | ----------- |
| Chapter 16   | Images       |
| Chapter 10   | Practical Information | 

* Article: [Video and Audio APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)

## Chapter 16: Images [CSS]

Images can be controlled via CSS to keeps rules that affect the presentation of a page in the CSS and out of the HTML markup.

***NOTE*** By default, images are inline elements. This means that they flow within the surrounding text.

### Specifying the size of an image

> Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.

The size of images be controlled using the `width` and `height` properties.


### Specifying the alignment of an image

The `float` property can be used to align images to the left/right of the page.

To center images, do the following: 

1. Use the `display` property with a value of block to turn it into a block level element.

2. Use the `text-align` property with a value of center on the containing element OR use the use the `margin` property on the image itself.

### Add background images to boxes

The background can be changed for entire HTML page or just a part of it.

The `background` property acts like a shorthand for all the background properties, them being:

1. background-color: to choose a color for the background.
2. background-image: to place an image behind any HTML element.
3. background-repeat: to specify whether a background image is repeated either horizontally, vertically, or both.
4. background-attachment: to specify whether a background image should stay in one position or move as the user scrolls up and down the page.
5. background-position: to specify where in the browser window the background image should be placed.

### Sprites

When a single image is used for several different parts of an interface, it is known as a *sprite*.

The advantage of using sprites is that the web browser only needs to request one image rather than many images, which can make the web page load faster.'

## Chapter 19: Practical Information

* Search engine optimization (SEO) is the practice of trying to let your site appear nearer the top of search engine results when people look for the topics that your website covers. It helps visitors find your sites when using search engines.

* Analytics tools such as Google Analytics allow you to see how many people visit your site, how they find it, and what they do when they get there.

* To put your site on the web, you will need to obtain a domain name and web hosting.

### Article: Video and Audio APIs

HTML5 allows embedding video and audio content to web pages via the `<video>` and `<audio>` elements, along with JavaScript APIs for controlling them.

Example - embedding an mp4 video to a web page:

```
<video src="rabbit320.mp4" controls>
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.webm">link to the video</a> instead.</p>
</video>
```

* The source attribute `src` contains a path to the video.
* Users must be able to control video and audio playback, you have two options to do so:

1. Use the `controls` attribute to include the browser's own control interface
2. Build your own interface using the appropriate JavaScript API. At a minimum, the interface must include a way to start/stop the media, and adjust the volume.

#### Media formats

Video and audio formats define a structure in which media tracks are stored, along with metadata describing it, what codecs are used to encode its channels, etc. Formats like MP3, MP4 and WebM are known as container formats. The video and audio tracks within the container hold data in the appropriate format for the codec used to encode that media.

Different browsers support different video and audio formats, and different container formats. For example, an MP4 container often packages AAC or MP3 audio with H.264 video. 

Therefore, it is advised to add multiple formats for the media by adding each one using the `<source>` element. Then use the `type` attribute to specify the MIME type of each media source. Browsers can use the `type` to immediately skip videos they don't understand. If `type` isn't included, browsers will load and try to play each file until they find one that works, which obviously takes time and is an unnecessary use of resources. Example:

```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

#### Other features

##### width and height

The width and height attributes are used to control the video size either with these attributes or with CSS. Audio tracks have no visual component, therefore, they don't support these attributes.

##### autoplay

It makes the audio or video start playing right away, while the rest of the page is loading. You are advised not to use autoplaying media on your page; because users can find it really annoying.

##### loop

It makes the video or audio start playing again whenever it finishes.

##### muted

It causes the media to play with the sound turned off by default.

##### poster

The URL of an image which will be displayed before the video is played (like a thumbnail). Audio tracks have no visual component, therefore, they don't support this attribute.

##### preload

Used for buffering large files; it can take one of three values:

1. `none` - doesn't buffer the file
2. `auto` - buffers the media file
3. `metadata` - buffers only the metadata for the file