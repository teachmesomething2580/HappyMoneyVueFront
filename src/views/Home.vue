<template>
  <div class="home">
    <EventCarousel :events="events"/>
    <MainService />
    <Notice :hostname="hostname"/>
    <GiftMall />
    <RecommandPrd :hostname="hostname"/>
    <EventSection :events="events" />
    <JoinStore :hostname="hostname"/>
    <Etc />
  </div>
</template>

<script>
import EventCarousel from '@/components/index/EventCarousel.vue'
import MainService from '@/components/index/MainService.vue'
import Notice from '@/components/index/Notice.vue'
import GiftMall from '@/components/index/GiftMall.vue'
import RecommandPrd from '@/components/index/RecommandPrd.vue'
import EventSection from '@/components/index/EventSection.vue'
import JoinStore from '@/components/index/JoinStore.vue'
import Etc from '@/components/index/Etc.vue'

export default {
  name: 'home',
  components: {
    EventCarousel,
    MainService,
    Notice,
    GiftMall,
    RecommandPrd,
    EventSection,
    JoinStore,
    Etc
  },
  data() {
    return {
      events: [],
      hostname: require('@/assets/js/variable.js').hostname
    }
  },
  methods: {
    getAPIEventLists() {
      const url = this.hostname + '/apis/event/?page_size=20';
      this.$http.get(url).then(
        response => {
          if (response.status == '200') {
            this.events = response.data.results;
          }
        },
        error => {
          
        });
    }
  },
  created() {
    // API Event List(6개) 가져오기
    this.getAPIEventLists();
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Nanum+Gothic');

html, body, ul {
  margin: 0;
  padding: 0;
  font-family: 'Nanum Gothic', sans-serif;
  overflow-x: hidden;
}

*, *::after, *::before { box-sizing:border-box; }

a {
  color: black;
  text-decoration: none;
}

.clearfix {
  overflow: hidden;
  &:after {
    display: block;
    content:"";
    clear: both;
  }
}
</style>
