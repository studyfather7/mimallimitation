<template>
  <mi-topbar/>
  <mi-header/>
  <mi-banner/>
  <mi-content/>
  <mi-footer/>
  <mi-sidebar/>
</template>

<script>
import MiBanner from './components/MiBanner.vue'
import MiContent from './components/MiContent.vue'
import MiHeader from './components/MiHeader'
import MiTopbar from './components/MiTopbar'
import MiFooter from './components/MiFooter.vue'
import MiSidebar from './components/MiSidebar.vue'
export default {
  name: 'App',
  components: { MiTopbar, MiHeader, MiBanner, MiContent, MiFooter, MiSidebar },
}
</script>

<style>
@import url(./assets/css/home.c43682e3.css);
* {
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
  margin: 0;
  padding: 0;
}

body {
  font: 14px/1.5 Helvetica Neue,Helvetica,Arial,Microsoft Yahei,Hiragino Sans GB,Heiti SC,WenQuanYi Micro Hei,sans-serif;
  min-width: 1226px;
  margin: 0;
}

ul {
  list-style-type: none;
}

h2 {
  font-size: 22px;
  font-family: Helvetica Neue;
  color: #333;
  line-height: 58px;
  font-weight: 200;
}

del {
  text-decoration: line-through;
  color: #b0b0b0;
}

.wrapper {
  position: relative;
  width: 1226px;
  margin-left: auto;
  margin-right: auto;
}
</style>
