<template>
  <div
    class="card card-background card-background-mask-dark align-items-start mt-4"
  >
    <div
      class="full-background cursor-pointer"
      :style="{
        backgroundImage: `url(${bgImg})`,
      }"
    />
    <div class="card-body">
      <h5 class="text-white mb-0">
        {{ title }}
      </h5>
      <p class="text-white text-sm">
        {{ desc }}
      </p>
      <div class="d-flex mt-4 pt-2">
        <vsud-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mb-0"
          type="button"
        >
          <i
            class="fas p-2"
            :class="$store.state.isRTL ? 'fa-forward' : 'fa-backward'"
          />
        </vsud-button>
        <vsud-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mx-2 mb-0"
          type="button"
        >
          <i class="fas fa-play p-2" />
        </vsud-button>
        <vsud-button
          color="white"
          variant="outline"
          class="rounded-circle p-2 mb-0"
          type="button"
        >
          <i
            class="fas fa-forward p-2"
            :class="$store.state.isRTL ? 'fa-backward' : 'fa-forward'"
          />
        </vsud-button>
      </div>
    </div>
  </div>
</template>

<script>
import VsudButton from "@/components/VsudButton.vue";
import bgImg from "@/assets/img/curved-images/curved1.jpg";
export default {
  name: "MusicPlayer",
  components: {
    VsudButton,
  },
  props: {
    title: {
      type: String,
      default: "Some Kind Of Blues",
    },
    desc: {
      type: String,
      default: "Deftones",
    },
  },
  data() {
    return {
      bgImg,
    };
  },
};
</script>
