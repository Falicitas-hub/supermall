<template>
  <div class="recommend">
    <div v-for="item in recommends" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="" />
        <div>{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    recommends: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style>
.recommend {
  display: flex;
}
.recommend-item {
  flex: 1;
  text-align: center;
  padding-top: 10px;
  padding-bottom: 30px;
  border-bottom: 10px solid #eee;
}
.recommend-item img {
  width: 100%;
  padding-bottom: 10px;
}
</style>