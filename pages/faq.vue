<template>
  <div class="relative w-full h-[50vh] flex flex-col justify-center">
    <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
  </div>
  <div>
    <img src="/faq.png" />
  </div>
  <div class="accordion mx-auto mb-16 max-w-7xl xl:max-w-[90rem]">
    <div v-for="(item, index) in items" :key="index" class="accordion-item">
      <MiscAccordian :title="item.title">
        <div>{{ item.content }}</div>
      </MiscAccordian>
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
};
</script>
