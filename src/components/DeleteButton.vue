<template>
  <div>
    <button @click="showing = true">
      <slot />
    </button>

    <md-dialog-confirm
      :md-active.sync="showing"
      md-title="Confirmation"
      md-content="Do you really want to delete?"
      md-confirm-text="Yes"
      md-cancel-text="Cancel"
      @md-cancel="onCancel"
      @md-confirm="onConfirm"
    />
  </div>
</template>
<script>
export default {
  name: 'DeleteButton',
  data() {
    return {
      showing: false,
    };
  },
  props: {},
};
</script>

<style scoped></style>
