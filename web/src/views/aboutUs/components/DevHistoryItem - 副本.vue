<template>
	<div>
		<div class="devhistory">
			<div class="ptheme">
				<h3>发展历程</h3>
				<img src="../../assets/images/theme.png" />
			</div>
			<div class="aboutnav">
						<div class="timeswiper">
				<div class="timeline">			
					<swiper :options="swiperOption">
					<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2002-2003</div>
							<div class="itemcon">
								<h3>中科信利实现电信市场的更大规模商用，提出国内第一个自主研发的电信级语音识别解决方案</h3>
								<p>通过三家SP合作，在中国移动彩铃IVR下载市场拿下23个省（包括 用户规模最大的五个省，广东、江苏、浙江、福建、山东）；成为华为公司的旋律识别、中文语音识别引擎供应商。</p>
							</div>							
						</swiper-slide>
						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2004</div>
								<div class="itemcon">
								<h3>中科信利实现电信市场的更大规模商用，提出国内第一个自主研发的电信级语音识别解决方案</h3>
								<p>通过三家SP合作，在中国移动彩铃IVR下载市场拿下23个省（包括 用户规模最大的五个省，广东、江苏、浙江、福建、山东）；成为华为公司的旋律识别、中文语音识别引擎供应商。</p>
							</div>	
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2005</div>
								<div class="itemcon">
								<h3>中科信利实现电信市场的更大规模商用，提出国内第一个自主研发的电信级语音识别解决方案</h3>
								<p>通过三家SP合作，在中国移动彩铃IVR下载市场拿下23个省（包括 用户规模最大的五个省，广东、江苏、浙江、福建、山东）；成为华为公司的旋律识别、中文语音识别引擎供应商。</p>
							</div>	
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2006</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2007</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2008</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2009</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2010</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2012</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2013</div>
						</swiper-slide>

						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2014</div>
						</swiper-slide>
						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2015</div>
						</swiper-slide>
						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2016</div>
						</swiper-slide>
						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2017</div>
						</swiper-slide>
						<swiper-slide>
							<div class="item-tail"></div>
							<div class="item-head"></div>
							<div class="item-content">2018</div>
						</swiper-slide>				
					</swiper>
					</div>
					<div class="swiper-button-prev" slot="button-prev"></div>
					<div class="swiper-button-next" slot="button-next"></div>
				</div>
			</div>
			<div class="container">
				<div class="aboutuscon clearfix">
					<div class="about_left">
						<Menu active-name="comprofileitem" @on-select="changeMenu">
							<div class="companynav">
								<MenuItem name="comprofileitem" v-for="(item,index)  in companytab" :key="index" :name="item.name">
								<div class="clearfix mitem">
									<div class="larrow"></div>
									<div class="coname"><i><img class="cimg" :src="item.cimg"/> <img :src="item.himg"  class="himg"/></i><span>{{item.title}}</span></div>
									<div class="rarrow"></div>
									<div class="hline"></div>
								</div>
								</MenuItem>
							</div>
						</Menu>
						<div class="left_cirlce"></div>
					</div>

					<div class="about_right">
						<transition name="slide-fade">
							<router-view :is="currentView"></router-view>
						</transition>

					</div>

				</div>

			</div>
		</div>
	</div>
</template>
<script>
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	import comprofileitem from './ComProfileItem.vue'
	import corcultureitem from './CorCultureItem.vue'
	import honoritem from './HonorItem.vue'
	export default {
		name: 'App',
		components: {
			swiper,
			swiperSlide,
			comprofileitem,
			corcultureitem,
			honoritem
		},
		data() {
			return {
				swiperOption: {
					slidesPerView: 'auto',
					spaceBetween: 30,
					navigation: {
						nextEl: '.swiper-button-next',
						prevEl: '.swiper-button-prev'
					}
				},		
				companytab: [{
						name: "comprofileitem",
						title: "公司简介",
						cimg: require("../../assets/images/cprofile.png"),
						himg: require("../../assets/images/cprofile1.png")
					},
					{
						name: "corcultureitem",
						title: "企业文化",
						cimg: require("../../assets/images/culture.png"),
						himg: require("../../assets/images/culture1.png")
					},
					{
						name: "honoritem",
						title: "荣誉资质",
						cimg: require("../../assets/images/honor.png"),
						himg: require("../../assets/images/honor1.png")
					},

				],
				currentView: "comprofileitem",
			}
		},
		methods: {
			changeMenu: function(name) {
				this.currentView = name;
			},
		}
	}
</script>

<style>

</style>