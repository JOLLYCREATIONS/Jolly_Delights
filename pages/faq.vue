<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div >
        <img src="/faq.png"/>
    </div>
    <div class="accordion mx-auto mb-16 max-w-7xl xl:max-w-[90rem]">
    <div
      v-for="(item, index) in items"
      :key="index"
      class="accordion-item"
    >
      <div class="accordion-title" @click="toggleItem(index)">
        {{ item.title }}
        <span v-if="isOpen(index)" class="accordion-icon">-</span>
        <span v-else class="accordion-icon">+</span>
      </div>
      <div v-if="isOpen(index)" class="accordion-content">
        {{ item.content }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      openIndex: null,
      items: [
        { title: 'Item 1', content: 'Content of item 1' },
        { title: 'Item 2', content: 'Content of item 2' },
        { title: 'Item 3', content: 'Content of item 3' }
      ]
    };
  },
  methods: {
    toggleItem(index) {
      if (this.openIndex === index) {
        this.openIndex = null;
      } else {
        this.openIndex = index;
      }
    },
    isOpen(index) {
      return this.openIndex === index;
    }
  }
};
</script>
<style scoped>
.accordion {
  width: 100%;
}

.accordion-item {
  border: 1px solid #ffff;
  margin-bottom: 5px;
}

.accordion-title {
  background-color: #fffff;
  color:#3C7B42;
  padding: 10px;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.accordion-content {
  padding: 10px;
}

.accordion-icon {
  font-size: 20px;
}
</style>