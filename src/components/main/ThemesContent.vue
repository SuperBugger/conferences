<template>
  <div class="themes-block" id="themes">
    <div class="themes-title-block">
      <div class="title">
        <div class="line"></div>
        <p class="themes-title">ПРОГРАММА КОНФЕРЕНЦИИ</p>
        <div class="line"></div>
      </div>
    </div>
    <div class="accordion-box">
      <div v-for="(item, index) in items" :key="index" class="accordion-block">
        <div class="accordion" @click="toggle(index)">
          <div class="accordion-header">
            <h3 class="accordion-title">{{ item.title }}</h3>
            <i :class="['arrow', {'arrow-down': activeIndex === index}]"></i>
          </div>
          <transition name="fade">
            <div class="accordion-content" :class="{ 'open': isActive(index) }" v-show="isActive(index)">
              <div class="dividing-line"></div>
              <div class="accordion-divider"></div>
              <div class="accordion-inner-content">
                <div class="accordion-row" v-for="(block, blockIndex) in item.blocks" :key="blockIndex">
                  <span class="bullet fst-bullet"></span>
                  <div class="accordion-text">
                    <p class="block-title">{{ block.fst_block_title }}</p>
                    <p class="text">{{ block.content }}</p>
                  </div>
                </div>
              </div>
              <!--                <div class="accordion-row">
                <span class="bullet"></span>
                <img v-for="(image, imageIndex) in item.images" :src="require(`../../imgs/${image}`)" :key="imageIndex" class="accordion-image" alt="Image">
              </div>-->
              <!--                <div class="accordion-row">
                                <span class="bullet"></span>
                                <iframe class="map" src="https://yandex.ru/map-widget/v1/?um=constructor%3Aab872f6b37c0768ce203e0e7e56339d074c6012579d529f8bdf75a6b8449d312&amp;source=constructor"></iframe>
                              </div>-->
            </div>
          </transition>
        </div>
      </div>
    </div>
    <div class="cover"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: -1,
      items: [
        {
          title: '10:00 - 10:10 – Прибытие и регистрация участников Пленарного заседания'
        },
        {
          title: '10:10 - 10:30 – Вступительное слово',
          blocks: [
            {
              fst_block_title: 'Магомедов Шамиль Гасангусейнович',
              content: 'Заместитель директора Института кибербезопасности и цифровых технологий РТУ МИРЭА по проектной работе, заведующий кафедрой «Интеллектуальные системы информационной безопасности», кандидат технических наук, доцент, победитель гранта Президента РФ среди молодых ученых кандидатов наук, директор Инжинирингового центра мобильных решений РТУ МИРЭА'
            },
            {
              fst_block_title: 'Аноприенко Александр Яковлевич',
              content: 'Ректор Донецкого национального технического университета, кандидат технических наук, доцент'
            },
            {
              fst_block_title: 'Покусов Виктор Владимирович',
              content: 'Генеральный директор ТОО «Национальный инновационный центр», председатель ОЮЛ «Казахстанская ассоциация информационной безопасности», член Совета по вопросам обеспечения кибербезопасности Республики Казахстан, член экспертного совета при Совете Безопасности Республики Казахстан по актуальным вопросам информационной безопасности, член общественного совета Министерства цифрового развития, инноваций и аэрокосмической промышленности Республики Казахстан'
            },
            {
              fst_block_title: 'Труфанов Владимир Николаевич',
              content: 'Заместитель директора ФГАНУ «Центр информационных технологий и систем органов исполнительной власти имени А.В. Старовойтова»'
            }
          ]
        },
        {
          title: '10:30 - 10:45 – Вектор развития методологии информационной безопасности в условиях цифровой трансформации общества и государства',
          blocks: [
            {
              fst_block_title: 'Максимова Елена Александровна',
              content: 'Председатель программного комитета конференции, профессор кафедры «Информационно-аналитические системы кибербезопасности» Института кибербезопасности и цифровых технологий РТУ МИРЭА, доктор технических наук, доцент'
            }
          ]
        },
        {
          title: '10:45 - 11:00 – Миллионеры из трущоб. Исследование АРТ-группировки',
          blocks: [
            {
              fst_block_title: 'Галкин Николай Николаевич',
              content: 'Руководитель направления исследования киберугроз «Перспективный мониторинг»'
            },
            {
              fst_block_title: 'Хромова Анна Владимировна',
              content: 'Руководитель направления исследования информационного пространства «Перспективный мониторинг»'
            }
          ]
        },
        {
          title: '11:00 - 11:15 – Основные техники социальной инженерии: виды атак и способы и предотвращения',
          blocks: [
            {
              fst_block_title: 'Горин Денис Станиславович',
              content: 'Заместитель директора Института кибербезопасности и цифровых технологий РТУ МИРЭА по работе со студентами, заведующий кафедрой «Разработка программных решений и системное программирование», кандидат экономических наук, доцент'
            }
          ]
        },
        {
          title: '11:15 - 11:30 – Современные подходы к построению Центра мониторинга кибербезопасности',
          blocks: [
            {
              fst_block_title: 'Устюжанин Андрей Алексеевич',
              content: 'Руководитель центра мониторинга и кибербезопасности ГК АО «ДОМ.РФ»'
            }
          ]
        },
        {
          title: '11:30 - 11:45 – Интеграция кибербезопасности в системы сервиса',
          blocks: [
            {
              fst_block_title: 'Седов Олег Витальевич',
              content: 'Директор по развитию ООО «Ростелеком-Солар»'
            }
          ]
        },
        {
          title: '11:45 - 12:00 – Последствия целевой атаки на оператора мобильной связи современной',
          blocks: [
            {
              fst_block_title: 'Смирнов Станислав Игоревич',
              content: 'Доцент кафедры «Интеллектуальные системы информационной безопасности» Института кибербезопасности и цифровых технологий РТУ МИРЭА, кандидат технических наук'
            }
          ]
        },
        {
          title: '12:00 - 12:15 – Риски и методы защиты данных в цифровом пространстве',
          blocks: [
            {
              fst_block_title: 'Адеева Кристина Викторовна',
              content: 'Менеджер по информационной безопасности ГК «Элемент»'
            }
          ]
        },
        {
          title: '12:15 - 12:30 – Комплексные решения для минимизации внутренних угроз кибербезопасности',
          blocks: [
            {
              fst_block_title: 'Морозов Виктор Егорович',
              content: 'Специалист компании ООО «Либрасофт», кандидат психологических наук, доцент'
            }
          ]
        },
        {
          title: '12:30 - 12:45 – Практико-ориентированная подготовка специалистов по разработке безопасного программного обеспечения в интересах создания Ассоциации организаций по оценке соответствия требованиям информационной безопасности АООСТИБ)',
          blocks: [
            {
              fst_block_title: 'Соболев Дмитрий Владимирович',
              content: 'Генеральный директор АО «Национальный инновационный центр»'
            },
            {
              fst_block_title: 'Трубиенко Олег Владимирович',
              content: 'Заведующий кафедрой «Информационно-аналитические системы кибербезопасности» Института кибербезопасности и цифровых технологий РТУ МИРЭА, кандидат технических наук, доцент'
            }
          ]
        },
        {
          title: '12:45 - 13:00 – Лучшие практики решения проблем с кадровым голодом в отрасли',
          blocks: [
            {
              fst_block_title: 'Дворянский Александр Евгеньевич',
              content: 'Директор по информационной безопасности ГК «Элемент»'
            }
          ]
        },
        {
          title: '13:00 - 13:15 – Торжественное закрытие пленарного заседания'
        }
      ]
    };
  },
  methods: {
    toggle: function(index) {
      this.activeIndex = this.activeIndex === index ? -1 : index;
    },
    isActive: function(index) {
      return this.activeIndex === index;
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');

.themes-block{
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 1080px;
  height: 100%;
  background-image: url('../../imgs/elearning-internet.jpg');
  overflow: hidden;
  border-radius: 40px;
  box-shadow: 0 10px 30px 0 #153A4B;
}

.cover{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #153A4B;
  z-index: 1;
  opacity: 0.9;
}

.themes-title-block {
  height: auto;
  max-width: 1100px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: transparent;
  margin: 0 auto;
}

.title {
  margin-top: 110px;
  width: 100%;
  z-index: 2;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 50px;
}

.themes-title {
  color: #ffffff;
  font-size: 24px;
  margin: 0;
  font-family: "Inter Tight", sans-serif;
  white-space: nowrap;
}

.line {
  height: 1px;
  background-color: #ffffff;
  margin: 0 50px 0 50px;
  flex-grow: 1;
}

.dividing-line{
  height: 1px;
  background-color: #085578;
  flex-grow: 1;
  opacity: 0.2;
}

.accordion-divider {
  position: absolute;
  left: 30px;
  top: 35px;
  bottom: 30px;
  width: 1px;
  height: calc(100% - 65px);
  background-color: #83AABB;
}

.bullet {
  display: inline-block;
  width: 11px;
  height: 11px;
  border-radius: 50%;
  background-color: white;
  border: 1px solid #83AABB;
  margin-left: 24px;
  margin-right: 5px;
  flex-shrink: 0;
}

.fst-bullet{
  margin-top: 4px;
}

.accordion-box{
  height: auto;
  max-width: 1100px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: transparent;
  margin: 0 auto 110px;
  position: relative;
  z-index: 2;
}

.accordion-block{
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 16px;
}

.accordion {
  width: calc(100% - 100px);
  background-color: white;
  border-radius: 16px;
}

.accordion:hover {
  background-color: #f0f0f0;
}

.accordion-header {
  margin-left: 30px;
  margin-right: 30px;
  display: flex;
  justify-content: space-between;
}

.arrow {
  background-image: url('../../imgs/icons8-down-button-32.png');
  width: 32px;
  height: 32px;
  margin: 30px 0 30px 0;
}

.arrow-down {
  transform: rotate(180deg);
}

.accordion-content {
  position: relative;
}

.accordion-inner-content{
  position: relative;
  display: flex;
  flex-direction: column;
  margin: 30px 30% 8px 0;
}

.accordion-row{
  display: flex;
  margin-bottom: 22px;
}

.accordion-title {
  font-size: 24px;
  font-family: "Inter Tight", sans-serif;
  font-weight: normal;
  width: calc(100% - 50px);
  margin: 30px 0 30px 0;
}

.accordion-text {
  margin: 0 0 0 30px;
}

.block-title{
  margin: 0;
  font-size: 18px;
  font-family: "Inter Tight", sans-serif;
}

.text{
  margin-top: 8px;
  margin-bottom: 0;
  font-size: 16px;
  font-family: "Inter Tight", sans-serif;
  opacity: 0.5;
}

.accordion-image {
  margin-left: 30px;
  max-height: 200px;
}

.map{
  margin-left: 30px;
  border: white;
}

@media (max-width: 430px) {
  .accordion-title{
    font-size: 16px;
    margin: 20px 0 20px 0;
  }
  .themes-title{
    font-size: 23px;
  }
  .accordion-header{
    margin-left: 20px;
    margin-right: 20px;
  }
  .accordion-inner-content{
    width: calc(100% - 35px);
  }
  .arrow{
    margin: auto 0 auto auto;
  }
}
</style>