<template>
  <cats-rock />
</template>

<style lang="scss">
body {
  height: 100vh;
  background-image: url("@/assets/back.jpeg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  margin: 0;
}
</style>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import CatsRock from "@/components/CatsRock.vue";

@Options({
  components: {
    "cats-rock": CatsRock,
  },
})
export default class RockView extends Vue {}
</script>
