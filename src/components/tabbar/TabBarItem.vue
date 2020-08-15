<template>
  <div class="tab-bar-item"  @click="itemclick">
      <div  v-if="!isActive" ><slot name="tab-bar-item-icon" ></slot></div>
     <div v-else> <slot  name="active"></slot></div>
     <div :style="isStyleActive"><slot name="tab-bar-item-text"></slot></div>
      
  </div>
</template>
<script>
export default {
  name:"TagBarItem",
  props:{
    path: {
        type: String,
    },
    activeStyle: {
        type: String,
        default: 'deeppink'
    }
  },
  data(){
    return {
      // isActive: true
      
    }
  },
  methods:{
    itemclick(){
      this.$router.replace(this.path)
    }
  },
  computed: {
    isActive() {
        return this.$route.path.indexOf(this.path) !== -1
    },
    isStyleActive() {
        return this.isActive ? {color:this.activeStyle} : {}
    }
 }
  
}
</script>

<style>
.tab-bar-item{
  flex: 1;
  text-align: center;
  height: 49px;
  
  
}
.tab-bar-item img{
  width: 24px;
  height: 24px;
  vertical-align: middle;
  margin: 4px 0 2px 0;
}
.tab-bar-item h5{
  font-size: 14px;
}




</style>
