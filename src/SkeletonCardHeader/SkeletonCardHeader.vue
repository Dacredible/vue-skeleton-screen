<template>
<v-card-text>
    <v-layout row align-center>
        <v-flex>
            <div class='skeleton-card-avatar'>
            </div>
        </v-flex>
        <v-flex class="flex--grow">
            <v-layout column>
                <div :style="{borderRadius: radius + 'px'}" class="skeleton-card-title grey">
                </div>
                <div :style="{borderRadius: radius + 'px'}" class="skeleton-card-subtitle grey lighten-1 mt-1">
                </div>
            </v-layout>
        </v-flex>
    </v-layout>
</v-card-text>
</template>

<script>
export default {
    name: "",
    components: {

    },
    props: {
        'round': {
            type: Boolean
        }
    },
    computed: {
        radius() {
            if(this.round === true){
                return 10;
            } else {
                return 0;
            }
        }
    },
    data: function() {
        return {}
    },
    methods: {}
}
</script>

<style scoped>
.skeleton-card-avatar {
    border-radius: 50%;
    height: 50px;
    width: 50px;
    background-color: grey;
}

.skeleton-card-subtitle {
    width: 70%;
    height: 12px;
}

.skeleton-card-title {
    width: 100%;
    height: 14px; 
}
</style>