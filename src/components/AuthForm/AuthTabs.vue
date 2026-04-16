<script setup>
import { ref } from 'vue'
import Tabs from 'primevue/tabs'
import TabList from 'primevue/tablist'
import Tab from 'primevue/tab'
import TabPanels from 'primevue/tabpanels'
import TabPanel from 'primevue/tabpanel'

const activeTab = ref('signin') // signin | signup | resetPassword
</script>

<template>
  <Tabs v-model:value="activeTab">
    <TabList>
      <Tab value="signin">Регистрация</Tab>
      <Tab value="signup">Авторизация</Tab>
    </TabList>
    <TabPanels>
      <TabPanel value="signin"> Регистрация контент </TabPanel>
      <TabPanel value="signup"> Авторизация контент </TabPanel>
    </TabPanels>
  </Tabs>
</template>
