# Vue 3 + Vite + State management

https://www.youtube.com/watch?v=VMJvXT4H6JM

Alternative option to vuex by implementing a useUser hook as in React

See Users.js

Also note the fallback when loading is not finished yet... wrapped in the Suspense component 

```
    <Suspense>
      <template #default>
        <Users />
      </template>
      <template #fallback>
        <div>Loading some users from https://reqres.in/api/users...</div>
      </template>
    </Suspense>```
