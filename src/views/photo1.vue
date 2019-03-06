<template>
    <div class="photo1">
    <album1/>
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import album1    from '@/components/album1.vue'; // @ is an alias to /src

@Component({
  components: {
    album1,
  },
})
export default class photo1 extends Vue {}
</script>

<style>

</style>
