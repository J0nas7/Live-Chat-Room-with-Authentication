<template>
  <form @submit.prevent="handleSubmit">
      <input type="text" required placeholder="Displayname" v-model="displayName">
      <input type="email" required placeholder="E-mail" v-model="email">
      <input type="password" required placeholder="********" v-model="password">
      <button>Signup</button>
  </form>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        // refs
        const displayName = ref('')
        const email = ref('')
        const password = ref('')

        const handleSubmit = () => {
            console.log(displayName.value, email.value, password.value)
        }

        return {
            displayName, email, password, handleSubmit
        }
    }
}
</script>

<style>

</style>