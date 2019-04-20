<template>
  <view>
    <calendar
      :date="date"
      :lunar="true"
      :disable-before="true"
      :start-date="'2019-3-2'"
      :end-date="'2019-5-20'"
      @change="change"
      @to-click="toClick"
    />
  </view>
</template>

<script>

import calendar from '@dcloudio/uni-ui/lib/uni-calendar/uni-calendar.vue';

export default {
  components: {
    calendar,
  },
  data() {
    return {
      date: '2019-03-15',
      myDate: ''
    };
  },
  methods: {
    change(e) {
      this.myDate = e.fulldate
    },
    toClick(e) {
      this.myDate = e.fulldate
    },
  },
};
</script>
