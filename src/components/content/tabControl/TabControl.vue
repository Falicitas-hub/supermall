<template>
  <div class="tab-control">
    <div
      v-for="(item, index) in titles"
      class="tab-control-item"
      :class="{ active: currentIndex === index }"
      @click="tabClick(index)"
    >
      <span>{{ item }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    titles: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    tabClick(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style>
.tab-control {
  display: flex;
  height: 44px;
  line-height: 44px;
  font-size: 18px;
  position: sticky;
  top: 44px;
  background-color: #fff;
}
.tab-control-item {
  flex: 1;
  text-align: center;
}
.tab-control-item span {
  padding-bottom: 5px;
}
.active {
  color: var(--color-high-text);
}
.active span {
  border-bottom: 3px solid var(--color-high-text);
}
</style>