<template>
  <footer
    class="w-full absolute bottom-0 bg-gray-800 h-56 flex flex-col justify-evenly items-center"
  >
    <div class="flex text-center">
      <router-link
        v-for="entry in entries"
        :key="entry.to"
        :to="entry.to"
        :exact="entry.exact"
        class="block text-base leading-6 font-normal text-gray-500 hover:text-gray-400 mx-5"
      >
        {{ entry.label }}
      </router-link>
    </div>
    
    <div class="text-base leading-6 font-normal text-gray-400">
      © 2021 Gonstack.com.
    </div>
  </footer>
</template>
<script>
export default {
  name: 'Footer',
  computed: {
    entries() {
      return [
        {
          label: 'Tất cả tài sản',
          to: '/all-items',
          exact: true
        },
        {
          label: 'Đang đăng bán',
          to: '/for-sale',
          exact: true
        },
        {
          label: 'Trả giá cao nhất',
          to: '/highest-bids',
          exact: true
        },
        {
          label: 'Gần nhất',
          to: '/recently-added',
          exact: true
        }
      ];
    }
  }
};
</script>
