<template>
<ul>
<li v-for="item in error" v-bind:key="item"> {{item}} is invalid </li>
</ul>
<input type="text" v-model="Data" />
<h1>{{Data}}</h1>
<input type="text" placeholder="email" />
<br /><br />
<input type="password" placeholder="password" />
<br /><br />
<select v-model="form.country">
    <option>ETH</option>
    <option>america</option>
</select>
<br /> <br />
<p> Gender </p>
<label>male</label>
<input type="radio" name="gender" value="male" v-model="form.gender" />
<label for="female">female</label>
<input type="radio" name="gender" value="female" v-model="form.gender" />
<br /><br />
<h3>Profesion</h3>
<label for="java"> java </label>
<label for="php"> php </label>
<input type="checkbox" value="java" v-model="technology" id="java" />
<input type="checkbox" value="php" v-model="technology" id="php" />
<br /><br />
<label for="student">student</label>
<input type="radio" value="student" id="student" v-model="profesion" name="profesion" />
<label for="developer">developer</label>
<input type="radio" value="developer" id="developer" v-model="profesion" name="profesion" />
<h2>Technolgy : {{technology}}</h2>
<h4>i am {{profesion}}</h4>
<br /><br />
<button v-on:click=login() type="button"> login </button>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            form: {
                email: "",
                password: "",
                gender: "",
                country: ""
            },
            Data: 200,
            technology: [],
            profesion: null,
            error: []
        }
    },
    methods: {
        login() {
            console.warn(this.form)
            for (const item in this.form) {
                if (this.form[item] === "" || this.form[item].length === 0) {
                    this.error.push(item)

                }
                if (this.error.length === 0) {
                    alert("data has been submitted")
                }
                console.warn(this.error)
            }
        }
    }

}
</script>

<style scoped>
h1 {
    color: orange
}
</style>
