<template>
  <section class="goods goods--howdeliver"> 
		<div class="wrapper wrapper--howdeliver">
			<div class="goods__coll" >
				<div :class="{'collapse': isCollapse}" class="goods__coll--wrap">
					<h2 class="title title--start">Как происходит доставка продуктов из магазинов</h2>
					<p class="goods__text goods__text--small">Вместо двух- (а то и четырёх-) часовой поездки в супермаркет Вы получаете товары и свежие продукты на дом по ценам магазина, в удобное для Вас время, ожидая курьера не более 25 минут!</p>
					<ol class="goods__list">
						<li
						v-for="item in howDeliverListFirst"
						:key="item.id"
						class="goods__text goods__text--tryit goods__text--howdeliver"
						>{{item.text}}</li>
					</ol>
					<h2 class="title">Начните экономить с igooods в Санкт-Петербурге уже сегодня!</h2>
					<p class="goods__text goods__text--small">Как изменятся ваши траты при заказе доставки еды и прочих товаров через интернет-магазин igooods? Ваши "транспортные расходы" увеличатся всего на 50-150 рублей (стоимость доставки минус ваша обычная стоимость проезда от дома до гипермаркета на общественном транспорте либо на автомобиле).</p>
					<ol class="goods__list">
						<li
						v-for="item in howDeliverListSecond"
						:key="item.id"
						class="goods__text goods__text--tryit goods__text--howdeliver"
						>{{item.text}}</li>
					</ol>
				</div>
				<button  @click="isCollapse = !isCollapse" class="goods__button goods__button--tryit goods__button--howdeliver">Узнать больше</button>
			</div>
			<div class="trynow">
				<img class="trynow__img" :src="require('@/assets/img/heart.svg')">
				<p class="trynow__text">Попробуйте прямо сейчас: привезём заказ через 90 минут</p>
				<a href="#" class="link link--button link--small">Заказать доставку</a>
			</div>
		</div>
	</section>
</template>
<script>
export default {
  data: () => {
    return {
      isCollapse: false,
    }
	},
	props: ['howDeliverListFirst', 'howDeliverListSecond']
}
</script>