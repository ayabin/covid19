<template>
  <span class="link-to-information-about-emergency-measure">
    <external-link
      url="https://www.bousai.metro.tokyo.lg.jp/1007617/index.html"
    >
      <v-icon
        size="2rem"
        class="link-to-information-about-emergency-measure-icon"
      >
        mdi-bullhorn
      </v-icon>
      {{ $t('東京都緊急事態措置について') }}
    </external-link>
  </span>
</template>

<script lang="ts">
import Vue from 'vue'
import ExternalLink from '@/components/ExternalLink.vue'

export default Vue.extend({
  components: { ExternalLink },
})
</script>

<style lang="scss">
.link-to-information-about-emergency-measure {
  background-color: $emergency;
  border: 2px solid $emergency;
  color: $gray-2;
  border-radius: 4px;
  padding: 4px 8px;
  display: inline-flex;
  @include font-size(16);
  &:hover {
    background-color: $white;
    border-radius: 4px;
  }

  .ExternalLink {
    color: $gray-2 !important;
    text-decoration: none;
    margin: -10px;
    padding: 10px;
  }

  > span {
    @include button-text('sm');
  }

  @include lessThan($medium) {
    margin-top: 8px;
  }
}
</style>
