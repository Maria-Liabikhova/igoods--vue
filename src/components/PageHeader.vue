<template>
	<div >
		<section class="h-menu" 
		:class="{'active': isActive}">
      <div class="h-menu__wrap"
			:class="{'active': isActive}">
        <div class="wrapper wrapper--h-menu">
          <div class="h-menu__inner h-menu__inner--top">
            <a href="#" class="link link--h-menu link--h-menu--top"><font-awesome-icon class="h-menu__icon" icon="sign-in-alt"/><p class="h-menu__text">Войти</p></a>
            <button @click="onClose()" class="h-menu__button h-menu__button--close"></button>
          </div>
           <div class="h-menu__inner h-menu__inner--info">
            <a href="#" class="link link--h-menu"><h3 class="h-menu__subject">Список магазинов</h3></a>
            <a href="#" class="link link--h-menu"><h3 class="h-menu__subject">Как это работает</h3></a>
            <ul class="h-menu__list"
						v-for="link in hmenuLinks"
						:key="link.id"
						>
              <li class="h-menu__item"><router-link to="link.href" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">{{link.text}}</p></router-link></li>
            </ul>
          </div>
          <div class="h-menu__inner h-menu__inner--bottom">
            <div class="footer__coll footer__coll--icons">
              <p class="footer__text footer__text--bold h-menu__subject--phone">8 (812) 504 89 52</p>
              <p class="h-menu__text h-menu__text--bottom">с 10:00 до 23:00 ежедневно</p>
							<div class="footer__wrapper">
								<div class="footer__wrap"
								v-for="icons in hmenuIcon"
								:key="icons.id"
								>
									<router-link to="icons.href" class="link link--h-menu link--h-menu--bottom"><img class="h-menu__soc" :src="icons.icon"></router-link> 
								</div>
							</div>
            </div>
          </div>
        </div>
      </div>
    </section>
		<header class="header">
			<section class="header__top">
				<div class="wrapper wrapper--header">
					<img class="header__img" :src="require('@/assets/img/label.jpg')" alt="логотип">
					<div class="header__list">
						<router-link
						v-for="links in headerLinks"
						:key="links.id"
						:to="links.href"
						class="link link--top link--disappear"
						>{{links.link}}
						</router-link>
						<router-link to="#" class="link link--top link--phone"><font-awesome-icon class="header__icon" :icon="['fas', 'phone' ]"/></router-link>
						<router-link to="#" href="#" class="link link--button link--small link--disappear">Заказать доставку</router-link>
					</div>
					<button
					@click="onShow()" 
					class="hamburger" type="menu"
					><font-awesome-icon icon="bars"/>
					</button>
				</div>
			</section>
			<section class="header__container">
				<section class="wrapper wrapper--profits">
					<tiny-slider ref="sliderProfits" v-bind="options" class="sliders">
							<div
							v-for="slide in headerCarousel"
							:key="slide.id"
							class="profits__wrap"
							:class="slide.class"
							>
								<div class="profits__discription">
									<h2 class="profits__title">{{slide.firstRow}}<br>{{slide.secondRow}}<br>{{slide.thirdRow}}</h2>
									<p class="profits__text">{{slide.firstTextRow}}<br>{{slide.secondTextRow}}<br>{{slide.thirdTextRow}}</p>
									<div class="profits__link-wrap">
										<router-link to="slide.linkFirst" class="link" :class="slide.classFirstLink">{{slide.linkFirstText}}<img class="profits__img profits__img--soc" :src="slide.firstlinkImg"></router-link>
										<router-link to="slide.linkSecond" class="link link--violet">{{slide.linkSecondText}}<img class="profits__img profits__img--soc" :src="slide.secondtlinkImg"></router-link>
									</div>
								</div> 
								<img class="profits__img" :class="slide.imgClass" :src="slide.img">
							</div>
					</tiny-slider>
					<button @click="onChangeSlide('prev')" class="nav nav--prev"><font-awesome-icon icon="angle-double-left"/></button>
					<button @click="onChangeSlide('next')" class="nav nav--next"><font-awesome-icon icon="angle-double-right"/></button>
				</section>
				<section class="wrapper wrapper--shops">
					<router-link
					v-for="link in headerShops"
					:key="link.id"
					:to="link.href"
					class="shops__links"
					><img class="shops__img" :src="link.imgSrc">
					</router-link>
				</section>
			</section>
		</header>
	</div>
</template>

<script>
import VueTinySlider from 'vue-tiny-slider';
export default {
	props: ["headerLinks", "headerShops", "headerCarousel", "hmenuLinks"],
	components: {'tiny-slider': VueTinySlider},
	data() {
    return {
			options: {
				fixedWidth: true,
				items: 1,
				slideBy: "page",
        mouseDrag: true,
        loop: true,
        gutter: 10,
				nav: false,
				controls: false,
				swipeAngle: false,
				autoplay: true,
				autoplayButtonOutput: false,
				speed: 400,
			},
			isActive: false,
			hmenuIcon: [
			 {icon: require('@/assets/img/instagram-brands.svg'),
        href: "#"},
        {icon: require('@/assets/img/vk-brands.svg'),
        href: "#"},
        {icon: require('@/assets/img/telegram-plane-brands.svg'),
        href: "#"},
        {icon: require('@/assets/img/facebook-f-brands.svg'),
				href: "#"},
			]
    }
	},
	methods: {
		onChangeSlide(direction) {
			return this.$refs.sliderProfits.slider.goTo(direction)
		},
		onShow() {
			console.log("hi")
			this.isActive = true
			document.body.classList.add('noScroll')
		},
		onClose() {
			console.log("bye")
			this.isActive = false
			document.body.classList.remove('noScroll')
		}
	}
};

</script>
<style scoped>
.tns-inner {
	width: 100%;
	border: 1 px solid red;
}

</style>