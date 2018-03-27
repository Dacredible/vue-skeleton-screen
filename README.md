## Installatoin

Using npm:

```shell
$ npm i --save skeletoncard
```

##Api

####header

Type: Boolean

Default: true

Description: header contains a avatar along with a title and subtitle, set to **false** to hide it.

####media

Type: Boolean

Default: true

Description: media is a grey div stands for image to be loaded, set to **false** to hide it.

####text

Type: Boolean

Default: true

Description: text contains a paragraph title and multiple lines text which specifies in **lines**.

####actions

Type: Boolean

Default: false

Description: actions contains two action button place holders, set to **true** to enable it.

####horizontal

Type: Boolean

Default: false

Description: a horizontal display.

#### lines

Type: Number

Default: 2

Description: the lines number in text section.

#### round

Type: Boolean

Default: false

Description: set to **true** if you want rounded corner of the placeholder.

#### hover

Type: Boolean

Default: false

Description: set to **true** can offer a hover effect, same in vuetify.

## Usage

```html
<skeleton-card actions round hover></skeleton-card>
```



![pic](https://i.imgur.com/t8z1lKk.png)

