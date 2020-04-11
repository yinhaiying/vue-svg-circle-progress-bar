<template>
  <div class="circle-progress">
    <svg :height="option.size" :width="option.size" x-mlns="http://www.w3.org/200/svg">
    <circle
      :r="option.radius"
      :cx="option.cx"
      :cy="option.cy"
      :stroke="option.bgColor"
      :stroke-width="option.strokeWidth"
      fill="none"/>
    <circle
      :r="option.radius"
      :cx="option.cx"
      :cy="option.cy"
      :stroke="option.progressColor"
      :stroke-dasharray="option.strokeDasharray"
      :stroke-width="option.strokeWidth"
      fill="none"
      stroke-linecap="round"
      transform="rotate(-90)"
      transform-origin="center">
      <animate
        v-if = "option.animate"
        from="0"
        :to="Math.PI * 2 * option.radius * option.progress /100"
        begin="0s"
        :dur="option.dur"
        attributeName="stroke-dasharray"
        fill="freeze"
      />
      </circle>
    </svg>
    <span class = "progress-text">{{progressOption.text}}</span>
  </div>
</template>

<script>
export default {
  name:'CircleProgress',
  data(){
    return {
      r:50
    }
  },
  props:{
    progressOption:Object
  },
  computed:{
    option(){
      let baseOption = {
        bgColor:'#F6F6F6',
        progressColor: 'yellow',
        strokeWidth:10,
        radius:50,
        dur:1,
        animate:false
      };
      Object.assign(baseOption,this.progressOption);
      baseOption.cy = baseOption.cx = baseOption.radius + baseOption.strokeWidth;
      baseOption.size = (baseOption.radius + baseOption.strokeWidth) * 2;
      let l = Math.PI * 2 * baseOption.radius * this.progressOption.progress/100;
      baseOption.strokeDasharray = `${l},10000`
      return baseOption;
    }
  }
}
</script>

<style lang = "less" scoped>
.circle-progress {
  display:inline-block;
  position:relative;
}
.circle-progress .progress-text{
    font-size:20px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translateX(-50%) translateY(-50%);
}
</style>
