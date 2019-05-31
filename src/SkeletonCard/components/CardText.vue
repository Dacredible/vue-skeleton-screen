<template>
    <div class="skeleton-card__text-container">
        <div :style="{borderRadius: radius + 'px'}" class="skeleton-card__text-title" :class="{ loading: isLoading}">
        </div>
        <div :style="{borderRadius: radius + 'px'}" :key="line" v-for="line in lines" class='skeleton-card__text' :class="{ loading: isLoading}">
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardText',
    props: {
        isLoading: {
            type: Boolean,
        },
        lines: {
            type: Number
        },
        round: {
            type: Boolean
        },
    },
    computed: {
        radius() {
            if (this.round === true) {
                return 15;
            }
            return 0;
        }
    }
};
</script>

<style>
.skeleton-card__text-container {
    padding-right: 24px;
}
.skeleton-card__text-title {
    width: 100%;
    height: 24px;
    background-color: #616161!important;
    border-color: #616161!important;
    margin-bottom: 8px;
}

.skeleton-card__text {
    width: 100%;
    height: 16px;
    background-color: #bdbdbd!important;
    border-color: #bdbdbd!important;
    margin-top: 4px;
}
</style>
