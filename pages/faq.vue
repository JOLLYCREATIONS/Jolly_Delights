<template>
  <div class="relative w-full h-[50vh] flex flex-col justify-center">
    <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
  </div>
  <div>
    <img src="/faq.png" />
  </div>
  <div class="accordion mx-auto mb-16 p-8 max-w-7xl xl:max-w-[90rem]">
    <div v-for="(item, index) in items" :key="index" class="accordion-item">
      <MiscAccordian :title="item.title">
        <div class="text-xl text-semibold">{{ item.content }}</div>
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
        { title: 'What types of events do you cater to?', content: 'Weddings, corporate gatherings, private parties, conferences, and more.' },
        { title: 'Do you provide full-service catering, including setup and cleanup?', content: 'Yes, our full-service catering includes setup, cleanup, ensuring a seamless experience.' },
        { title: 'How far in advance do I need to place an order ?', content: 'As far in advance as possible, especially for large events. we try to accommodate short notice orders whenever possible.' },
        { title: 'What safety measures do you have in place for food handling and delivery?', content: 'Food safety is our top priority. we follow strict hygiene and sanitation protocols throughout the process.' },
        { title: 'What is your cancellation policy?', content: 'The cancellation policy varies depending on the circumstances and timing. Contact us as soon as possible.' }
      ]
      
    };
  },
};
</script>
