<template>
  <div class="details">
    <div class="user-info row">
      <div class="card ">
        <div>
          <img class="picture" :src="info.picture">
        </div>
        <div class="name">
          {{info.id}}
          <span>{{info.title}}.</span> 
          <span style="font-weight:700">{{info.firstName}} {{info.lastName}}</span>
        </div>
      </div>
    </div>
  </div>   
</template>

<script>
export default {
  data() {
    return {
      users: [],
      info: {},
      id: null
    }
  },
  async created(){
    this.users =await fetch(
      'https://dummyapi.io/data/v1/user?page=0&limit=50', {
        headers: { 
          'app-id' : '634dbb85eb3e526af6093a40'
        }
      })
      .then(res => res.json())
      this.users = this.users.data
      console.log(this.users)
      
    let users2 =await fetch(
      'https://dummyapi.io/data/v1/user?page=1&limit=50', {
        headers: { 
          'app-id' : '634dbb85eb3e526af6093a40'    
        }
      })
      .then(res => res.json())
      users2 = users2.data
      console.log(users2)
      users2.forEach(element => {
        this.users.push(element)
      });
      console.log(this.users) 

      this.id = this.$route.params.id
        
      this.users.forEach(element => {
        if(this.id == element.id){
          this.info = element
        }
      });
  }
}
</script>

<style scoped>
.details{
  font-family: 'Titillium Web', sans-serif;
  margin-top: 5%;
}
.row{
  width: 20%;
  padding-top: 1.5%;
  padding-bottom: 1.5%;
  margin:auto;
  background-color: burlywood;
  text-align: center;
  box-shadow: 0 2px 32px 0 rgb(0 0 0 / 30%);
}
.card{
  width:70%;
  margin: auto;
  padding-top: 2.5%;
  padding-bottom: 2.5%;
}
.name{
  color: black;
  font-size: 16px;
}
.picture{
  width: 70%;
  margin-bottom: 5%;
}
@media (max-width: 1500px){
  .card{
  width:100%;
  margin: auto;
  padding-top: 2.5%;
  
  }
}
@media (max-width: 1200px){
  .row{
    width: 30%; 
  }
}
@media (max-width: 800px){
  .row{
    width: 50%; 
  }
}
@media (max-width: 550px){
  .row{
    width: 80%; 
  }
}
</style>