<template>
  <div class="layout-container">
    <ParentLayout>
      <template #page-top>
        <div v-if="show" class="page-top">
          <div class="version-alert">
            <p v-if="isNext">This page covers a next version of Handsontable, and is not published yet.</p>
            <p v-else-if="!isLatest">This page covers a non-latest version of Handsontable.</p>
          </div>
        </div>
      </template>
    </ParentLayout>
  </div>
</template>

<script>
import ParentLayout from '@parent-theme/layouts/Layout.vue';
import NavLinks from '@theme/components/NavLinks.vue';
import NavLink from '@theme/components/NavLink.vue';
import Sidebar from '@theme/components/Sidebar.vue';

export default {
  name: 'Layout',
  components: {
    ParentLayout,
    NavLinks,
    NavLink,
    Sidebar
  },
  computed: {
    isLatest() {
      return this.$page.currentVersion === this.$page.latestVersion;
    },

    isNext() {
      return this.$page.currentVersion === 'next';
    },

    show() {
      return this.$page.latestVersion && !this.isLatest || this.isNext;
    }
  }
};
</script>

<style lang="stylus">
.layout-container
  min-height 100%

.version-alert
  margin-top 2rem
  padding 1rem 1.2rem
  border-radius 6px
  color #fff
  border 1px solid #e9eef2
  background #2456f2
  p
    margin 0
    padding 0
    font-weight 500
    line-height 1.5
</style>
