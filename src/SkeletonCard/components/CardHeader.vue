<template>
    <div class="skeleton-card__header">
        <div class="skeleton-card__row">
            <div v-if="avatar" class="skeleton-card__column">
                <CardAvatar></CardAvatar>
            </div>
            <div class="skeleton-card__column grow-column">
                <div :style="{borderRadius: radius + 'px'}" class="skeleton-card__title" :class="{ loading: isLoading}">
                </div>
                <div :style="{borderRadius: radius + 'px'}" class="skeleton-card__subtitle" :class="{ loading: isLoading}">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CardAvatar from './CardAvatar.vue';

export default {
    name: 'CardHeader',
    components: {
        CardAvatar
    },
    props: {
        isLoading: {
            type: Boolean,
        },
        avatar: {
            type: Boolean,
        },
        round: {
            type: Boolean,
        }
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
.skeleton-card__header {
    position: relative;
    padding: 16px;
    width: 100%;
    height: auto;
}

.skeleton-card__row {
    display: flex;
    -webkit-box-flex: 1;
    flex-wrap: nowrap;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}

.skeleton-card__column {
    display: block;
    width: auto;
    flex: 1 1 auto;
}

.grow-column {
    flex-grow: 99;
}

.skeleton-card__title {
    width: 100%;
    height: 14px;
    background-color: #9e9e9e!important;
    border-color: #9e9e9e!important;
}

.skeleton-card__subtitle {
    width: 70%;
    height: 12px;
    background-color: #bdbdbd!important;
    border-color: #bdbdbd!important;
    margin-top: 4px;
}
</style>
