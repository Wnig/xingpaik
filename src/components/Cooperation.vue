<template>
    <div class="cooperation">
  		<div class="pc">
  			<div class="mask">
		      <div class="mask_">
		        <div class="mask-con">
		          <img src="../assets/00001.jpg" alt="">
		        </div>
		        <div class="mask_bg"></div>
		      </div>
		      <div class="pre-btn">
	          		<span>PREV</span>
	          		<i class="pre"></i>
	          	</div>
	          	<div class="next-btn">
	          		<span>NEXT</span>
	      			<i class="next"></i>
			    </div>
		    </div>
	  		<nav class="sider-nav clearfix">
		      	<div @click="menuIsShow" class="menu"></div>
		      	<div id="top"><i class="icon-72"></i></div>
		    </nav> 
		    <transition name='slide'>
			    <div class="sider-nav-cons" v-if="isShow">
			    	<div class="sider-nav-cons-" @click="menuIsShow"></div>
			    	<div class="sider-nav-con">
				    	<div class="cont">
				    		<div class="tips-mask" v-if="isTrue">
				    			<div class="tips-mask-con">
					    			<div class="fail"></div>
					    			<h4 style="color:#f00">很抱歉，</h4>
					    			<p>提交信息失败，请查看网络！</p>
				    			</div>
				    		</div>
				    		<i class="cancel" @click="menuIsShow"></i>
				    		<p>联系我们</p>
				    		<p>请拨打合作咨询热线：</p>
				    		<h3 style="margin-bottom: 8.33vh">400-861-8089</h3>
				    		<div class="input-con" v-if="!isSuccess">
					    		<p style="margin-bottom: 2.13vh">或者填写你的联系方式，我们会主动与你联系：</p>
								<input type="text" placeholder="姓名" v-model="userInfoItem.keyName" v-on:blur="checkData" v-on:focus="checkName">
								<input type="text" placeholder="手机号码" v-model="userInfoItem.keyTel" v-on:blur="checkData" v-on:focus="checkTel">
								<input style="margin-bottom:2.59vh" type="text" placeholder="公司名称（选填）" v-model="userInfoItem.keyComp" v-on:blur="checkData">
								<div class="btn" @click="submitData">提交</div>
								<p class="error" v-if="errormsg">{{msg}}</p>
				    		</div>
				    		<div class="tips-con" v-if="isSuccess">
				    			<div class="success"></div>
				    			<h4>感谢您对猩派客的关注！</h4>
				    			<p>我们已收到您的信息，客服会在48小时内联系您。</p>
				    		</div>
							<img class="codes" src="../assets/Group14.png" alt="">
							<p style="text-align:center">扫描小程序码立即体验</p>
				    	</div>
				    </div>
			    </div>	
		    </transition>
			<div class="selection selection-1">
				<app-header></app-header>
			  	<div class="cont">
				  	<div class="cont_">
				  		<h1>去中心化的互联网新零售营销平台<br/><strong>代理商全国火热招募中</strong><br/>… …</h1>
				  		<p>马上拨打猩派客掘金加盟热线</p>
				  		<h2>400-861-8089</h2>
				  		<div class="down-con" @click="slideDown">
					  		<div class="down">
					  		</div>
					  		<div class="slidedown">Scroll Down</div>
				  		</div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-2">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
				  			<h2 class="title">盈利模式</h2>
				  			<p class="discr">猩派客渠道盈利方式</p>
				  		</div>
				  		<div class="list-con">
				  			<div class="list_div">
				  				<div class="list_div_con">
					  				<div class="list_div_ list_div_bg_01">
					  				</div>
					  				<p>线上广告收入</p>
				  				</div>
				  			</div>
				  			<div class="list_div">
				  				<div class="list_div_con">
					  				<div class="list_div_ list_div_bg_02">
					  				</div>
					  				<p>销售佣金</p>
				  				</div>
				  			</div>
				  			<div class="list_div">
				  				<div class="list_div_con">
					  				<div class="list_div_ list_div_bg_03">
					  				</div>
					  				<p>会员收入</p>
				  				</div>
				  			</div>
				  			<div class="list_div">
				  				<div class="list_div_con">
					  				<div class="list_div_ list_div_bg_04">
					  				</div>
					  				<p>定制化服务收入</p>
				  				</div>
				  			</div>
				  		</div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-4">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
							<h2 class="title">入驻<strong>猩派客</strong>，打造企业自己的互联网新零售电商平台！</h2>
							<p class="discr">如何入驻猩派客？</p>
							<p class="dis">1.申请微信公众号（服务号）<br/>2.申请开通微信支付</p>
						</div>
						<div id="swiper" class="swiper-container clearfix">
				          	<div class="swiper-wrapper">
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00001.jpg" alt="" data-num="1">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00002.jpg" alt="" data-num="2">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00003.jpg" alt="" data-num="3">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00004.jpg" alt="" data-num="4">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00005.jpg" alt="" data-num="5">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00006.jpg" alt="" data-num="6">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00007.jpg" alt="" data-num="7">
				          				<div class="list_bg">
				          					<i class="add"></i>
				          				</div> 
				          			</div>
				          		</div>
				          	</div>
				        </div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-3">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
							<h2 class="title">发展蓝图</h2>
							<p class="discr">猩派客1-2年<br/>发展蓝图</p>
						</div>
						<div class="map">
							<img src="../assets/83.png" alt="">
							<span class="c_01">北<br/>京</span> 
							<span class="c_02">河<br/>南</span>
							<span class="c_03">江<br/>苏</span>
							<span class="c_04">上<br/>海</span>
							<span class="c_05">浙<br/>江</span>
							<span class="c_06">湖<br/>南</span>
							<span class="c_07">福<br/>建</span>
							<span class="c_08">广<br/>东</span>
							<span class="c_09">四<br/>川</span>
							<span class="c_10">重<br/>庆</span>
						</div>
						<ul>
							<li><i class="y_dot"></i>首批已覆盖区域</li>
							<li><i class="b_dot"></i>业务布局中</li>
							<li><i class="g_dot"></i>暂无发展计划</li>
						</ul>
				  	</div>
				</div>
				<app-footer></app-footer>
			</div>
		</div>
		<div class="mob">
			<div class="selection selection-1">
				<app-header></app-header>
			  	<div class="cont">
				  	<div class="cont_">
				  		<h1>去中心化的互联网新<br/>零售营销平台<br/><strong>代理商全国火热招募中</strong><br/>… …</h1>
				  		<p>马上拨打猩派客掘金加盟热线</p>
				  		<h2>400-861-8089</h2>
				  		<div class="down-con" @click="slideDown">
					  		<div class="down">
					  		</div>
					  		<div class="slidedown">Scroll Down</div>
				  		</div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-2">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
				  			<h2 class="title">盈利模式</h2>
				  			<p class="discr">猩派客渠道盈利方式</p>
				  		</div>
				  		<div id="swiperCon" class="swiper-container clearfix">
				          	<div class="swiper-wrapper">
				            	<div class="swiper-slide">
						  			<div class="list_div">
						  				<div class="list_div_con">
							  				<div class="list_div_ list_div_bg_01">
							  				</div>
							  				<p>线上广告收入</p>
						  				</div>
						  			</div>
				            	</div>
				            	<div class="swiper-slide">
						  			<div class="list_div">
						  				<div class="list_div_con">
							  				<div class="list_div_ list_div_bg_02">
							  				</div>
							  				<p>销售佣金</p>
						  				</div>
						  			</div>
				            	</div>
				            	<div class="swiper-slide">
						  			<div class="list_div">
						  				<div class="list_div_con">
							  				<div class="list_div_ list_div_bg_03">
							  				</div>
							  				<p>会员收入</p>
						  				</div>
						  			</div>
				            	</div>
				            	<div class="swiper-slide">
						  			<div class="list_div">
						  				<div class="list_div_con">
							  				<div class="list_div_ list_div_bg_04">
							  				</div>
							  				<p>定制化服务收入</p>
						  				</div>
						  			</div>
				            	</div>
				            </div>
				            <div class="swiper-pagination"></div>
				        </div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-4">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
							<h2 class="title">入驻<strong>猩派客</strong>打造<br/>企业自己的互联网新<br/>零售电商平台！</h2>
							<p class="discr">如何入驻猩派客？</p>
							<p class="dis">1.申请微信公众号（服务号）<br/>2.申请开通微信支付</p>
						</div>
						<div id="swiper02" class="swiper-container clearfix">
				          	<div class="swiper-wrapper">
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00001.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00002.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00003.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00004.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00005.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00006.jpg" alt="">
				          			</div>
				          		</div>
				          		<div class="swiper-slide">
				          			<div class="list_div">
				          				<img src="../assets/00007.jpg" alt="">
				          			</div>
				          		</div>
				          	</div>
				          	<div class="swiper-pagination"></div>
				        </div>
				  	</div>
				</div>
			</div>
			<div class="selection selection-3">
			  	<div class="cont">
				  	<div class="cont_">
				  		<div class="discr-con">
							<h2 class="title">发展蓝图</h2>
							<p class="discr">猩派客1-2年<br/>发展蓝图</p>
						</div>
						<div class="map">
							<img src="../assets/021.png" alt="">
							<span class="c_01">北<br/>京</span> 
							<span class="c_02">河<br/>南</span>
							<span class="c_03">江<br/>苏</span>
							<span class="c_04">上<br/>海</span>
							<span class="c_05">浙<br/>江</span>
							<span class="c_06">湖<br/>南</span>
							<span class="c_07">福<br/>建</span>
							<span class="c_08">广<br/>东</span>
							<span class="c_09">四<br/>川</span>
							<span class="c_10">重<br/>庆</span>
						</div>
						<ul>
							<li><i class="y_dot"></i>首批已覆盖区域</li>
							<li><i class="b_dot"></i>业务布局中</li>
							<li><i class="g_dot"></i>暂无发展计划</li>
						</ul>
				  	</div>
				</div>
				<app-footer></app-footer>
			</div>
			<nav class="sider-nav clearfix">
		      <div @click="menuIsShow" class="menu"></div>
		      <div id="top"><i class="icon-72"></i></div>
		    </nav> 
		    <transition name='slide'>
		    	<div class="sider-nav-cons" v-if="isShow">
			    	<div class="sider-nav-cons-" @click="menuIsShow"></div>
			    	<div class="sider-nav-con">
				    	<div class="cont">
				    		<div class="tips-mask" v-if="isTrue">
				    			<div class="tips-mask-con">
					    			<div class="fail"></div>
					    			<h4 style="color:#f00">很抱歉，</h4>
					    			<p>提交信息失败，请查看网络！</p>
				    			</div>
				    		</div>
				    		<i class="cancel" @click="menuIsShow"></i>
				    		<p>联系我们</p>
				    		<p>请拨打合作咨询热线：</p>
				    		<h3 style="margin-bottom: 8.33vh">400-861-8089</h3>
				    		<div class="input-con" v-if="!isSuccess">
					    		<p style="margin-bottom: 2.13vh">或者填写你的联系方式，我们会主动与你联系：</p>
								<input type="text" placeholder="姓名" v-model="userInfoItem.keyName" v-on:blur="checkData" v-on:focus="checkName">
								<input type="text" placeholder="手机号码" v-model="userInfoItem.keyTel" v-on:blur="checkData" v-on:focus="checkTel">
								<input style="margin-bottom:2.59vh" type="text" placeholder="公司名称（选填）" v-model="userInfoItem.keyComp" v-on:blur="checkData">
								<div class="btn" @click="submitData">提交</div>
								<p class="error" v-if="errormsg">{{msg}}</p>
				    		</div>
				    		<div class="tips-con" v-if="isSuccess">
				    			<div class="success"></div>
				    			<h4>感谢您对猩派客的关注！</h4>
				    			<p>我们已收到您的信息，客服会在48小时内联系您。</p>
				    		</div>
				    	</div>
				    </div>
			    </div>
		    </transition>
		</div>
  	</div>
