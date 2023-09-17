<template>
  <div class="tariff__plans plans">
    <div class="plans__list">
      <table class="list">
        <tr class="list__item item">
          <td class="item__title">
            <div class="component-timer">
              <TariffTimer/>
              <div class="timer-title">(для діючих передплатників додаткова знижка 10%)</div>
            </div>
          </td>
          <td class="item__status-superpro">
            <div class="plan__top top">
              <div class="hit-sale">
                <span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="10" height="16" viewBox="0 0 10 16" fill="none">
                    <path d="M1.58652 10.4346L4.89479 13.9128L8.20306 10.4346L9.52637 11.1302L4.89479 15.9998L0.263208 11.1302L1.58652 10.4346Z" fill="#232323"/>
                    <path d="M1.58652 5.21728L4.89479 8.69555L8.20306 5.21729L9.52637 5.91294L4.89479 10.7825L0.263208 5.91294L1.58652 5.21728Z" fill="#232323" fill-opacity="0.5"/>
                    <path d="M1.58652 -3.64895e-07L4.89479 3.47826L8.20306 -6.08158e-08L9.52637 0.695652L4.89479 5.56522L0.263208 0.695652L1.58652 -3.64895e-07Z" fill="#232323" fill-opacity="0.1"/>
                    </svg>
                </span>
                  Хіт Продажу
                  <span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="10" height="16" viewBox="0 0 10 16" fill="none">
                    <path d="M1.58652 10.4346L4.89479 13.9128L8.20306 10.4346L9.52637 11.1302L4.89479 15.9998L0.263208 11.1302L1.58652 10.4346Z" fill="#232323"/>
                    <path d="M1.58652 5.21728L4.89479 8.69555L8.20306 5.21729L9.52637 5.91294L4.89479 10.7825L0.263208 5.91294L1.58652 5.21728Z" fill="#232323" fill-opacity="0.5"/>
                    <path d="M1.58652 -3.64895e-07L4.89479 3.47826L8.20306 -6.08158e-08L9.52637 0.695652L4.89479 5.56522L0.263208 0.695652L1.58652 -3.64895e-07Z" fill="#232323" fill-opacity="0.1"/>
                    </svg>
                </span>
              </div>
              <div class="top__title title">
                <div class="title__name">Суперпрофесіонал</div>
                <div class="title__discount discount">-75%</div>
              </div>
              <div class="top__description">8 професійних курсів<br> за ціною 2</div>
              <div class="top__price price">
                <div class="price__old">1079 грн/міс.</div>
                <div class="price__new">679 грн/міс.</div>
              </div>
              <div class="top__payment payment">
                <div class="payment__card"><v-button>Оплатити карткою</v-button></div>
                <div class="payment__part">Оплатити частинами</div>
              </div>
            </div>
          </td>
          <td class="item__status-premium">
            <div class="plan__top top">
              <div class="top__title title">
                <div class="title__name">Преміум</div>
                <div class="title__discount discount">-75%</div>
              </div>
              <div class="top__description">8 професійних курсів за ціною 2 +<br> бухгалтерська відеоплатформа №1</div>
              <div class="top__price price">
                <div class="price__old">1079 грн/міс.</div>
                <div class="price__new">679 грн/міс.</div>
              </div>
              <div class="top__payment payment">
                <div class="payment__card"><v-button>Оплатити карткою</v-button></div>
                <div class="payment__part">Оплатити частинами</div>
              </div>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
              Поглиблені професійні курси підвищення кваліфікації <span class="h-focus">(8 курсів/рік)</span>
          </td>
          <td class="item__status-superpro">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
              </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
            <div class="mark-new">NEW</div>
            <div class="content__description">Практичні курси автоматизації (робота в BAS, Medoc, Excel, ЕК)</div>
          </td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
            <div class="mark-new">NEW</div>
            <div class="content__description">Закриті клубні лекції з експертами <span class="h-focus">(1 р./ міс.)</span></div>
          </td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
            Майстер-класи зі змін у законодавстві <span class="h-focus">(4+ р./міс.)</span>
          </td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Безлімітні відповіді на запитання під час онлайн-навчання</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
            Тестові та практичні завдання зі зворотним зв'язком
          </td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">
            Роздатковий матеріал (корисні файли, брошури, презентації)
          </td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Клуб однодумців у Viber та підтримка куратора</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Сертифікати після проходження курсів</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M14.0648 21.8668L8.73145 16.5335L10.5981 14.6668L14.0648 18.1335L22.8648 9.3335L24.7314 11.2002L14.0648 21.8668Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Доступ до <span class="focus-bold">Бухгалтерської Відеоплатформи №1:</span></td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Відеокурси і вебінари <span class="h-focus">(1100+ вже та 20+ щомісяця)</span></td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Безлімітні швидкі консультації від експертів (сервіс ОК)</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Бланки та зразки документів <span class="h-focus">(2000+ вже та 30+ щомісяця)</span></td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Консультант з пошуку та підготовки документів <span class="h-focus">(безлімітно, щодня)</span></td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Калькулятори</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">Довідники</td>
          <td class="item__status-superpro">
            <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
              <path d="M24.3378 10.2736L22.4578 8.39355L16.7312 14.1202L11.0045 8.39355L9.12451 10.2736L14.8512 16.0002L9.12451 21.7269L11.0045 23.6069L16.7312 17.8802L22.4578 23.6069L24.3378 21.7269L18.6112 16.0002L24.3378 10.2736Z" fill="#232323"/>
            </svg>
          </td>
          <td class="item__status-premium">
            <div class="padding">
              <svg xmlns="http://www.w3.org/2000/svg" width="33" height="32" viewBox="0 0 33 32" fill="none">
                <path d="M14.0645 21.8668L8.7312 16.5335L10.5979 14.6668L14.0645 18.1335L22.8645 9.3335L24.7312 11.2002L14.0645 21.8668Z" fill="#232323"/>
              </svg>
            </div>
          </td>
        </tr>
        <tr class="list__item item">
          <td class="item__title">&nbsp;</td>
          <td class="item__status-superpro">
            <div class="plan__bottom bottom">
              <div class="bottom__price price">
                <div class="block-price">
                  <div class="price__old">1079 грн/міс.</div>
                  <div class="price__new">679 грн/міс.</div>
                </div>
                <div class="price__discoun discount">
                  -75%
                </div>
              </div>
              <div class="bottom__invoice">
                <v-button>Завантажити рахунок</v-button>
              </div>
            </div>
          </td>
          <td class="item__status-premium">
            <div class="plan__bottom bottom">
              <div class="bottom__price price">
                <div class="block-price">
                  <div class="price__old">1079 грн/міс.</div>
                  <div class="price__new">679 грн/міс.</div>
                </div>
                <div class="price__discoun discount">
                  -75%
                </div>
              </div>
              <div class="bottom__invoice">
                <v-button>Завантажити рахунок</v-button>
              </div>
            </div>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.tariff__plans{
  margin-top: 80px;
  .plans__list{
  
    .list{
      width: 1035px;
      padding: 16px 32px;
      border-collapse: collapse;
      border-spacing: 0;
      @media screen and (max-width: 1000px) {
        width: 100%;
      }
      .list__item{
        display: flex;
        align-items: center;
        border-bottom: 1px solid rgba($color-black-content, 0.10);
        &:first-child{
          border-bottom: 0;
          .item__status-premium{
            border-top-right-radius: 19px;
            border-top-left-radius: 19px;
            border-top: 2px solid $color-blue-primary;
          }
        }
        &:last-child{
          border-bottom: 0;
          .item__status-premium{
            border-bottom-right-radius: 19px;
            border-bottom-left-radius: 19px;
            border-bottom: 2px solid $color-blue-primary;
          }
        }
        .item__title{
          width: 100%;
          font-family: 'Raleway', sans-serif;
          font-size: 15px;
          font-weight: 500;
          line-height: 140%;
          .component-timer{
            width: 225px;
            margin-top: -70px;
            margin-left: 48px;
            .tariff__timer{
              margin: 0;
              margin-bottom: 14px;
            }
            .timer-title{
              text-align: center;
              font-family: 'Raleway', sans-serif;
              font-size: 15px;
              font-weight: 400;
              line-height: 150%; /* 22.5px */
              letter-spacing: -0.12px;
              color: #515154;
            }   
          }
        }
        .item__status-premium{
          border-right: 2px solid $color-blue-primary;
          border-left: 2px solid $color-blue-primary;
          padding: 0 29px;
          .padding{
            padding: 8px 0;
          }
        }
        .item__status-superpro{
          padding: 0 29px;
          .hit-sale{
            width: 100%;
            top:-30px;
            left: 0;
            position: absolute;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 13px;
      
            text-transform: uppercase;
            font-family: 'Raleway', sans-serif;
            padding: 5px 0;
            font-size: 14px;
            font-weight: 700;
            line-height: 110%;

            border-radius: 15px 15px 0px 0px;
            background: #FFE601;
          }
        }
        td:nth-last-child(-n+2){
          width: 100%;
          text-align: center;
        }
      }
      .plan__top{
        position: relative;
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-top: 9px;
        padding-bottom: 40px;
        .top__title{
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 4px;
            line-height: 150%;
            .title__name{
              text-transform: uppercase;
              font-family: 'Raleway',sans-serif;
              font-size: 13px;
              font-weight: 700;
    
            }
        }
        .top__description{
          margin-bottom: 12px;
          text-align: center;
          font-family: 'Raleway', sans-serif;
          font-size: 13px;
          font-weight: 500;
          line-height: 150%; /* 19.5px */
          text-transform: lowercase;
        }
        .top__price{
          display: flex;
          flex-direction: column;
          align-items: center;
          gap: 5px;
 
        }
        .top__payment{
          display: flex;
          flex-direction: column;
          align-items: center;
     
          .payment__card{
            margin: 12px;
          }
          .payment__part{
            color: $color-grey-light;
            font-family: 'Raleway', sans-serif;
            font-size: 13px;
            font-weight: 400;
            line-height: normal;
            text-decoration-line: underline;
          }
        }
        .focus-bold{
          color: $color-blue-primary;
          font-weight: 700;
        }
        .v-button{
            padding: 16px 40px;
        }
      }
      .plan__bottom{
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-top: 40px;
        padding-bottom: 18px;
        .bottom__price{
          display: flex;
          align-items: center;
          margin-bottom: 12px;
          gap: 26px;
          .block-price{
            display: flex;
            flex-direction: column;
            gap: 5px;
          }
        }
      }
    }
    .discount{
          height: 34px;
          width: 34px;
          display: flex;
          align-items: center;
          justify-content: center;
          font-family: 'inter', sans-serif;
          font-size: 10px;
          font-weight: 700;
          border-radius: 17px;
          color: $color-white-background;
          background: $color-blue-primary;
    }
    .price__old{
              color: $color-grey-light;
              font-family: 'Raleway',sans-serif;
              font-size: 13px;
              font-weight: 400;
              line-height: normal;
              text-decoration-line: line-through;
    }
    .price__new{
              font-family: 'Raleway',sans-serif;
              font-size: 17px;
              font-weight: 700;
              line-height: normal;
    }
    .mark-new{
        display: flex;
        margin-top: 2px;
        margin-right: 8px;    
        float: left;
        padding: 3px 5px;
        
        font-family: 'Raleway', sans-serif;
        font-size: 16px;

        font-weight: 600;
        line-height: 80%;
        border-radius: 3px;
        color: $color-background;
        background: $color-blue-primary;
    }
    .focus-bold{
        color: $color-blue-primary;
        font-weight: 700;
    }
    .v-button{
          padding: 16px 40px;
          white-space: nowrap;
    }
  }
}
</style>