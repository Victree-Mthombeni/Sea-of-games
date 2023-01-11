
<template>
  <div class = main-container>

    <div class = "side-bar">

      <h3>Filter result</h3>

      <form>
      <div class = "container-item"> 
      <label>Name [contain] </label>
      <input type="text" placeholder="Text String">
      </div>

      <div class = "container-item"> 
      <label>Minimum Score </label>
      <input type="text" placeholder="1-10">
      </div>

      <div class = "container-item"> 
      <label>Order by</label>
      <select v-model="currentOrder">
            <option value="name">Release Date</option>
            <option value="value">Score</option>
            <option value="value">Name</option>
        </select>
      </div>

      <div class = "container-item"> 
      <input class="clear" type="reset" value="Clear">
      </div>
    </form>
    </div>
  
  <div class = "card">
    <div v-for="game in games" :key="game.id" class="row">    
      <div class="column two">
      <h3>{{ game.name }} </h3>
        <p>Release Date: {{ game.first_release_date }} </p>
        <p>{{ game.summary }} </p> 
      </div>
</div>
</div>
</div>


</template>



<script>

export default{
  data()
  {
    return {
      games: []
    }
  },
  async mounted()
  {
    fetch('https://public.connectnow.org.uk/applicant-test/')
     .then(res => res.json())
     .then(data => this.games = data)
     .catch(err => console.log(err.message))
  },
  methods: {
        toggleOrder(name) {
            this.currentOrder = name;
        },
        orderedItems(items) {
            return items.filter(item => {
                if (item[this.currentOrder]) return item;
            });     
        },
        format_date(value){
         if (value) {
           return moment(String(value)).format('DD/MM/YYYY')
          }
        }
      

    }
}


</script>


<style scoped>
p{
  font-size: 12px;
}
.row{
  padding: 20px;
  margin: 20px;
  background-color: #03080f;
}
.clear{
  float: right;
  padding: 5px 20px;
  margin: 0px 15px;
  color: white;
  outline: none;

}

.side-bar{
  background-color: #03080f;
  margin: 10px;
  padding: 10px;
  max-height: 450px;

}
.main-container {
    display: grid;
    grid-template-columns: 3fr 8fr;
    padding: 0 2rem;
  }

  .column .one {
  width: 10px;
  float: left;
}

.column .two {
  margin-left: 60px;
}

  .clear{
    float: right
  }

  .container-item{
    padding: 20px;
  }
</style>
