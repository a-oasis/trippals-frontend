<script setup>
import { ref } from 'vue'
import MainCard from '@/components/MainCard.vue'

let bestBoard = ref([
  {thumbnail: 'https://wimg.mk.co.kr/meet/neds/2020/05/image_readtop_2020_506007_15897737584203733.jpg', title: '`포스트 코로나 워너비 여행지`, 전세계 1위로 꼽힌 나라가?' },
  {thumbnail: 'https://newsroom-prd-data.s3.ap-northeast-2.amazonaws.com/wp-content/uploads/2024/02/%EC%A7%80%EB%82%9C%ED%95%B4%EC%97%90-%EA%B0%80%EC%9E%A5-%EC%9D%B8%EA%B8%B0-%EC%9E%88%EB%8D%98-%EC%97%AC%ED%96%89%EC%A7%80%EB%8A%94-%EC%9D%BC%EB%B3%B8-%EB%9C%A8%EB%8A%94-%EC%97%AC%ED%96%89%EC%A7%80%EB%8A%94-%EC%96%B4%EB%94%94_01-1200x777.png', title: '지난해에 가장 인기 있던 여행지는 일본! 뜨는 여행지는 어디?' },
  {thumbnail: 'https://www.opinionnews.co.kr/news/photo/202008/37778_27871_4042.png', title: '[주말엔 뭐하지?] 우리나라 맞아? \'외국 감성\' 폭발하는 국내 여행지들' },
  {thumbnail: 'https://tgzzmmgvheix1905536.cdn.ntruss.com/2020/07/a8db9da6f35c4b95b62976597f846c48', title: '여행지 선택부터 기내식까지, 방구석 여름 휴가법' },
]);

let latestBoard = ref([
  {thumbnail: 'https://wimg.mk.co.kr/meet/neds/2022/07/image_readtop_2022_589210_16570008355097198.jpg', title: '올 상반기 한국인 제일 많이 검색한 국내 여행지는 제주…해외는?' },
  {thumbnail: 'https://t1.daumcdn.net/thumb/R720x0/?fname=http://t1.daumcdn.net/brunch/service/user/STq/image/JMwoK5KKWwE8DiIEqIX0TeBHi1M.jpg', title: '미세먼지 피해 떠나는 청정 힐링 여행지 TOP7' },
  {thumbnail: 'https://www.travelnbike.com/news/photo/201806/59638_91021_3124.jpg', title: '올해 여름휴가철 해외여행 키워드 동남아·휴양·가족·실속' },
  {thumbnail: 'https://statics.vinpearl.com/%EB%B2%A0%ED%8A%B8%EB%82%A8-%EC%97%AC%ED%96%89%EC%A7%80-2_1655286956.jpg', title: '베트남에서 꼭 가봐야 할 도시 & 여행지 BEST 10' },
]);

</script>

<template>
  <div class="container">
    <div id="header" class="position-relative py-6 m-auto mt-5 rounded-5 shadow-lg">
      <div id="gradient" class="w-100 h-100 rounded-5 text-center">
      </div>
      <div class="position-absolute top-50 start-50 translate-middle">
        <h1 class="display-4 fw-bolder text-white w-100 text-center">Plan. Travel. Share.</h1>
        <p class="tab-content text-center text-white">Start your next adventure here: plan your trip, book experiences, and share your journey with a community of travelers.</p>

        <div class="input-group">
          <input type="search" class="form-control rounded" placeholder="Search" aria-label="Search" aria-describedby="search-addon" />
          <button type="button" class="btn btn-primary">search</button>
        </div>
      </div>
    </div>

    <hr class="m-5"/>
    <h3 class="ms-5 mb-3">Latest Review</h3>
    <div class="d-flex justify-content-center justify-content-between flex-wrap w-100 px-lg-5">
      <MainCard v-for="(item, index) in latestBoard" :key="index" :board="item"/>
    </div>
    <hr class="m-5"/>
    <h3 class="ms-5 mb-3">Best Review</h3>
    <div class="d-flex justify-content-center justify-content-between flex-wrap w-100 px-lg-5">
      <MainCard v-for="(item, index) in bestBoard" :key="index" :board="item"/>

    </div>
    <hr class="m-5"/>
  </div>

</template>

<style scoped>
  #header {
    height: 600px;
    width: 85%;
    background-image: url("../assets/main.webp");
    background-size: cover;
    background-position: center 0;
  }

  #gradient {
    opacity: 50%;
    background: linear-gradient(90deg, rgba(255,255,255,0) 0%, rgba(80,80,80,1) 100%);
  }

</style>