# vue-svg-circle-progress-bar

![vue-progress.gif](https://i.loli.net/2020/04/11/ANuIagl3UScTYJK.gif)

Install
```javascript
npm i vur-circle-progress-bar
```

Using
```javascript
import CircleProgress from 'vue-svg-circle-progress-bar'

export default {
  components:{
   CircleProgress
  },
  data(){
    return {
      progressOption:{
        progressColor:'yello',
        progress:50,
        text:"50%"
      }
    }
  }
}
```
```javascript
<CircleProgress :progressOption = "progressOption"/>
```

see the `prop` in `progressOption`
| props | default | type | description |
| ------ | ------ | ------ |------ |
| progress | 50 | Number |  progress   |
| text | 50 | String |the progress text|
| bgColor | #F6F6F6 | String |backgroundColor of progress|
| progressColor | #FF0000 | String |progressColor of progress|
| strokeWidth | 10 | Number | width of progress|
| radius | 50 | Number |radius of progress|
| animate | false | Boolean |  animate or not    |
| dur | 1 | Number |during of animation|


## keywords
`vue` `svg` `progress`
