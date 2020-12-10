<template>
  <div>
    <h1>Truck JWT login Button Demo</h1>
    <p>Clicking button to login with the JWT token:</p>
    <p><code>{{jwt}}</code></p>
    <a :href="loginLink" class="btn">Login</a>
  </div>
</template>

<script>
export default {
  name: 'JWT',
  data () {
    const search = new URLSearchParams(window.location.search)
    return {
      jwt: search.get('jwt')
    }
  },
  computed: {
    loginLink() {
      return 'http://44.227.72.76/admin/jwt.php?token=' + this.jwt
    }
  }
}
</script>
<style scoped>
a.btn {
  display: inline-block;
  font-size: 1.2rem;
  color: #fff;
  margin-top: 10px;
  cursor: pointer;
  background-color: #3eaf7c;
  padding: .8rem 1.6rem;
  border-radius: 4px;
  transition: background-color .1s ease;
  box-sizing: border-box;
  text-decoration: none;
  border-bottom: 1px solid #389d70;
}
a.btn:hover {
  background-color: #4abf8a;
}
code {
  background: #f1f1f1;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 10px;
}
</style>
