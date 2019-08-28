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

<img src="https://media.giphy.com/media/VzetAs00R58i7KxaJc/giphy.gif">


## Installatoin

Using npm:

```shell
$ npm i --save vue-skeleton-screen
```

## Dependencies

- **Vue**, This is a component written in vue and can only use for Vue projects. For information, go to https://vuejs.org/.

## Api

| flag      | Type   | Default   | Description                                                  |
| --------- | ------ | --------- | ------------------------------------------------------------ |
| header    | Bool   | **true**  | header with or without a avatar along with a title and subtitle set to **false** to hide it. |
| avatart   | Bool   | **true**  | a round avatar in header, set to **false** to hide it.       |
| media     | Bool   | **true**  | media is a grey div stands for image to be loaded, set to **false** to hide it. |
| action    | Bool   | **false** | actions contains two action button placeholders, set to **true** to enable it. |
| lines     | Number | **2**     | display how many lines in text section.                      |
| round     | Bool   | **false** | set to **true** if you want rounded corner of the placeholder |
| dark      | Bool   | **false** | set to **true** to use dark theme.                           |
| isLoading | Bool   | **false** | set to **true** to display loading animation.                |

