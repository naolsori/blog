 <template>
 <input type="text" v-model="Data" />
<h1>{{Data}}</h1>
<input type = "text" placeholder="email" />
<br /><br />
<input type = "password" placeholder="password" />
<br /><br/>
<button v-on:click=getData()>login</button>
<br /> <br />
<h3>Profesion</h3>
<label for="java"> java </label>
 <label for="php"> php </label>
<input type="checkbox" value="java" v-model="technology" id="java" />
<input type="checkbox" value="php"  v-model="technology" id="php" />
<br /><br />
<label for="student">student</label>
 <input type="radio" value="student" id="student" v-model="profesion" name="profesion" />
 <label for="developer">developer</label>
 <input type="radio" value="developer" id="developer" v-model="profesion" name="profesion" />
<h2>Technolgy : {{technology}}</h2>
<h4>i am {{profesion}}</h4>

</template>
<script>
export default {
 name: 'Home', 
 data(){
    return{
        Data : 200,
        technology:[],
        profesion: null
    }
 },
 methods:{
     getName(name){
            return name;
        },
        getData(){
            console.warn("hi naol")
        },
        getconsole(){
            console.warn("this event")
        }
        }

    }
    
</script>
<style scoped>h1{
color: orange
}

</style>