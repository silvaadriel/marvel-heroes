<template lang="pug">
  v-card
    v-card-text
      div.o-container
        the-title-text(:title="$t('app.name')")
        div.o-flex-container
          p.c-info {{ $t('info.application') }}
          the-button(
            :text="$t('button.go_to_grid')"
            route-name="heroes"
          )
</template>

<script>
import TheButton from '@/components/TheButton.vue';
import TheTitleText from '@/components/TheTitleText.vue';

export default {
  name: 'Home',
  components: {
    TheButton,
    TheTitleText,
  },
};
</script>

<style lang="sass" scoped>
  .o-container
    display: flex

    &:first-child
      flex-direction: column

    .o-flex-container
      display: flex
      justify-content: center
      align-items: center
      flex-direction: column

      .c-info
        text-align: center
        width: 400px
        font-size: 20px
        margin-top: 50px
        color: $color-red
</style>
