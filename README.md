## Usage

```javascript
//javascript
import SkeletonCard from 'vue-skeleton-screen'
...
export default{
...
	components: {
    	SkeletonCard,
	}
...
};
```



```html
<!-- html -->
<skeleton-card actions round hover></skeleton-card>
```

<img style="float: left;" src="https://i.imgur.com/t8z1lKk.png">

<img style="float: right;" src="https://i.imgur.com/UXpuhbs.png">



## Installatoin

Using npm:

```shell
$ npm i --save vue-skeleton-screen
```

## Dependencies

- **Vuetify**, not included in package, you should install it on your own. For information, go to https://vuetifyjs.com/en/.

## Api

#### - header

Type: Boolean

Default: **true**

Description: header contains a avatar along with a title and subtitle, set to **false** to hide it.

#### - media

Type: Boolean

Default: **true**

Description: media is a grey div stands for image to be loaded, set to **false** to hide it.

#### - text

Type: Boolean

Default: **true**

Description: text contains a paragraph title and multiple lines text which specifies in **lines**.

#### - actions

Type: Boolean

Default: **false**

Description: actions contains two action button place holders, set to **true** to enable it.

#### - horizontal

Type: Boolean

Default: **false**

Description: a horizontal display.

#### - lines

Type: Number

Default: **2**

Description: the lines number in text section.

#### - round

Type: Boolean

Default: **false**

Description: set to **true** if you want rounded corner of the placeholder.

#### - hover

Type: Boolean

Default: **false**

Description: set to **true** to have a hover effect, same in vuetify.



