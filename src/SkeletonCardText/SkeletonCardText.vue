<template>
<v-card-title primary-title>
    <div :style="{borderRadius: radius + 'px'}" class="skeleton-card-text-title grey darken-2 mb-1">
    </div>
    <div :style="{borderRadius: radius + 'px'}" :key="line" v-for="line in lines" class='skeleton-card-text mt-1 grey lighten-1'>
    </div>
</v-card-title>
</template>

<script>
export default {
    name: "",
    props: {
        'lines': {
            default: 2
        },
        'round':{
            type: Boolean
        }
    },
    computed: {
        radius() {
            if(this.round === true){
                return 15;
            } else {
                return 0;
            }
        }
    },
}
</script>

<style scoped>

.skeleton-card-text-title {
    width: 100%;
    height: 24px;
}

.skeleton-card-text {
    width: 100%;
    height: 16px;
}
</style>