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
        progressColor:'yello'
      }
    }
  }
}
```
```javascript
<CircleProgress :progressOption = "progressOption"/>
```

see the `prop` in `progressOption`
| props | default | type |
| ------ | ------ | ------ |
| bgColor | #F6F6F6 | String |
| progressColor | #FF0000 | String |
| strokeWidth | 10 | Number |
| radius | 50 | Number |
| animate | false | Boolean |
| dur | 1 | Number |


## keywords
`vue` `svg` `progress`
