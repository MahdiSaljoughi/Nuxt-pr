<template>
  <div>
    <input type="email" v-model="email" placeholder="1" /><input
      type="password"
      v-model="password" placeholder="2"
    />
    <input type="submit" @click="addUser" />
  </div>
</template>

<script>
export default {
  data() {
    return {
        email: "",
        password: "",
    }
  },
  methods: {
    addUser() {
      console.log("function called", this.email, this.password);
    },
  },
};
</script>
