<template>
  <div>
    <Dialog :header="header" :visible.sync="show" :modal="true" :closable="true" @hide="doit">
      <slot />
    </Dialog>
  </div>
</template>

<script>
export default {
  props: {
    show: Boolean,
    header: String,
  },
  methods: {
    doit: function () {
      let currentShow = this.show;
      this.$emit("showModel", currentShow)
    },
  },
  data() {
    return {
    };
  },
};
</script>
