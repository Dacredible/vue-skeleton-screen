<template>
    <div class="skeleton-card__content">
        <div class="skeleton-card__row">
            <div class="skeleton-card__column grow-column">
                <CardText :round="round" :lines="lines" :isLoading="isLoading"></CardText>
            </div>
            <div class="skeleton-card__column">
                <CardMedia v-if="media" :isLoading="isLoading"></CardMedia>
            </div>
        </div>
    </div>
</template>

<script>
import CardText from './CardText.vue';
import CardMedia from './CardMedia.vue';

export default {
    name: 'CardContent',
    components: {
        CardText,
        CardMedia
    },
    props: {
        isLoading: {
            type: Boolean
        },
        round: {
            type: Boolean
        },
        lines: {
            type: Number
        },
        media: {
            type: Boolean
        }
    },
    mounted() {
        // console.log(this.lines);
    }
};
</script>

<style>
.skeleton-card__content {
    position: relative;
    padding: 0 16px;
    width: 100%;
    height: auto;
}
</style>
