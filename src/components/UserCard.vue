<template>
  <div class="user-card">
    <h3>User Card</h3>
    <p>Name: {{ name }}</p>
    <p>Email: {{ email }}</p>
    <p>Role: {{ role }}</p>
    <slot></slot>
    <slot name="extra"></slot>
    <button @click="welcomeUser">Welcome</button>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type:String,
      required: true
    },
    email: {
      type:String,
      required: true
    },
    role:  {
      type:String,
      default: 'user'
    },
  },
  methods: {
    welcomeUser() {
      this.$emit('user-welcome', `Welcome ${this.name}!`);
    }
  }
}
</script>

<style scoped lang="scss">
.user-card {
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 5px;
  margin: 5px 0;
}
</style>