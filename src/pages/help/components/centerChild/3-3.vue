<template>
	<div id=''>
		<div class='helpCenterContent'>
			<img v-bind:src='item.img' class='helpImgArrayItem' v-if="item.index==currentShow" usemap ="#helpCenterMap"  v-for='item in helpImgArray'>
			<map id ="helpCenterMap" name='helpCenterMap'>
				<area shape ="rect" coords ="0,0,185,30"  alt="注册登录" href="/#/helpcenter/center/1-1"/>
			 	<area shape ="rect" coords ="185,0,370,30" alt="产品搜索" href="/#/helpcenter/center/2-1"/>
			 	<area shape ="rect" coords ="370,0,555,30" alt="产品购买" href="/#/helpcenter/center/3-1"/>
			 	<area shape ="rect" coords ="555,0,740,30" alt="产品租赁" href="/#/helpcenter/center/4-1"/>
			 	<area shape ="rect" coords ="740,0,925,30" alt="订阅购买" href="/#/helpcenter/center/5-1"/>
			 
				<area shape ="rect" coords ="654,359,741,380" alt="next" href="/#/helpcenter/center/3-4"/>
			 	<area shape ="rect" coords ="515,359,602,380"  alt="previous" href="/#/helpcenter/center/3-2"/>
			</map>
		</div>
	</div>
</template>

<script>

	module.exports = {
    	//components configs
    	name:'1-3',
        data: function () {
            return {
              	helpImgArray:[
              		{img:require('./images/3-1.jpg'),index:1},
              		{img:require('./images/3-2.jpg'),index:2},
              		{img:require('./images/3-3.jpg'),index:3},
              		{img:require('./images/3-4.jpg'),index:4}
              		
            	],
              	currentShow:3
            }
        },
        methods:{
        	
        }
    }
</script>

<style>
img.helpImgArrayItem{
	width: 976px;
	float: left;
}
div.helpCenterContent{
	float: left;
	width: 100%;
}
</style>