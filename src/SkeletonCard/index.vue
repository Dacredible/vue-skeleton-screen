<template>
    <div class="skeleton-card" :style="{backgroundColor: bgcolor}">
        <CardHeader v-if="header" :round="round" :avatar="avatar" :isLoading="isLoading"></CardHeader>
        <CardContent :round="round" :lines="lines" :media="media" :isLoading="isLoading"></CardContent>
        <CardActions v-if="actions" :isLoading="isLoading"></CardActions>
    </div>

</template>

<script>
import CardHeader from './components/CardHeader.vue';
import CardContent from './components/CardContent.vue';
import CardActions from './components/CardActions.vue';

export default {
    name: 'SkeletonCard',
    props: {
        isLoading: {
            type: Boolean,
            default: false
        },
        header: {
            type: Boolean,
            default: true
        },
        avatar: {
            type: Boolean,
            default: true
        },
        media: {
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
    },
    components: {
        CardHeader,
        CardContent,
        CardActions
    },
    computed: {
        bgcolor() {
            if (this.dark) {
                return '#424242';
            }
            return 'white';
        }
    },
    mounted() {
        // console.log(this.lines);
    }
};
</script>

<style>
/* reset box-sizing just for this component in case the user use different box model */
.skeleton-card {
 box-sizing: border-box;
}
*, *:before, *:after {
 box-sizing: inherit;
}

.skeleton-card {
    position: relative;
    display: block;
    width: auto;
    height: auto;
    margin: 8px 48px;
    padding: 0 8px 8px;
    border-radius: 2px;
    box-shadow: 0 2px 1px -1px rgba(0,0,0,.2), 0 1px 1px 0 rgba(0,0,0,.14), 0 1px 3px 0 rgba(0,0,0,.12);
    text-decoration: none;
    cursor: default;
}

.loading {
    position: relative;
    overflow: hidden;
}

.loading::after {
    display: block;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    transform: translateX(-100%);
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, .2), transparent);
    animation: loading 1.5s infinite;
}

@keyframes loading {
    100% {
        transform: translateX(100%);
    }
}
</style>

