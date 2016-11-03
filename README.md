# markdown-it-youtube-vimeo

> markdown-it plugin for embedding videos hosted on YouTube and Vimeo.

## Usage

#### Enable plugin

```js
var md = require('markdown-it')({
  html: true,
  linkify: true,
  typography: true
}).use(require('markdown-it-video', { // <-- this use(package_name) is required
  youtube: { width: 640, height: 390 },
  vimeo: { width: 500, height: 281 },
  vine: { width: 600, height: 600, embed: 'simple' },
  prezi: { width: 550, height: 400 }
}));
```

#### YouTube

This only works in the inline style.

```md
@[youtube](dQw4w9WgXcQ)
```

is interpreted as

```html
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" id="youtubeplayer" type="text/html" width="640" height="390"
  src="//www.youtube.com/embed/dQw4w9WgXcQ"
  frameborder="0"/></div></p>
```

Alternately, you could use a number of different YouTube URL formats rather than just the video id.

```md
@[youtube](http://www.youtube.com/embed/dQw4w9WgXcQ)
@[youtube](https://www.youtube.com/watch?v=dQw4w9WgXcQ&feature=feedrec_centerforopenscience_index)
@[youtube](http://www.youtube.com/user/IngridMichaelsonVEVO#p/a/u/1/QdK8U-VIH_o)
@[youtube](http://www.youtube.com/v/dQw4w9WgXcQ?fs=1&amp;hl=en_US&amp;rel=0)
@[youtube](http://www.youtube.com/watch?v=dQw4w9WgXcQ#t=0m10s)
@[youtube](http://www.youtube.com/embed/dQw4w9WgXcQ?rel=0)
@[youtube](http://www.youtube.com/watch?v=dQw4w9WgXcQ)
@[youtube](http://youtu.be/dQw4w9WgXcQ)
```

#### Vimeo

This only works in the inline style.

```md
@[vimeo](19706846)
```

is interpreted as

```html
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" id="vimeoplayer" type="text/html" width="500" height="281"
  src="//player.vimeo.com/video/19706846"
  frameborder="0"/></div></p>
```

Alternately, you could use the url instead of just the video id.

```md
@[vimeo](https://vimeo.com/19706846)
@[vimeo](https://player.vimeo.com/video/19706846)
```
