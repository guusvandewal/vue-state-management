<template>
  <div v-if="error">{{ error }}</div>
  <div v-else-if="users">
    <h2>Loaded the following users IDs</h2>
    <ul>
      <li v-for="user in users.data" :key="user.id">
        <code>{{ user.id }} {{ user.first_name }}</code>
      </li>
    </ul>
  </div>
</template>

<script>
import useUsers from '../modules/users';

export default {
  name: 'Users',

  setup() {
    const { users, error } = useUsers();

    return { users, error };
  },
};
</script>

<style scoped>
ul {
  display: inline-block;
  text-align: center;
  list-style: none;
}
li {
  text-align: left;
}
</style>
