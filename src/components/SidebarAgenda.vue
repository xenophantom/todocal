<script setup lang="ts">
import { ref } from 'vue'
import { useItemStore } from '@/stores/ItemStore'
import ItemCard from '@/components/ItemCard.vue'
import SidebarAddItemButton from '@/components/SidebarAddItemButton.vue'
import ItemForm from '@/components/ItemForm.vue'

const store = useItemStore()

const showItemForm = ref(false)
</script>

<template>
  <div class="layout">
    <h2>agenda <span class="material-symbols-rounded"> arrow_forward </span></h2>
    <ItemCard v-for="item in store.Items" :key="item.id" :name="item.name" :status="item.status" />
    <SidebarAddItemButton @click="showItemForm = true" button-text="add item" />

    <Teleport to="body">
      <ItemForm :show="showItemForm" @close="showItemForm = false" />
    </Teleport>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  height: 100%;
  min-width: 350px;
  padding: 0px 16px;
  flex-direction: column;
  align-items: flex-start;
  gap: 24px;
}

h2 {
  font-size: 2rem;
  font-weight: 800;
  color: var(--light);
}

.material-symbols-rounded {
  font-variation-settings:
    'FILL' 0,
    'wght' 800,
    'GRAD' 0,
    'opsz' 24;
}
</style>
