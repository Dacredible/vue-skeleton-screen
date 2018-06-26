<template>
<v-card v-if="dark" class="px-2 mx-5" :hover="hover" color="grey darken-3">
    <skeleton-card-header v-if="header" :round="round" />
    <skeleton-card-content :horizontal="horizontal" :round="round" :lines="lines" :media="media"/>
    <skeleton-card-actions v-if="actions" />
</v-card>
<v-card v-else class="px-2 mx-5" :hover="hover">
    <skeleton-card-header v-if="header" :round="round" />
    <skeleton-card-content :horizontal="horizontal" :round="round" :lines="lines" :media="media"/>
    <skeleton-card-actions v-if="actions" />
</v-card>
</template>

<script>
import SkeletonCardHeader from "./SkeletonCardHeader/SkeletonCardHeader.vue";
import SkeletonCardActions from "./SkeletonCardActions/SkeletonCardActions.vue";
import SkeletonCardContent from "./SkeletonCardContent/SkeletonCardContent.vue";

export default {
  name: "",
  props: {
    header: {
      type: Boolean,
      default: true
    },
    media: {
      type: Boolean,
      default: true
    },
    text: {
      type: Boolean,
      default: true
    },
    actions: {
      type: Boolean,
      default: false
    },
    horizontal: {
      type: Boolean,
      default: false
    },
    lines: {
      type: Number,
      default: 2
    },
    dark: {
      type: Boolean,
      default: false
    },
    round: {
      type: Boolean,
      default: false
    },
    hover: {
      type: Boolean,
      defalut: false
    }
  },
  components: {
    SkeletonCardHeader,
    SkeletonCardActions,
    SkeletonCardContent
  },
  data: function() {
    return {};
  },
  methods: {}
};
</script>

<style>
.flex--grow {
  flex-grow: 99 !important;
}
</style>
