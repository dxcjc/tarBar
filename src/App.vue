<template>
  <div id="app">
    <div id="nav">
      <router-view></router-view>
      <tab-bar>
        <TabBarItem path="/home" isStyleActive="blue">
          <img slot="tab-bar-item-icon" src="@/assets/images/home.svg" alt="首页"/>
          <img slot="active" src="@/assets/images/home_active.svg" alt="首页"/>
          <h5 slot="tab-bar-item-text">首页</h5>
        </TabBarItem>
        <TabBarItem path="/category">
          <img slot="tab-bar-item-icon" src="@/assets/images/category.svg" alt="分类"/>
          <img slot="active" src="@/assets/images/category_active.svg" alt="分类"/>
          <h5 slot="tab-bar-item-text">分类</h5>
        </TabBarItem>
        <TabBarItem path="shopcart">
          <img slot="tab-bar-item-icon" src="@/assets/images/shopcart.svg" alt="购物车"/>
          <img slot="active" src="@/assets/images/shopcart_active.svg" alt="购物车"/>
          <h5 slot="tab-bar-item-text">购物车</h5>
        </TabBarItem>
        <TabBarItem path="profile">
          <img slot="tab-bar-item-icon" src="@/assets/images/profile.svg" alt="个人"/>
          <img slot="active" src="@/assets/images/profile_active.svg" alt="个人"/>
          <h5  slot="tab-bar-item-text">个人</h5>
        </TabBarItem>
      </tab-bar>
    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
import TabBar from '@/components/tabbar/TabBar.vue'
import Common from '@/assets/css/common.css'
import TabBarItem from '@/components/tabbar/TabBarItem.vue'
export default {
  name: 'app',
  components: {
    TabBar,TabBarItem
  }
}
</script>

<style>


</style>
