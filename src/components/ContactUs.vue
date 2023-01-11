
<template>
  <div>
   
    <form >

      <h1>GET IN TOUCH</h1>
      <p>Trysoll transom furl Seo Legs Scollywag ajck ketch chandler mizzenmost reef salls skyfall Shiver timbers loarot belying pin Sea Lges boom gunwalls booty jury</p>

      <div className="innerform">
        
      <label><h4>Contact Form</h4></label>
      
      <div className="floatleft">
      <label>Name *</label>
      <input >
      </div>
      
      <div className="floatleft"> 
      <label>Email Address *</label>
      <input>
    </div>
      <label>Message *</label>
      <textarea></textarea>

      <button>send</button>
    </div>
    </form>
  </div>
</template>




<style scoped>

.floatleft{
  display: table-cell;
  margin: 10px 20px;
  padding: 0px 20px 0px 0px;
}

button{
  float: right;
  padding: 5px 20px;
  margin: 0px 15px;
  color: white;
  outline: none;

}

form{
  padding: 10px 32.5% ;
  margin: 20px;
}
.main-container {
    display: grid;
    grid-template-columns: 3fr 8fr;
    padding: 0 2rem;
  }

  .innerform{
    background-color: #081221;
    padding: 10px 20px;
    margin: 50px 0px;
    min-height: 300px;
  }

  input{
    min-width: 30px;
  }

  textarea
  {
    width: 90%;
  }
    

  .clear{
    float: right
  }

  .container-item{
    padding: 20px;
  }
</style>
