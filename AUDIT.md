# Audits on Bootstrap docs

## 1. Critical css

With gulp I automated generated critical css. This reduced the time before the initial render.

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/critical-css/before.png)

Before


![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/critical-css/after.png)

After

I reduced the first paint from `1.94s` to `258ms`.

## 2. CDN usage

I serve static files from CDN's where possible.

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/cdn/css_before.png)
Css before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/cdn/css_after.png)
Css after

This reduced the transfer size of css from `142kb (4.84s)` to `22.9kb (1.38s)`.

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/cdn/js_before.png)
Js before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/cdn/js_after.png)
Js after

This reduced the transfer size of js from `210kb` to `91.43kb`.

## 3. Minify css
I minified the css files I cannot serve from a CDN

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/minify-css/before.png)
Before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/minify-css/after.png)
After

This reduced docs.css from `30.5kb` to `20.7kb`

## 4. Minify html
I Minified the html files

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/minify-html/before.png)
Before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/minify-html/after.png)
After

This reduced the page size from `18,3kb` to `16,7kb`

## 5. Images converted to webp
With gulp I converted all the images to the .webp format. Also I automated replacing images in the html with pictures. These pictures first try to use the .webp sources and fallback to the original compressed images.

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/compress-images/before.png)
Before

![After compression](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/compress-images/after_compress.png)
After (original mimetypes)

With the original mimetypes I reduced the total transfer size of images from `729kb` to `215.9kb`.

![After webp](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/compress-images/after_webp.png)
After (webp)

With webp, I reduced the total transfer size of images to `177.0kb`

## 6. Gzip static files

![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/gzip/before.png)
Before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/gzip/after.png)
After

With enabling gzip, I reduced the total tranfer size with `45kb`.

## 7. Concat css files
![Before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/concat/before.png)
Before

![After](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/concat/after.png)
After

This concatenation reduced load time with `122ms`.

![Page speed insights - before](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/concat/gps_before.png)
Page speed insights - before

![Page speed insights - after](https://github.com/Frankwarnaar/minor-performance-matters-bootstrap/blob/master/audits/concat/gps_after.png)
Page speed insights - after
