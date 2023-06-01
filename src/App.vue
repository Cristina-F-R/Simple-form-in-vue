
<template>
<h1> Simple From</h1>
<p>{{form}} </p>
  <form>

    <label>Email: </label>
    <input type="text" placeholder=" enter email" v-model="form.email" />
    <br/>
    <br/>
    <label>Password: </label>
    <input type="password" placeholder=" enter password" v-model="form.password"/>
    <br/>
    <br/>
    <select v-model='form.country'>
      <option> Spain </option>
      <option> France </option>
      <option> Italy </option>
    </select>
    <br/>
    <br/>
    <h3> Gender </h3>
    <label>Male: </label>
    <input type="radio" name="gender" value="male" v-model="form.gender" />
    <br/>
    <label>Femle: </label>
    <input type="radio" name="gender" value="female" v-model="form.gender" />
    <br/>
    <br/>
    <h3> Technology </h3>
    <label>React: </label>
    <input type="checkbox" value="java" v-model="form.technology" />
    <br/>
    <label>.Net: </label>
    <input type="checkbox" value=".net" v-model="form.technology" />
    <br/>
    <br/>


    <button type="button" v-on:click="login"> Login </button>
  </form>

</template>

<script>
export default {
  name: "Home",
  data () {
    return {
      form: {
        email: '', 
        password: '',
        country: '',
        gender: '', 
        technology:[]
      },
    }
  },
  methods:{
    login (){

      console.warn(this.form)
      }
  }
}

</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
