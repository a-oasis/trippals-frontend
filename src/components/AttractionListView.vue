<script setup>
import AttractionCard from '@/components/AttractionCard.vue'

let { attractionList } = defineProps({ attractionList: Object })
let emits = defineEmits(["moveMarker"])

const moveMarker = (obj) => {
  emits("moveMarker", obj.latitude, obj.longitude)
}
</script>

<template>
  <AttractionCard v-for="(attraction, index) in attractionList" :key="index" :attraction="attraction" @click="moveMarker(attraction)" />

</template>

<style scoped>

</style>