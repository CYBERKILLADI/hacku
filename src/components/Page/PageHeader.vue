<template>
  <section class="header">
    <div class="header__left">
      <slot />
    </div>

    <div v-if="$slots.center" class="header__center">
      <slot name="center" />
    </div>

    <div v-if="$slots.right" class="header__right">
      <slot name="right" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.header {
  @apply flex mb-6;

  &::v-deep {
    .title {
      @apply text-lg font-bold text-white mb-1;

      .icon {
        @apply mr-2;
      }
    }

    .subtitle {
      
    }

    .tip {
      @apply ml-2;
    }
  }
}

.header__left {
  @apply flex-1;

  &:not(:last-child) {
    @apply mr-3;
  }
}
</style>
