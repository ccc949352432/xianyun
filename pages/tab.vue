<template>
  <div>
    <div class="top">
      <span
        v-for="(item, index) in ['新闻', '体育', '军事']"
        :key="index"
        :class="{active:current===index}"
        @click="handleClick(index)"
      >{{ item }}</span>
    </div>
    <div v-if="current===0">
      <ul>
        <li>这是最近的新闻</li>
        <li>这是最近的新闻</li>
        <li>这是最近的新闻</li>
      </ul>
    </div>
    <div v-if="current===1">
      <ul>
        <li>这是最近的体育</li>
        <li>这是最近的体育</li>
        <li>这是最近的体育</li>
      </ul>
    </div>
    <div v-if="current===2">
      <ul>
        <li>这是最近的军事</li>
        <li>这是最近的军事</li>
        <li>这是最近的军事</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: 0
    }
  },
  methods: {
    handleClick(index) {
      this.current = index
    }
  }
}
</script>

<style>
.top {
  margin-bottom: 20px;
}
.top span {
  cursor: pointer;
  margin-left: 20px;
}
.active{
  color:red
}
</style>
