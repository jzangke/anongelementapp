<template>
  <div class="footer">
    <ul>
      <li v-for="(item,index) in navs">
        <router-link :to="item.path">
          <i class="iconfont" v-html="item.icon"></i>
          <span>{{item.name}}</span>
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navs: [
        {
          name: "首页",
          icon: "&#xe61f;",
          path: "/home"
        },
        {
          name: "分类",
          icon: "&#xe60e;",
          path: "/classification"
        },
        {
          name: "购物车",
          icon: "&#xe66e;",
          path: "/buyCar"
        },
        {
          name: "个人中心",
          icon: "&#xe606;",
          path: "/personal"
        }
      ]
    };
  }
};
</script>

<style lang="">
.footer {
  width: 100%;
  height: 0.98rem;
  position: fixed;
  left: 0;
  bottom: 0;
  background: #ffffff;
}
.footer > ul {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.footer > ul > li > a {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.footer > ul > li > a > i {
  font-size: 40px;
}
</style>