<template>
  <div>
    <BaseModal :show="show" :header="product.name">
      <span class="p-float-label">
        <InputText id="name" type="text" :value="product.name" />
        <label for="name">Product</label>
      </span>
    </BaseModal>
  </div>
</template>

<script>
import BaseModal from "../_modals/BaseModal";

export default {
  props: ["product", "show"],
  components: { BaseModal },
  data() {
    return {};
  },
};
</script>
