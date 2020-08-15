<template>
<div id="TabBar">
  <slot></slot>
</div>
</template>

<script>

export default {
  name:"TabBar"

}
</script>

<style scoped>
#TabBar{
  display:flex;
  position: fixed;
  bottom: 0px;
  left: 0px; 
  right: 0px;
  background-color: #f6f6f6;
  box-shadow: 0 -1px 1px rgba(100,100,100,.2);
}
</style>