</template>

<script>
import Header from './Header'
import Footer from './Footer'
import qs from 'qs'

//封装过期控制代码
function set(key,value){
    var curTime = new Date().getTime();
    localStorage.setItem(key,JSON.stringify({data:value,time:curTime}));
}
function get(key, exp){
    var data = localStorage.getItem(key);
    var dataObj = JSON.parse(data);
    if (data != "" && data != null) {
	    if (new Date().getTime() - dataObj.time>exp) {
	        // console.log('信息已过期');
	    } else {
	        var dataObjDatatoJson = JSON.parse(dataObj.data)
	        return dataObjDatatoJson;
	    }
    }
}

export default {
  name: 'Cooperation',
  data () {
    return {
    	isMask: false,
    	isShow: false,
    	isTrue: false,
    	isSuccess: false,
    	userInfoItem: {
	        keyName : '',
	        keyTel: '',
	        keyComp: ''
	    },
	    errormsg: false,
	    msg: ''
    }
  },
  created() {
  	var dataObjData = get('information',1000*60*60*24);//过期时间为24小时
  	// var dataObjData = get('information',1000*60); //过期时间为1分钟

    if (dataObjData != "" && dataObjData != null) {
        this.isSuccess = true;
    } else {
        this.isSuccess = false;
    };
  },
  methods: {
  	slideDown() {
      let downHeight = document.documentElement.clientHeight || document.body.clientHeight;
      window.scrollTo(0, downHeight);
      this.slideShow = true;
    },
    isMasks() {
    	this.isMask = !this.isMask;
    },
    menuIsShow() {
    	this.isShow = !this.isShow;
    },
    checkName() {
    	let that = this;
    	if(that.userInfoItem.keyTel == '' || that.userInfoItem.keyTel == undefined) {
        	that.errormsg = true;
        	that.msg = '请填写手机号';
        } else if(!(/^1(3|4|5|7|8)\d{9}$/.test(that.userInfoItem.keyTel))) {
        	that.errormsg = true;
        	that.msg = '请填写正确手机号';
        } else {
        	that.errormsg = false;
        }
    },
    checkTel() {
    	let that = this;
    	if(that.userInfoItem.keyName == '' || that.userInfoItem.keyName == undefined) {
            that.errormsg = true;
            that.msg = '请填写姓名';
        } else {
	    	that.errormsg = false;
        }
    },
    checkData() {
    	let that = this;
    	if(that.userInfoItem.keyName == '' || that.userInfoItem.keyName == undefined) {
            that.errormsg = true;
            that.msg = '请填写姓名';
        } else if(that.userInfoItem.keyTel == '' || that.userInfoItem.keyTel == undefined) {
        	that.errormsg = true;
        	that.msg = '请填写手机号';
        } else if(!(/^1(3|4|5|7|8)\d{9}$/.test(that.userInfoItem.keyTel))) {
        	that.errormsg = true;
        	that.msg = '请填写正确手机号';
        } else {
        	that.errormsg = false;
        }
    },
    submitData() {
    	let that = this;
    	if(that.userInfoItem.keyName == '' || that.userInfoItem.keyName == undefined) {
            that.errormsg = true;
            that.msg = '请填写姓名';
        } else if(that.userInfoItem.keyTel == '' || that.userInfoItem.keyTel == undefined) {
        	that.errormsg = true;
        	that.msg = '请填写手机号';
        } else if(!(/^1(3|4|5|7|8)\d{9}$/.test(that.userInfoItem.keyTel))) {
        	that.errormsg = true;
        	that.msg = '请填写正确手机号';
        } else {
	        this.$http.post('https://abc.smartmapdt.com/mall/rest/businessReservation/reservation', qs.stringify({
	              	name: that.userInfoItem.keyName,
				    phone: that.userInfoItem.keyTel,
				    companyName: that.userInfoItem.keyComp
            	})).then((response) => {

				that.userInfoItem.keyName = '';
				that.userInfoItem.keyTel = '';
				that.userInfoItem.keyComp = '';
				
				if(response.data.status == '1') {
					that.errormsg = false;
					that.isTrue = false;
					that.isSuccess = true;
					var values =  '{"isSuccess": "true"}';
    				set('information', values); 

				} else if(response.data.status == '100001') {
					that.errormsg = true;
	    			that.isTrue = false;
	    			that.msg = response.data.msg;

				} else {
					that.errormsg = false;
	    			that.isTrue = true;
					that.isSuccess = false;

					setTimeout(() => {
				    	that.isTrue = false;
			    	}, 2000);
				};
		    	
			});
        };
    }
  },
  components: {
    'app-header': Header,
    'app-footer': Footer
  },
  mounted() {
  	// 返回顶部
    $('#top, #tops').on('click', function() {
    	$('html, body').animate({scrollTop: '0px'}, 800);
    });

  	$(window).scroll(function() {
	　　 var scrollTop = $(this).scrollTop();
	　　 var scrollHeight = $(document).height();
	　　 var windowHeight = $(this).height();

		if(scrollTop < scrollHeight / 9) {
			$('#tops').css({
				'display': 'none'
			});
		} else {
			$('#tops').css({
				'display': 'block'
			});
		}
	});

	let swiper01 = new Swiper('#swiper', {
      slidesPerView: 7,
      spaceBetween: 8,
      speed: 500,
      mousewheelControl: true,
      releaseOnEdges: true,
      paginationClickable: true,
    });

    let swiper02 = new Swiper('#swiper02', {
      slidesPerView: 1,
      spaceBetween: 8,
      speed: 500,
      mousewheelControl: true,
      releaseOnEdges: true,
      paginationClickable: true,
      pagination: '.swiper-pagination',
    });


	let swiper03 = new Swiper('#swiperCon', {
      loop: true, 
      slidesPerView: 1,
      spaceBetween: 100,
      speed: 500,
      mousewheelControl: true,
      releaseOnEdges: true,
      paginationClickable: true,
      pagination: '.swiper-pagination',
    });

    $('.list_div').on('click', function() {
      $('.mask').css({
        'display': 'block'
      });
      $('body').css({ 
        "overflow-y":"hidden"       
      });
      let imgSrc = $(this).find('img').attr('src');
      let num = $(this).find('img').attr('data-num');
      $('.mask img').attr('src', imgSrc);
      $('.mask img').attr('data-num', num);
    });
    $('.mask_bg').on('click', function() {
      $('.mask').css({
        'display': 'none'
      });
      $('body').css({ 
        "overflow-y":"scroll"       
      });
    });

    $('.pre-btn').on('click', function() {
    	let num = $('.mask img').attr('data-num');

    	if(num < 1 || num == 1) {
    		num = 1;
    		let imgSrc = $('#swiper .swiper-slide').eq(num-1).find('img').attr('src');
    		$('.mask img').attr('src', imgSrc);
    		$('.mask img').attr('data-num', num);
    	} else {
			num--;
			let imgSrc = $('#swiper .swiper-slide').eq(num-1).find('img').attr('src');
			$('.mask img').attr('src', imgSrc);
    		$('.mask img').attr('data-num', num);
    	};
    	
    });

    $('.next-btn').on('click', function() {
    	let num = $('.mask img').attr('data-num');

    	if(num > $('#swiper .swiper-slide').length || num == $('#swiper .swiper-slide').length) {
    		num = $('#swiper .swiper-slide').length;
    		let imgSrc = $('#swiper .swiper-slide').eq(num-1).find('img').attr('src');
    		$('.mask img').attr('src', imgSrc);
    		$('.mask img').attr('data-num', num);
    	} else {
			num++;
			let imgSrc = $('#swiper .swiper-slide').eq(num-1).find('img').attr('src');
			$('.mask img').attr('src', imgSrc);
    		$('.mask img').attr('data-num', num);
    	};
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	/*selection-1*/
	.selection-1 {
		background: url('../assets/67.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-1 .cont {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 50%;
		color: #FFFFFF;
		text-align: center;
		line-height: 2.34vw;
		font-size: 1.3vw;
	}
	.selection-1 h1 {
		/*height: 5.69vw;*/
		margin-bottom: 6.11vh;
		color: #FFFFFF;
		text-align: center;
		line-height: 4.39vw;
		font-size: 2.86vw;
		font-weight: 600;
		font-family: 'PingFangSC-Regular';
	}
	.selection-1 h1 strong {
		display: inline-block;
		color: #FF973F;
		line-height: 4.53vw;
		font-size: 2.86vw;
		font-family: 'PingFangSC-Regular';
	}
	.selection-1 p {
		color: #FFFFFF;
		text-align: center;
		line-height: 2.34vw; 
		font-size: 1.3vw;
		font-family: 'PingFangSC-Thin';
	}
	.selection-1 p span {
		display: inline-block;
		width: 2vw;
	}
	.selection-1 h2 {
		margin-top: 2vh;
		color: #FF973F;
		font-size: 2.86vw;
		font-family: 'PingFangSC-Regular';
	}

	/*selection-2*/
	.selection-2 {
		background: #f5f5f5;
	}
	.selection-2 .title {
		color: #000;
	}
	.selection-2 .discr {
		color: #999;
	}
	.selection-2 .cont {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 88%;
	}
	.selection-2 .list-con {
		display: flex;
		justify-content: center;
		align-items: center;
		margin-top: 10.72vh;
	}
	.selection-2 .list_div {
		width: 14.43vw;
		height: 21.3vw;
		margin: 0 1.35vw;
		cursor: pointer;
		-webkit-transition: all 0.5s;
	    transition: all 0.5s;
	}
	.selection-2 .list_div_con {
		width: 100%;
		height: 100%;
	}
	.selection-2 .list_div_ {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 15.73vw;
	}
	.selection-2 .list_div_bg_01 {
		background: url('../assets/79.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-2 .list_div_bg_02 {
		background: url('../assets/80.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-2 .list_div_bg_03 {
		background: url('../assets/81.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-2 .list_div_bg_04 {
		background: url('../assets/82.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-2 .list_div p {
		height: 5.57vw;
		color: #999999;
		text-align: center;
		line-height: 5.57vw;
		font-size: 1.3vw;
		font-family: 'PingFangSC-Light';
		background-color: #fff;
	}
	

	/*selection-3*/
	.selection-3 {
		height: 116.11vh;
		background: url('../assets/85.jpg') center center no-repeat;
		background-size: cover;
	}

	.selection-3 .cont {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}
	.selection-3 .discr-con {
		position: absolute;
		left: 9.32vw;
		top: 14.81vh;
		width: 23.44vw;
	}
	.selection-3 .title {
		margin-bottom: 4.17vh;
		text-align: left;
	}
	.selection-3 .title:after {
		margin: 0;
	}
	.selection-3 .discr {
		color: #FFFFFF;
		text-align: left;
		font-size: 1.67vw;
	}
	.selection-3 .map {
		position: relative;
		width: 55.68vw;
	}
	.selection-3 .map img {
		display: block;
		width: 100%;
		margin: 0 auto;
	}
	.selection-3 ul {
		position: absolute;
		right: 11.04vw;
		bottom: 33.81vh;
	}
	.selection-3 li {
		margin-bottom: 2.5vh;
		color: #FFFFFF;
		font-size: 1.04vw;
	}
	.selection-3 li i {
		display: inline-block;
		width: 0.83vw;
		height: 0.83vw;
		margin-right: 0.63vw;
		border-radius: 50%;
	}
	.selection-3 .y_dot {
		background: #FFB800;
	}
	.selection-3 .b_dot {
		background: #65C7F1;
	}
	.selection-3 .g_dot {
		background: #999999;
	}
	.selection-3 .map span {
		position: absolute;
		color: #000000;
		line-height: 1.1vw;
		font-size: 0.9vw;
		font-family: 'PingFangSC-Semibold';
	}
	.map .c_01 {
		right: 24.5%;
    	bottom: 57.5%;
    	-webkit-animation: float_01 2.6s infinite;
    	animation: float_01 2.6s infinite;
	}
	.map .c_02 {
		right: 28.5%;
    	bottom: 37.5%;
    	-webkit-animation: float_02 1.6s infinite;
    	animation: float_02 1.6s infinite;
	}
	.map .c_03 {
		right: 16.2%;
    	bottom: 37.5%;
    	-webkit-animation: float_02 2s infinite;
    	animation: float_02 2s infinite;
	}
	.map .c_04 {
		right: 13%;
    	bottom: 32.5%;
    	-webkit-animation: float_01 1.6s infinite;
    	animation: float_01 1.6s infinite;
	}
	.map .c_05 {
		right: 15%;
    	bottom: 26.5%;
    	-webkit-animation: float_02 3s infinite;
    	animation: float_02 3s infinite;
	}
	.map .c_06 {
		right: 30.5%;
    	bottom: 19.5%;
    	-webkit-animation: float_01 3s infinite;
    	animation: float_01 3s infinite;
	}
	.map .c_07 {
		right: 18.5%;
    	bottom: 15.5%;
    	-webkit-animation: float_02 1.3s infinite;
    	animation: float_02 1.3s infinite;
	}
	.map .c_08 {
		right: 26.5%;
    	bottom: 8.5%;
    	-webkit-animation: float_01 2.5s infinite;
    	animation: float_01 2.5s infinite;
	}
	.map .c_09 {
		right: 48.5%;
    	bottom: 26.5%;
    	-webkit-animation: float_02 2.8s infinite;
    	animation: float_02 2.8s infinite;
	}
	.map .c_10 {
		right: 38.5%;
    	bottom: 26.5%;
    	-webkit-animation: float_01 2s infinite;
    	animation: float_01 2s infinite;
	}
	
	/*selection-4*/
	.selection-4 {
		background: url('../assets/19.jpg') center center no-repeat;
		background-size: cover;
	}
	.selection-4 h2 strong {
		color: #FF983E;
		font-family: 'PingFangSC-Semibold';
	}
	.selection-4 .cont {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}
	.selection-4 .dis {
		margin-top: 2.87vh;
		color: #999999;
		text-align: center;
		font-size: 1.3vw;
		/*font-family: 'PingFangSC-Light';*/
	}
	#swiper {
		position: relative;
		width: 100vw;
		height: 36.39vh;
		margin-top: 10.93vh;
	}
	.selection-4 .list_div {
		position: relative;
	}
	.selection-4 .list_div img {
		display: block;
		width: 100%;
		margin: 0 auto;
	}
	.selection-4 .list_bg  {
		position: absolute;
		top: 0;
		left: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 100%;
		background: rgba(0,0,0,0.65);
		z-index: 2;
	}
	.selection-4 .list_bg i {
		display: block;
		width: 4.06vw;
		height: 4.06vw;
		background: url('../assets/0049.svg') center center no-repeat;
		background-size: 100% 100%;
		cursor: pointer;
		opacity: 0;
		-webkit-transform: scale(0);
	    transform: scale(0);
	    -webkit-transform: rotate(90deg);
	    transform: rotate(90deg);
	    -webkit-transition: all 1.2s;
	    transition: all 1.2s;
	}
	.selection-4 .list_bg:hover i {
		opacity: 1;
		-webkit-transform: scale(1.1);
	    transform: scale(1.1);
	    -webkit-transition: all 1.2s;
	    transition: all 1.2s;
	}
	.mask .pre-btn, .mask .next-btn {
		position: absolute;
		color: #FFFFFF;
		text-align: center;
		font-size: 1.3vw;
		font-family: 'PingFangSC-Thin';
		z-index: 9999;
		cursor: pointer;
		opacity: 0.3;
		-webkit-transition: all 1.2s;
	    transition: all 1.2s;
	}
	.mask .pre-btn:hover , .mask .next-btn:hover {
		opacity: 1;
		-webkit-transition: all 1.2s;
	    transition: all 1.2s;
	}
	.mask .pre-btn {
		left: 5.21vw;
		top: 33.89vh;
	}
	.mask .next-btn {
		right: 5.21vw;
		top: 33.89vh;
	}
	.mask .pre-btn span {
		display: block;
	}
	.mask .next-btn span {
		display: block;
	}
	.mask .pre-btn i {
		display: block;
		width: 4.06vw;
		height: 4.06vw;
		margin: 1.39vh auto 0;
		background: url('../assets/0047.svg') center center no-repeat;
		background-size: 100% 100%;
	}
	.mask .next-btn i {
		display: block;
		width: 4.06vw;
		height: 4.06vw;
		margin: 1.39vh auto 0;
		background: url('../assets/0048.svg') center center no-repeat;
		background-size: 100% 100%;
	}

	.mask {
	    display: none;
	    position: fixed;
	    left: 0;
	    top: 0;
	    width: 100%;
	    height: 100%;
	    background: rgba(0,0,0,0.60);
	    z-index: 999999;
	}
	.mask_ {
	    display: flex;
	    justify-content: center;
	    align-items: center;
	}
	.mask_bg {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
	}
	.mask-con {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		margin: 0 auto;
	    display: flex;
	    justify-content: center;
	    align-items: center;
	    width: 40%;
	    height: 100vh;
	}
	.mask img {
	    display: block;
	    width: 100%;
	    height: auto;
	}


	@media screen and (max-width: 750px) {
		/*selection-1*/
		.selection-1 {
			background: url('../assets/019.jpg') center center no-repeat;
			background-size: cover;
		}
		.selection-1 .cont {
			height: 70%;
			line-height: 11.2vw;
			font-size: 8vw;
		}
		.selection-1 h1 {
			height: auto;
			margin-bottom: 6.11vh;
			line-height: 11.2vw;
			font-size: 8vw;
		}
		.selection-1 h1 strong {
			line-height: 11.2vw;
			font-size: 8vw;
		}
		.selection-1 p {
			color: #FFFFFF;
			text-align: center;
			line-height: 2.34vw; 
			font-size: 3.3vw;
			font-family: 'PingFangSC-Thin';
		}
		.selection-1 h2 {
			/*margin-top: 2vh;*/
			color: #FF973F;
			font-size: 7.86vw;
			font-family: 'PingFangSC-Regular';
		}

		/*selection-2*/
		.selection-2 .cont {
			height: 100%;
		}
		#swiperCon {
			width: 65.6vw;
			height: 105.53vw;
			margin-top: 3vh;
		}
		.selection-2 .list_div {
			width: 65.6vw;
			height: 96.53vw;
			margin: 0;
		}
		.selection-2 .list_div_con {
			width: 100%;
			height: 100%;
		}
		.selection-2 .list_div_ {
			width: 100%;
			height: 71.2vw;
		}
		.selection-2 .list_div p {
			height: 25.33vw;
			line-height: 25.33vw;
			font-size: 6.67vw;
		}
		
		/*selection-3*/
		.selection-3 {
			height: 143.24vh;
			background: none;
		}
		.selection-3 .cont {
			height: 120.7vh;
			background: url('../assets/020.jpg') center center no-repeat;
			background-size: cover;
		}
		.selection-3 .discr-con {
			position: static;
			width: 100%;
			padding-top: 7.95vh;
			padding-left: 9.87vw;
		}
		.selection-3 .title {
			margin-bottom: 4.17vh;
			text-align: left;
		}
		.selection-3 .title:after {
			margin: 0;
		}
		.selection-3 .discr {
			font-size: 3.2vw;
		}
		.selection-3 .map {
			width: 100%
		}
		.selection-3 .map img {
			display: block;
			width: 100%;
			margin: 0 auto;
		}
		.selection-3 ul {
			position: absolute;
			right: 65vw;
    		bottom: 90.81vh;
		}
		.selection-3 li {
			margin-bottom: 0.45vh;
			color: #FFFFFF;
			font-size: 3.2vw;
		}
		.selection-3 li i {
			display: inline-block;
			width: 2.13vw;
			height: 2.13vw;
			margin-right: 0.63vw;
			border-radius: 50%;
		}
		.selection-3 .map span {
			position: absolute;
			color: #000000;
			line-height: 4vw;
			font-size: 3.2vw;
		}

		.map .c_01 {
			right: 39.5%;
    		bottom: 55.5%;
	    	-webkit-animation: float_01 2.6s infinite;
	    	animation: float_01 2.6s infinite;
		}
		.map .c_02 {
			right: 45.5%;
	    	bottom: 37.5%;
	    	-webkit-animation: float_02 1.6s infinite;
	    	animation: float_02 1.6s infinite;
		}
		.map .c_03 {
			right: 26.2%;
	    	bottom: 37.5%;
	    	-webkit-animation: float_02 2s infinite;
	    	animation: float_02 2s infinite;
		}
		.map .c_04 {
			right: 21%;
	    	bottom: 32.5%;
	    	-webkit-animation: float_01 1.6s infinite;
	    	animation: float_01 1.6s infinite;
		}
		.map .c_05 {
			right: 24%;
	    	bottom: 26.5%;
	    	-webkit-animation: float_02 3s infinite;
	    	animation: float_02 3s infinite;
		}
		.map .c_06 {
			right: 48.5%;
	    	bottom: 19.5%;
	    	-webkit-animation: float_01 3s infinite;
	    	animation: float_01 3s infinite;
		}
		.map .c_07 {
			right: 29.5%;
	    	bottom: 15.5%;
	    	-webkit-animation: float_02 1.3s infinite;
	    	animation: float_02 1.3s infinite;
		}
		.map .c_08 {
			right: 40.5%;
	    	bottom: 8.5%;
	    	-webkit-animation: float_01 2.5s infinite;
	    	animation: float_01 2.5s infinite;
		}
		.map .c_09 {
			right: 77.5%;
	    	bottom: 26.5%;
	    	-webkit-animation: float_02 2.8s infinite;
	    	animation: float_02 2.8s infinite;
		}
		.map .c_10 {
			right: 61.5%;
	    	bottom: 26.5%;
	    	-webkit-animation: float_01 2s infinite;
	    	animation: float_01 2s infinite;
		}

		/*selection-4*/
		.selection-4 {
			height: 135vh;
			background: url('../assets/19.jpg') center center no-repeat;
			background-size: cover;
		}
		.selection-4 h2 strong {
			color: #FF983E;
			font-family: 'PingFangSC-Semibold';
		}
		.selection-4 .cont {
			display: flex;
			justify-content: center;
			align-items: center;
			height: 100%;
		}
		.selection-4 .dis {
			margin-top: 2.87vh;
			color: #999999;
			text-align: center;
			font-size: 3vw;
			/*font-family: 'PingFangSC-Light';*/
		}
		#swiper02 {
			width: 100vw;
			height: 70vh;
			margin-top: 8.93vh;
		}
		.selection-4 .list_div {
			position: relative;
			height: 90%;
		}
		.selection-4 .list_div img {
			display: block;
			width: 80%;
			height: 100%;
			margin: 0 auto;
		}
		.selection-4 .list_bg  {
			position: absolute;
			top: 0;
			left: 0;
			display: flex;
			justify-content: center;
			align-items: center;
			width: 100%;
			height: 100%;
			background: rgba(0,0,0,0.65);
			z-index: 2;
		}
		.selection-4 .list_bg i {
			display: block;
			width: 4.06vw;
			height: 4.06vw;
			background: url('../assets/0049.svg') center center no-repeat;
			background-size: 100% 100%;
			cursor: pointer;
			opacity: 0;
			-webkit-transform: scale(0);
		    transform: scale(0);
		    -webkit-transform: rotate(90deg);
		    transform: rotate(90deg);
		    -webkit-transition: all 1.2s;
		    transition: all 1.2s;
		}
		.selection-4 .list_bg:hover i {
			opacity: 1;
			-webkit-transform: scale(1.1);
		    transform: scale(1.1);
		    -webkit-transition: all 1.2s;
		    transition: all 1.2s;
		}

	}
	@media screen and (min-width: 751px) {
		.selection-2 .list_div:hover {
			box-shadow: 0 8px 30px 0 rgba(0, 0 ,0, 0.1);
		    -webkit-transform: scale(1.05) translateY(-5px);
		    transform: scale(1.05) translateY(-5px);
		    -webkit-transition: all 0.5s;
		    transition: all 0.5s;
		}
	}
</style>
