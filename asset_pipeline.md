# Asset pipeline

`#rails` `#asset_pipeline`

* **What is the “Asset Pipeline”?**
  > The process of *flattening* and *mashing* all asset files of the same file type together into *one big file* (and then minify it).
  > * Asset Pipeline provides a framework to *concatenate* and *minify* (or compress) JavaScript and CSS assets.
  >  
  > The benefit of  Asset Pipeline, we can:
  >  * Minify
  >  * Compile
  >  * Fingerprint

* **What are “Manifest Files”?**
  > Special files determine which asset file to include in Asset Pipeline


* **Why would you namespace your stylesheets?**
  > namespace stylesheets to make only a portion of the stylesheets available to only a specific set of views similarly to javacsript 


* **What does it mean to “Escape” HTML?**
  > when escape HTML the HTML code will be display as normal text

---
* *loadpaths* include paths to access all assset files
* path to asset files are flattened
* *application* manifest files  (applicaton.js, application.css) determine which file to include, then pre-compile files, then mashing/stacking files (of the same type) together into one big one, then minify/compress it

---
* **Why use asset pipeline**
  > 1. asset specified separately must be retrieved separately => high number of HTTP requests
  > 2. Raw javascript, css file waste a lot of bandwidth with comments, extra space, long variable names
  > 3. Caching => the browser won’t know when the asset file changes (because the name is the same)
  > 4. Can use pre-processor to pre-processing asset file (Coffescript, Sass, ERB, Less…)

  > The asset pipeline can solve all the problem above when used properly.
  > 1. It can compile multiple asset into one
  > 2. minify and compress assets
  > 3. provide digesting of assets to avoid caching issues
  > 4. pro-process alternative language and turn them into JavaScript and CSS

---
From perspective of Rails Developer, there are 3 main features to understand about asset pipeline
  1. asset directories
  2. manifest files
  3. preprocessor engines