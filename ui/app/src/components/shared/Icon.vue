<script lang="ts">
import { defineComponent, PropType } from "vue";
import CircleArrows from "./icons/CircleArrows.vue";
import CircleHalf from "./icons/CircleHalf.vue";
import PoolIcon from "./icons/PoolIcon.vue";
import DownArrow from "./icons/DownArrow.vue";
import Tick from "./icons/Tick.vue";
import Cross from "./icons/Cross.vue";
import Back from "./icons/Back.vue";
import Plus from "./icons/Plus.vue";
import InfoBoxBlack from "./icons/InfoBoxBlack.vue";
import InfoBoxGrey from "./icons/InfoBoxGrey.vue";

export default defineComponent({
  props: {
    icon: {
      type: String as PropType<
        "arrows" | "back" | "circle-half" | "pool" | "plus" | "down" | "tick" | "cross" |
        "info-box-black" | "info-box-grey"
      >,
    },
  },
  components: { Cross, Tick, DownArrow, CircleArrows, CircleHalf, PoolIcon, Back, Plus,
    InfoBoxBlack, InfoBoxGrey},
});
</script>

<template>
  <span>
    <CircleArrows v-if="icon === 'circle-arrows'" />
    <CircleHalf v-if="icon === 'circle-half'" />
    <PoolIcon v-if="icon === 'pool'" />
    <DownArrow v-if="icon === 'down'" />
    <Tick v-if="icon === 'tick'" />
    <Cross v-if="icon === 'cross'" />
    <Back v-if="icon === 'back'" />
    <Plus v-if="icon === 'plus'" />
    <InfoBoxBlack v-if="icon === 'info-box-black'" />
    <InfoBoxGrey v-if="icon === 'info-box-grey'" />
  </span>
</template>
