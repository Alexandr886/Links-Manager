<script setup>
import { ref } from 'vue'
import Tabs from 'primevue/tabs'
import TabList from 'primevue/tablist'
import Tab from 'primevue/tab'
import TabPanels from 'primevue/tabpanels'
import TabPanel from 'primevue/tabpanel'
import LoginForm from './LoginForm.vue'
import RegistrationForm from './RegistrationForm.vue'

const activeTab = ref('signin') // signin | signup | resetPassword
</script>

<template>
  <Tabs v-model:value="activeTab">
    <TabList>
      <Tab value="signin">Авторизация</Tab>
      <Tab value="signup">Регистрация</Tab>
    </TabList>
    <TabPanels>
      <TabPanel value="signin">
        <LoginForm />
      </TabPanel>
      <TabPanel value="signup">
        <RegistrationForm />
      </TabPanel>
    </TabPanels>
  </Tabs>
</template>
