
language-haml
=============
[Haml](http://haml.info/) language grammar for GitHub's [Atom](https://atom.io/) IDE.

![screenshot](http://ridingtheclutch.com.s3.amazonaws.com/images/language-haml.png)

## Supported Filetypes

* `.haml`
* `.hamlc` (CoffeeScript Haml)

## Supported filters

You can switch to another language right in the middle of your Haml file by
using a "filter":

![screenshot](http://ridingtheclutch.com.s3.amazonaws.com/images/haml_filters.png)

This Haml bundle currently supports the following filters:

* `:css`
* `:coffee`
* `:javascript`
* `:markdown`
* `:php`
* `:ruby`
* `:ruby2js`
* `:sass`
* `:scss`

The Haml documentation lists the following additional filters:

* `:cdata`
* `:erb`
* `:escaped`
* `:less`
* `:plain`
* `:preserve`
* `:textile`

To add more you can simply copy and paste one of the captures in the `ruby haml.cson` file
and make the changes necessary to support your filter of choice:

```cson
{
  'begin': '^(\\s*)(:css)'
  'beginCaptures':
    '2':
      'name': 'entity.name.tag.haml'
  'end': '^(?! *$|\\1 )'
  'name': 'source.css.embedded.html'
  'patterns': [
    {
      'include': 'source.css'
    }
  ]
}
```
