<template>
  <b-container fluid="xl">
    <page-title />
    <page-section class="mb-1">
      <div class="terminal-container">
        <kvm-console :is-full-window="false" />
      </div>
    </page-section>
    <page-section :section-title="$t('pageKvm.virtualMedia')" class="mb-1 mt-5">
      <virtual-media />
    </page-section>
  </b-container>
</template>

<script>
import PageTitle from '@/components/Global/PageTitle';
import PageSection from '@/components/Global/PageSection';
import KvmConsole from './KvmConsole';
import VirtualMedia from './KvmVirtualMedia.vue';

export default {
  name: 'Kvm',
  components: { PageTitle, KvmConsole, PageSection, VirtualMedia },
};
</script>

<style scoped>
.terminal-container {
  width: 70%;
}
</style>
