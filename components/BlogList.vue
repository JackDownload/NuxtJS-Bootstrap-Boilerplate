<template>
    

<div>
<b-col v-for="article of articles" :key="article.slug" class="col-sm-3">
              <NuxtLink
                :to="{ name: 'blog-slug', params: { slug: article.slug } }"
              >  
<div class="fond"> <span class="s1">blog</span><span class="s2">card</span></div>
<div class="card">
  <div class="thumbnail"><img class="left" <img                         :src="article.thumbnail"
                        left
                        blank-color="#d0b8ac"
                        loading="lazy"
                        alt="" /></div>
  <div class="right">
    <h1>{{ article.title }}</h1>
      <h2>{{ article.main_ingredient }}</h2>
    </div>
    <div class="separator"></div>
    <p>{{ article.description }}</p>
  </div>
  <h5>{{ article.time }}</h5>
  <ul>
    <li><i class="fa fa-eye fa-2x"></i></li>
    <li><i class="fa fa-heart-o fa-2x"></i></li>
    <li><i class="fa fa-envelope-o fa-2x"></i></li>
    <li><i class="fa fa-share-alt fa-2x"></i></li>
  </ul>
  <div class="fab"><i class="fa fa-arrow-down fa-3x"></i></div>

 </NuxtLink>
</b-col>
</div>
</template>
<script>
export default {
    components: { },
    
}
</script>

<style lang="scss" scoped>
@import "https://fonts.googleapis.com/css?family=Roboto";
/*Just the background stuff*/
/*My hum... body.. yeah..*/
/* The card */
/* Image on the left side */
/*object-fit: cover;*/
/*object-position: center;*/
/* Right side of the card */
/* DATE of release*/
/* Those futur buttons */
/* Floating action button */
span.s1 {
	position: absolute;
	top: 0;
	font-size: 15rem;
	font-weight: 800;
	text-transform: uppercase;
	color: #3C4447;
}
span.s2 {
	font-weight: 800;
	position: absolute;
	bottom: 0;
	right: 0;
	font-size: 15rem;
	text-transform: uppercase;
	color: #3C4447;
}
body {
	background-color: #353B3F;
	font-family: "Roboto", sans-serif;
}
.card {
	position: relative;
	height: 450px;
	width: 900px;
	margin: 200px auto;
	background-color: #FFF;
	-webkit-box-shadow: 10px 10px 93px 0px rgba(0, 0, 0, 0.75);
	-moz-box-shadow: 10px 10px 93px 0px rgba(0, 0, 0, 0.75);
	box-shadow: 10px 10px 93px 0px rgba(0, 0, 0, 0.75);
}
.thumbnail {
	float: left;
	position: relative;
	left: 30px;
	top: -30px;
	height: 320px;
	width: 530px;
	-webkit-box-shadow: 10px 10px 60px 0px rgba(0, 0, 0, 0.75);
	-moz-box-shadow: 10px 10px 60px 0px rgba(0, 0, 0, 0.75);
	box-shadow: 10px 10px 60px 0px rgba(0, 0, 0, 0.75);
	overflow: hidden;
}
img.left {
	position: absolute;
	left: 50%;
	top: 50%;
	height: auto;
	width: 100%;
	-webkit-transform: translate(-50%, -50%);
	-ms-transform: translate(-50%, -50%);
	transform: translate(-50%, -50%);
}
.right {
	margin-left: 590px;
	margin-right: 20px;
}
h1 {
	padding-top: 15px;
	font-size: 1.3rem;
	color: #4B4B4B;
}
.author {
	background-color: #9ECAFF;
	height: 30px;
	width: 110px;
	border-radius: 20px;
	>img {
		padding-top: 5px;
		margin-left: 10px;
		float: left;
		height: 20px;
		width: 20px;
		border-radius: 50%;
	}
}
h2 {
	padding-top: 8px;
	margin-right: 6px;
	text-align: right;
	font-size: 0.8rem;
}
.separator {
	margin-top: 10px;
	border: 1px solid #C3C3C3;
}
p {
	text-align: justify;
	padding-top: 10px;
	font-size: 0.95rem;
	line-height: 150%;
	color: #4B4B4B;
}
h5 {
	position: absolute;
	left: 30px;
    	bottom: -120px;
	font-size: 6rem;
	color: #C3C3C3;
}
h6 {
	position: absolute;
	left: 30px;
	bottom: -55px;
	font-size: 2rem;
	color: #C3C3C3;
}
ul {
	margin-left: 250px;
}
li {
	display: inline;
	list-style: none;
	padding-right: 40px;
	color: #7B7B7B;
}
.fab {
	position: absolute;
	right: 50px;
	bottom: -40px;
	box-sizing: border-box;
	padding-top: 18px;
	background-color: #1875D0;
	width: 80px;
	height: 80px;
	color: white;
	text-align: center;
	border-radius: 50%;
	-webkit-box-shadow: 10px 10px 50px 0px rgba(0, 0, 0, 0.75);
	-moz-box-shadow: 10px 10px 50px 0px rgba(0, 0, 0, 0.75);
	box-shadow: 10px 10px 50px 0px rgba(0, 0, 0, 0.75);
}

</style>