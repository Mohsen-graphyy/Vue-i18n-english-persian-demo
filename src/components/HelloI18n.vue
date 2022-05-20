<template>
  <h1>{{ $t("title") }}</h1>
  <p :class="{'rtl' : $i18n.locale == 'fa'}">{{ $t("description") }}</p>
  <LocaleSwitcher />
</template>

<script>
import { defineComponent } from 'vue'
import LocaleSwitcher from "./LocaleSwitcher.vue";
export default defineComponent({
  name: 'HelloI18n',
  components: { LocaleSwitcher }
})
</script>

<i18n>
{
  "en": {
    "hello": "Hello i18n in SFC!"
  }
}
</i18n>
<style scoped>
  .rtl {
    direction: rtl;
    font-size: 2rem;
    
  }
</style>