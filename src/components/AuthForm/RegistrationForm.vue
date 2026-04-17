<script setup>
import { ref } from 'vue'
import InputText from 'primevue/inputtext'
import Button from 'primevue/button'

const formData = ref({
  email: '',
  password: '',
  firstname: '',
})
</script>
<template>
  <form>
    <div class="mb-3">
      <InputText
        type="text"
        name="firstname"
        placeholder="Введите своё имя"
        v-model="formData.firstname"
        class="w-full"
      />
    </div>

    <div class="mb-3">
      <InputText
        type="text"
        name="email"
        placeholder="Введите e-mail"
        v-model="formData.email"
        class="w-full"
      />
    </div>

    <div class="mb-3">
      <InputText
        type="password"
        name="password"
        placeholder="Введите пароль"
        v-model="formData.password"
        class="w-full"
      />
    </div>

    <div class="grid grid-cols-2 gap-2">
      <Button label="Регистрация" severity="success" />
      <Button label="GitHub" severity="contrast" icon="pi pi-github" />
    </div>
  </form>
</template>
