<template>
  <a-layout>
    <the-head></the-head>
    <!--<a-layout-header class="header">-->
      <!--<div class="logo" />-->
      <!--<a-menu-->
              <!--theme="dark"-->
              <!--mode="horizontal"-->
              <!--v-model:selectedKeys="selectedKeys1"-->
              <!--:style="{ lineHeight: '64px' }"-->
      <!--&gt;-->
        <!--<a-menu-item key="1">nav 1</a-menu-item>-->
        <!--<a-menu-item key="2">nav 2</a-menu-item>-->
        <!--<a-menu-item key="3">nav 3</a-menu-item>-->
      <!--</a-menu>-->
    <!--</a-layout-header>-->
    <router-view/>
    <!--<a-layout-footer style="text-align: center">-->
      <!--Ant Design ©2018 Created by Ant UED-->
    <!--</a-layout-footer>-->
    <the-footer></the-footer>
  </a-layout>
</template>
<script>
  import { UserOutlined, LaptopOutlined, NotificationOutlined } from '@ant-design/icons-vue';
  import { defineComponent, ref } from 'vue';
  import TheHead from '@/components/the-head';
  import TheFooter from '@/components/the-footer';
  // import HelloWorld from '@/components/Helloworld';
  export default defineComponent({
    components: {
      // UserOutlined,
      // LaptopOutlined,
      // NotificationOutlined,
      TheHead,
      TheFooter,
      // HelloWorld,
    },

    setup() {
      return {
        selectedKeys1: ref(['2']),
        selectedKeys2: ref(['1']),
        collapsed: ref(false),
        openKeys: ref(['sub1']),
      };
    },
  });
</script>
<style>
  #components-layout-demo-top-side-2 .logo {
    float: left;
    width: 120px;
    height: 31px;
    margin: 16px 24px 16px 0;
    background: rgba(255, 255, 255, 0.3);
  }

  .ant-row-rtl #components-layout-demo-top-side-2 .logo {
    float: right;
    margin: 16px 0 16px 24px;
  }

  .site-layout-background {
    background: #fff;
  }
</style>