# presskit-static()

A Hugo theme for generating static presskit()-like sites. No PHP necessary!

presskit-static() is a theme you can use with Hugo to generate a presskit as static HTML, which you can then upload to Amazon S3 or Google Cloud Storage. You don't need to run a dedicated server for your Presskit, and you don't need to worry about your hosting provider going down (both S3 and GCS provide at least 99.9% uptime SLA). As an added bonus, S3 and Google Cloud Storage are often orders of magnitude cheaper than paying for shared hosting or a VPS.

## Getting Started

First you need to [install Hugo](https://gohugo.io/getting-started/installing/). It's available for every major operating system. Once this is done, you should be able to type "hugo" at the command line.

Create a new Hugo site with:

```
hugo new site
```


