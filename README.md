# presskit-static()

A Hugo theme for generating static presskit()-like sites. No PHP necessary!

presskit-static() is a theme you can use with Hugo to generate a presskit as static HTML, which you can then upload to Amazon S3 or Google Cloud Storage. You don't need to run a dedicated server for your Presskit, and you don't need to worry about your hosting provider going down (both S3 and GCS provide at least 99.9% uptime SLA). As an added bonus, S3 and Google Cloud Storage are often orders of magnitude cheaper than paying for shared hosting or a VPS.

## Getting Started

### 1. Initial setup

First you need to [install Hugo](https://gohugo.io/getting-started/installing/). It's available for every major operating system. Once this is done, you should be able to type "hugo" at the command line.

Create a new Hugo site with:

```
hugo new site
```

With your new site created, [download the presskit-static ZIP](https://github.com/RedpointGames/presskit-static/archive/master.zip) and place it in the `themes/` directory such that `themes/presskit-static/theme.toml` exists.

Add the line `theme = "presskit-static"` to your `config.toml` file.

You can run Hugo as a server locally while you're writing content to preview it by running `hugo server -t presskit-static` in the directory where your project is located.

### 2. Add pages

You now need to add pages to the `content/` directory.  You can copy the files inside `content-examples/` directory to your content directory to get a presskit up and running quickly.

### 3. Add images

You can add logos, videos and images to your presskit site by placing resources in the following directories, with the same layout used as in the PHP-version of presskit():

- `static/<id>/images` - For image files
- `static/<id>/images/images.zip` - For a ZIP file of all images
- `static/<id>/images/logo.zip` - For a ZIP file of all logos
- `static/<id>/logos` - For logos
- `static/<id>/trailers` - For .mp4 or .mov trailers (games only)
- `static/<id>/videos` - For .mp4 or .mov videos (companies only)

The `<id>` is the value of the `id: ` field in the company or game document. Unlike the PHP version of presskit(), this allows for multiple companies and games to have their own assets.

### 4. Generate HTML files

From the command line, run:

```
hugo -d ./dist
```

The `dist` folder will now have a set of static HTML files, images and other assets you can directly upload to S3 or Google Cloud Storage.

## License

```
Copyright 2017 Redpoint Games Pty Ltd

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```