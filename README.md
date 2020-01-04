# EJS Preview

[![Donate](https://amrayn.github.io/donate.png?v2)](https://amrayn.com/donate)

```
yarn global add ejs-preview
```

```
ejs-preview --root=/path/to/root/files --common=/json/file.json
```

* `root`: Path to the root files. e.g, `/app/src/templates`
* `common`: Path to JSON file. Common data for all the templates. e.g, `/app/src/templates/preview-common.json`

Once server is running you can pass following query parameters

* `template`: EJS file base to render (relative to root) e.g, `?template=emails/welcome` will render `<root>/emails/welcome.ejs`.

  The template specific data is picked up from `<root>/emails/welcome.preview.js` which should look like:

```
module.exports = {
  activationLink: '/link',
};
```
* `common` If you want to override `common` args provided at the startup
* `plain` If specified `plain/text` content-type is sent

You can change the port with `PORT` environment variable


# License
```
The MIT License (MIT)

(c) 2020 Amrayn Web Services
(c) 2020 @abumusamq

https://amrayn.com
https://humble.js.org

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
