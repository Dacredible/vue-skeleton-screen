<template>
    <div>
        <v-layout v-if="horizontal" row align-center>
        <v-flex class="flex--grow">
            <skeleton-card-text :round="round" :lines="lines" />
        </v-flex>
        <v-flex>
            <skeleton-card-media height="150px" width="150px" v-if="media" />             
        </v-flex>
    </v-layout>
    <v-layout column v-else>
        <v-flex class="px-3">
            <skeleton-card-media v-if="media" />           
        </v-flex>
        <v-flex>
            <skeleton-card-text :lines="lines" v-if="text" :round="round" /> 
        </v-flex>
    </v-layout>
    </div>
</template>

<script>
import SkeletonCardMedia from "../SkeletonCardMedia/SkeletonCardMedia.vue";
import SkeletonCardText from "../SkeletonCardText/SkeletonCardText.vue";

export default {
    name:"",
    props: ["horizontal", "round", "media", "lines"],
    components: {
        SkeletonCardMedia,
        SkeletonCardText
    }
}
</script>

<style scoped>

</style>
