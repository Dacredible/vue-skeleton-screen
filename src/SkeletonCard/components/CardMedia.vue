<template>
    <div class="skeleton-card__media" :class="{ loading: isLoading }"></div>
</template>

<script>
export default {
    name: 'CardMedia',
    props: {
        isLoading: {
            type: Boolean,
        }
    }
};
</script>

<style>
.skeleton-card__media {
    height: 150px;
    width: 150px;
    background-color: grey;

}
</style>
