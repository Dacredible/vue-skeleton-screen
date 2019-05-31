<template>
  <div class="skeleton-card__actions">
    <div class="skeleton-card__btn" :class="{ loading: isLoading}"></div>
    <div class="skeleton-card__btn" :class="{ loading: isLoading}"></div>
  </div>
</template>

<script>
export default {
    name: 'CardActions',
    props: {
        isLoading: {
            type: Boolean,
        }
    }
};
</script>

<style>
.skeleton-card__actions {
    display: flex;
    padding: 8px 16px;
}

.skeleton-card__btn {
  background-color: #e5e5e5;
  width: 90px;
  height: 36px;
  margin: 0 4px;
}
</style>
