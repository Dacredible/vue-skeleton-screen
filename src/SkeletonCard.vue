<template>
<v-card class="px-2 mx-5" :hover="hover">
    <skeleton-card-header v-if="header" :round="round" />
    <v-container v-if="horizontal">
        <v-layout row align-center>
            <v-flex class="flex--grow">
                <skeleton-card-text :round="round" :lines="lines" />
            </v-flex>
            <v-flex>
                <skeleton-card-media height="150px" width="150px" v-if="media" />             
            </v-flex>
        </v-layout>
    </v-container>
    <v-layout column v-else>
        <v-flex class="px-3">
            <skeleton-card-media v-if="media" />           
        </v-flex>
        <v-flex>
            <skeleton-card-text :lines="lines" v-if="text" :round="round" /> 
        </v-flex>
    </v-layout>
    <skeleton-card-actions v-if="actions" />
</v-card>
</template>

<script>
import SkeletonCardHeader from "./SkeletonCardHeader/SkeletonCardHeader.vue";
import SkeletonCardMedia from "./SkeletonCardMedia/SkeletonCardMedia.vue";
import SkeletonCardText from "./SkeletonCardText/SkeletonCardText.vue";
import SkeletonCardActions from "./SkeletonCardActions/SkeletonCardActions.vue";

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
    SkeletonCardMedia,
    SkeletonCardText,
    SkeletonCardActions
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
