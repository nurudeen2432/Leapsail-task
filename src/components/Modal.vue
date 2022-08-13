<template>
<main>
<div class="container">
    
    <div class="left">
        <h1 style="font-weight:bold;">We are revolutionalizing your concept of comfort</h1>
        <h4 style="font-size:20px">Created with a can do an achievers mindset. A self-onboarding application with features that open you to a new way</h4>
        <button class="bot">Get Started</button>
    </div>
<div class="right">
    <img src="@/assets/pexel1.png" alt="" class='img1'>
    <img src="@/assets/pexel2.png" alt="" class="img2">
    <img src="@/assets/pexel3.png" alt="" class="img3">
</div>
</div>
<section>
<div class="work">
    <h2>Work in the way that works for you</h2>
    <p style='font-size:20px;'>What would you like to manage with Leapsail.com? </p>
    <label class='switch'>
        <input type="checkbox">
        <span class="slider"></span>
    </label>
    <label class='switch'>
        <input type="checkbox">
        <span class="slider"></span>
    </label>
    <label class='switch'>
        <input type="checkbox" checked >
        <span class="slider"></span>
    </label>
    <label class='switch'>
        <input type="checkbox" checked>
        <span class="slider"></span>
    </label>
    <button class="bot2">Get Started</button>
</div>
</section>
<div class="container-2">
    <div >
        <img src="@/assets/Frame2.png" alt="" style="width:400px;" class="image">
    </div>
    <div class="text">
        <h1>Investment</h1>

        <h3>Reap enticing investment rewards! Be confident in your investment because of the security we provide for you</h3>

        <h3 style="color:#f6b736; cursor:pointer;">Learn More</h3>
    </div>
</div>
<div class="container-3">
    <div class="text-1">
        <h1>Pay Small Small</h1>
        <h3>No matter how solid your plans are, sometimes you don't have all the money </h3>

        <h5 style="color:#f6b736; cursor:pointer " >Learn More</h5>
    </div>
    <div >
        <img src="@/assets/Frame.png" alt="" class="image-1">
    </div>
</div>

<div class="why">
    <h4 style="font-weight:bold;">Why Leapsail</h4>
    <h1 style="
        font-size:50px;
        color:grey;
        font-weight:bolder;
        font-family:Time new roman;
    ">Excellent Customer relations? &nbsp; <b style="color:#f6b736;"> Of Course !</b></h1>
    
</div>
</main>
</template>

<script>
export default {
    
    props : [],
    methods:{
    
    }
}
</script>


<style>
.left{
    margin: 200px 50px;
    padding:5px;
}

.container{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-columns: auto minmax( 327px, auto-fit)
}
@media screen and (max-width:400px){
    .container{
        display: block;
    }
   
   
    .img1, .img2, .img3{
        width: 100px;
    }
}
@media screen and (max-width:360px){
    body{
        overflow-x: hidden;
    }
    .bot2{
       padding-left: 30px;
    }
}
.right{
    margin: 30px;
}

.img1{
   
    width:300px;
    top:30px;
    
}

.img3{
    width: 300px;
}
.bot{
  margin-left: 5px;
  background: #f6b736;
  border: 1px solid #f6b736;
  color: white;
  border-radius: 20px;
  height: 40px;
  width: 150px;
font-size: 16px;
}
.bot:hover{
  background: #fff;
  color: #333;
  transition: .1s all ease-in-out;
}
.work{
    text-align: center;
    position:relative;
}
.work h2{
    font-size: 40px;
    font-weight: bold;

}
.switch{
    position: relative;
    display: inline-block;
    width: 110px;
    height: 60px;
    margin: 0 10px;
}
.slider{
    position: absolute;
    cursor:pointer;
    top:0;
    left:0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    transition: .4s;
    border-radius:34px;
}

.switch input{
    display: none;
}
 .slider:before{
    position: absolute;   
    content:"";
    height: 50px;
    width: 50px;
    left:5px;
    bottom: 5px;
    background-color: white;
    transition: 0.4s;
    border-radius: 50px;

}
input:checked + .slider{
    background-color: #f6b736;
    
}
input:checked + .slider:before{
    transform: translateX(50px)

}
.bot2{
    position: absolute;
    top:160%;
    left:45%;
    margin-bottom: 30px;
     background: #f6b736;
  border: 1px solid #f6b736;
  color: white;
  border-radius: 20px;
  height: 40px;
  width: 150px;
font-size: 16px;
}
.container-2{
    margin: 200px;
    display: grid;
    grid-template-columns: 1fr 1fr;
}
@media screen and (max-width: 400px) {
    .container-2{
        display: block;
        margin:10px;
    
    }
    .bot2{
        top:100%;
        left:30%;
    }
    .image{
        width: 100px;
    }
}
.text{
    padding-top: 200px;
}
.container-3{
    display: grid;
    grid-template-columns: 1fr 1fr;
    margin: 200px;
}
.text-1{
    padding-top: 180px;
    
}
@media screen and (max-width:400px){
    .container-3{
        display:block;
        margin:10px;
    }
    .image-1{
        width: 300px;
    }
}
.why{
    padding-left: 200px;
}
</style>

