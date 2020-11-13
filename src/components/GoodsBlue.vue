<template>
  <section class="goods goods--blue">
    <div class="wrapper wrapper--blue">
      <h2 class="title">Как работает igooods</h2>
      <div class="goods__row">
        <div class="goods__item goods__item--blue">
          <div class="goods__circle"><font-awesome-icon class="goods__icon" :icon="['fas', 'shopping-cart']"/></div>
          <h3 class="goods__subject">Вы заказываете продукты</h3>
          <p class="goods__text goods__text--blue">Выберите магазин и соберите корзину на сайте или в приложении. Цены как в гипермакете</p>
        </div>
        <div class="goods__item goods__item--blue">
          <div class="goods__circle goods__circle--turquoise"><font-awesome-icon class="goods__icon" :icon="['fas', 'calendar-check']"/></div>
          <h3 class="goods__subject">Мы покупаем всё по списку</h3>
          <p class="goods__text goods__text--blue">Персональный закупщик купит продукты и передаст курьеру. Если чего-то нет в наличии, согласует с вами замены</p>
        </div>
        <div class="goods__item goods__item--blue">
          <div class="goods__circle goods__circle--yellow"><font-awesome-icon class="goods__icon" :icon="['fas', 'clock']"/></div>
          <h3 class="goods__subject">Доставляем за полтора часа</h3>
          <p class="goods__text goods__text--blue">Курьер приедет к вам в удобное время. Ближайшая доставка через 90 минут, оплата наличными или картой</p>
        </div>
      </div>
      <a href="#" class="goods__link goods__link--button  link--button link--blue">Заказать доставку от 199 ₽</a>
    </div>
  </section>
</template>