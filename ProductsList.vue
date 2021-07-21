<template>
  ...
   <Column field="id" headerStyle="width: 5%">
     <template #body="slotProps">
        <ProductForm :product="slotProps.data" :show="showModal(slotProps.data.id)" />
           <a href="#" @click.stop="toggleModal(slotProps.data.id)">
              <span class="pi pi-external-link"> </span>
           </a>
     </template>
   </Column>
  ...
</template>

<script>
import ProductForm from "./forms/ProductForm";

export default {
  data() {
     return {
       activeModal: 0,
     }
   },
  components: { ProductForm },
  methods: {
    toggleModal: function (id) {
      if (this.activeModal !== 0) {
        this.activeModal = 0;
        return false;
      }
      this.activeModal = id;
    },
    showModal: function (id) {
      return this.activeModal === id;
    },
  },
</script>
