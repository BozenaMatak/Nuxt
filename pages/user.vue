<template>
  <div class="all-users">
    <div class="row ">
      <div class="card" v-for="user in users" :key="user.id">
        <NuxtLink class="link" :to="`/${user.id}`">
          <div>
            <img class="picture" :src="user.picture">
          </div>
          <div class="name">
            {{user.firstName}}
            {{user.lastName}}
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
  
<script>
  export default {
    data() {
      return {
        users: []
      }
    },
    async created(){
      this.users = await fetch(
        'https://dummyapi.io/data/v1/user?page=0&limit=50', {
          headers: { 
            'app-id' : '634dbb85eb3e526af6093a40'                
          }
        })
        .then(res => res.json())
        this.users = this.users.data
        console.log(this.users)
     
      let users2 = await fetch(
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
    },   
  };
</script>

<style scoped>

.all-users{
  font-family: 'Titillium Web', sans-serif;
  background-color: cadetblue;
}
.link{
  text-decoration: none
}
.row{
  padding-top: 1.5%;
  padding-bottom: 1.5%;
  background-color: burlywood;
  width: 70%;
  margin-left: 15%;
  margin-right: 15%;
  text-align: center;
  box-shadow: 0 2px 32px 0 rgb(0 0 0 / 70%);
}
.card{
  padding-top: 2.5%;
  padding-bottom: 2.5%;
  margin: 2.5% 6.66% 2.5% 6.66%;
  width:20%;
  box-shadow: 0 2px 32px 0 rgba(0, 0, 0, 0.4);
}
.name{
  color: black;
  font-size: 17px;
}
.picture{
  width: 80%;
  margin-bottom: 5%;
}

@media (max-width: 800px) and (max-width: 650px){
  .row{
    width: 80%;
    margin-right: 10%;
    margin-left: 10%;
  }
  .card{
    width: 25%;
    margin-left: 4.1%;
    margin-right: 4.1%;
  }
  .name{
    font-size: 15px;
  }
}

@media(max-width: 400px) and (max-width: 550px){

  .row{
    width: 90%;
    margin-left: 5%;
    margin-right: 5%;
  }
  .name{
    font-size: 13px;
  }

}
@media(max-width: 350px){
  .row{
    margin: 0;
    width: 100%;
  }
}


</style>