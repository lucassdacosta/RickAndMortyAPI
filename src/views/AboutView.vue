<template>
  <div class="about">
    <div class="main">
      <div class="img">
        <img src="../../public/Eu.jpeg" alt="">
      </div>
      <div class="aboutMe">
        <h3 class="name"><span>Nome:</span> Lucas Simões da Costa</h3>
        <p><span>RA:</span> 1973724</p>
      </div>
    </div>
  </div>
</template>

<style>
.about{
  background-color: grey;

  height: 80vh;

  display: flex;
  justify-content: center;
  align-items: center;
}

.main{
  padding-right: 8px;
  color: white;
  
  border-radius: 22px 0 0 22px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

  display: flex;
  justify-content: center;
  align-items: center;
  gap: 40px;

}

.img img{
  border-radius: 10%;
  width: 200px;
}


</style>
