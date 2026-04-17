<script setup>
import { ref } from 'vue'
import InputText from 'primevue/inputtext'
import Button from 'primevue/button'

const formData = ref({
  email: '',
})
</script>

<template>
  <form action="">
    <div class="mb-3">
      <InputText
        type="text"
        name="email"
        placeholder="Введите e-mail"
        v-model="formData.email"
        class="w-full"
      />
    </div>
    <div class="grid">
      <Button label="Сброс пароля" severity="success" />
    </div>
  </form>
</template>
