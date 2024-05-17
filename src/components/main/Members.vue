<template>
  <div class="members-block" id="members">
    <div class="members-title-block">
      <div class="line"></div>
      <p class="members-title">УЧАСТНИКИ</p>
      <div class="line"></div>
    </div>
    <div class="company-cards">
      <div v-for="(company, index) in companies" :key="index" class="company-card">
        <img :src="require(`../../imgs/${company.logo}`)" :alt="company.name" class="company-logo">
        <h3 class="company-card-title">{{ company.name }}</h3>
        <p class="company-card-description">{{ company.description }}</p>
      </div>
    </div>
    <div class="speaker-cards">
      <div v-for="(speaker, index) in speakers" :key="index" class="speaker-card">
        <img :src="require(`../../imgs/${speaker.photo}`)" :alt="speaker.name" class="speaker-photo">
        <div class="speaker-info">
          <div class="speaker-divider"></div>
          <h3 class="speaker-name">{{ speaker.name }}</h3>
          <p class="speaker-description">{{ speaker.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      companies: [
        {
          name: 'Компания 1',
          description: 'Описание компании 1 Описание компании 1 Описание компании 1 Описание компании 1 Описание компании 1 Описание компании 1 Описание компании 1 ',
          logo: 'MIREA_Gerb_Colour.png'
        },
        {
          name: 'Компания 2',
          description: 'Описание компании 2 Описание компании 2 Описание компании 2 Описание компании 2 Описание компании 2 ',
          logo: 'MIREA_Gerb_Colour.png'
        },
        {
          name: 'Компания 3',
          description: 'Описание компании 3 Описание компании 3 Описание компании 3 Описание компании 3 Описание компании 3 Описание компании 3 ',
          logo: 'MIREA_Gerb_Colour.png'
        },
      ],
      speakers: [
        {
          name: 'Кузьмин Геннадий Васильевич',
          description: 'Советник генерального директора АО «Научно-исследовательский институт' +
              ' точных приборов», д.т.н., профессор',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Магомедов Шамиль Гасангусейнович',
          description: 'Заведующий кафедрой «Интеллектуальные системы информационной' +
              ' безопасности» Института кибербезопасности и цифровых технологий РТУ МИРЭА, к.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Горин Денис Станиславович',
          description: 'Заместитель директора по воспитательной ' +
              'работе, заведующий кафедрой «Разработка программных решений и системное ' +
              'программирование» Института кибербезопасности и цифровых технологий РТУ ' +
              'МИРЭА, к.э.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        /*{
          name: 'Матвеев Александр Владимирович',
          description: 'Заведующий кафедрой прикладной \n' +
              'математики и информационных технологий, Санкт-Петербургский университет \n' +
              'Государственной противопожарной службы МЧС России имени Героя \n' +
              'Российской Федерации генерала армии Е.Н. Зиничева, главный редактор научно-аналитического журнала «Вестник Санкт-Петербургского университета ГПС \n' +
              'МЧС России» г. Санкт-Петербург, к.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Трубиенко Олег Владимирович',
          description: 'Заведующий кафедрой «Информационно-аналитические системы кибербезопасности» Института кибербезопасности и \n' +
              'цифровых технологий РТУ МИРЭА, к.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Артемова Светлана Валерьевна',
          description: 'Заведующий кафедрой «Защита \n' +
              'информации» Института кибербезопасности и цифровых технологий РТУ \n' +
              'МИРЭА, д.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },{
          name: 'Иванова Ирина Алексеевна',
          description: 'Заведующий кафедрой «Цифровые технологии \n' +
              'обработки данных» Института кибербезопасности и цифровых технологий РТУ \n' +
              'МИРЭА, к.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },{
          name: 'Радченко Татьяна Викторовна',
          description: 'Заместитель заведующего кафедрой \n' +
              '«Правовое обеспечение национальной безопасности» Института \n' +
              'кибербезопасности и цифровых технологий РТУ МИРЭА, к.ю.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Глобенко Оксана Александровна',
          description: 'Заместитель директора по научной работе \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА, к.ю.н., \n' +
              'доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Ильягуева Алина Александровна',
          description: 'Доцент кафедры «Правовое обеспечение \n' +
              'национальной безопасности» Института кибербезопасности и цифровых \n' +
              'технологий РТУ МИРЭА, к.ю.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Максимова Елена Александровна',
          description: 'И.о. заведующего кафедрой «Предметно-ориентированные информационные системы», профессор кафедры \n' +
              '«Информационно-аналитические системы кибербезопасности» Института \n' +
              'кибербезопасности и цифровых технологий РТУ МИРЭА, д.т.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Макаров Константин Сергеевич',
          description: 'Заведующий кафедрой программного \n' +
              'обеспечения и администрирования информационных систем',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Аксенов Виктор Александрович',
          description: 'Заместитель начальника УВД на ММ ГУ \n' +
              'МВД России по г. Москве, полковник полиции',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Седов Олег Витальевич',
          description: 'Директор по развитию ООО «Ростелеком-Солар»',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Буйневич Михаил Викторович',
          description: 'Профессор кафедры прикладной математики\n' +
              'и информационных технологий Санкт-Петербургского университета ГПС МЧС \n' +
              'России, д.т.н., профессор',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Наумов Петр Николаевич',
          description: 'Ведущий научный сотрудник АО «Научно-исследовательский институт точных приборов», д.т.н., профессор',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Баранов Владимир Витальевич',
          description: 'Заведующий кафедрой информационной \n' +
              'безопасности Южно-Российского государственного политехнического \n' +
              'университета (НПИ) имени М.И. Платова, д.в.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Морозов Виктор Егорович',
          description: 'Специалист компании ООО «Либрасофт»,\n' +
              'к.психол.н., доцент',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Шмавонян Саркис Артушевич',
          description: 'Менеджер по работе с образовательными \n' +
              'организациями ООО «Киберпротект»',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Азерский Владислав Дмитриевич',
          description: 'Ведущий специалист по реагированию на \n' +
              'инциденты и цифровой криминалистике, компания F.A.C.C.T.',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Ковалев Анатолий Сергеевич',
          description: 'Руководитель безопасной разработки систем \n' +
              'ООО «Цифровые технологии»',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Устюжанин Андрей Алексеевич',
          description: 'Руководитель Центра мониторинга \n' +
              'кибербезопасности АО «ДОМ.РФ»',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Садыков Ильдар Венерович',
          description: 'Руководитель отдела экспертного обучения, \n' +
              'компания Positive Technologies',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Карельский Дмитрий Владимирович',
          description: 'Специалист по анализу защищённости, \n' +
              'компания Bi.Zone',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Смирнов Станислав Игоревич',
          description: 'Доцент кафедры «Интеллектуальные системы \n' +
              'информационной безопасности» Института кибербезопасности и цифровых \n' +
              'технологий РТУ МИРЭА, к.т.н.\n',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Карасёв Павел Игоревич',
          description: 'Доцент кафедры «Защита информации» Института \n' +
              'кибербезопасности и цифровых технологий РТУ МИРЭА, к.т.н.',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Алексеенко Анна Станиславовна',
          description: 'Старший преподаватель кафедры \n' +
              '«Информационно-аналитические системы кибербезопасности» Института \n' +
              'кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },{
          name: 'Котилевец Игорь Денисович',
          description: 'Старший преподаватель кафедры «Цифровые \n' +
              'технологии обработки данных» Института кибербезопасности и цифровых \n' +
              'технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Шутов Василий Александрович',
          description: 'Преподаватель кафедры «Защита \n' +
              'информации» Института кибербезопасности и цифровых технологий РТУ \n' +
              'МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Метелев Илья Александрович',
          description: 'Преподаватель кафедры «Защита \n' +
              'информации» Института кибербезопасности и цифровых технологий РТУ \n' +
              'МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },{
          name: 'Рязанцев Александр Витальевич',
          description: 'Преподаватель кафедры «Защита \n' +
              'информации» Института кибербезопасности и цифровых технологий РТУ \n' +
              'МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Самогин Артём Сергеевич',
          description: 'Ассистент кафедры «Правовое обеспечение \n' +
              'национальной безопасности» Института кибербезопасности и цифровых \n' +
              'технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Долженков Сергей Сергеевич',
          description: ' Ассистент кафедры «Разработка программных \n' +
              'решений и системное программирование» Института кибербезопасности и \n' +
              'цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },{
          name: 'Шаров Иван Михайлович',
          description: 'Младший программист ситуационного центра РТУ \n' +
              'МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Утенкова Мария Александровна',
          description: 'Председатель Студенческого научного \n' +
              'общества Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Палтаджян Сона Григорьевна',
          description: 'Член Студенческого научного общества \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Приймак Полина Александровна',
          description: 'Член Студенческого научного общества \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Симоненкова Екатерина Сергеевна',
          description: 'Член Студенческого научного общества \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Полянская Полина Алексеевна',
          description: 'Член Студенческого научного общества \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },
        {
          name: 'Москалев Илья Сергеевич',
          description: 'Член Студенческого научного общества \n' +
              'Института кибербезопасности и цифровых технологий РТУ МИРЭА',
          photo: 'Kudzh-S.A..jpg'
        },*/
      ]
    };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');
.members-block {
  min-height: 650px;
  height: 100%;
  max-width: 1220px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #FFFFFF;
  margin: 0 auto;
}

.members-title-block {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 70px;
  margin-top: 250px;
}

.members-title {
  color: #085578;
  font-size: 24px;
  margin: 0;
  font-family: "Inter Tight", sans-serif;
  white-space: nowrap;
}

.line {
  height: 1px;
  max-width: 327px;
  background-color: #085578;
  margin: 0 50px 0 50px;
  flex-grow: 1;
}

.speaker-divider {
  position: absolute;
  width: 2px;
  height: 100%;
  background-color: #085578;
}

.company-cards {
  display: flex;
  width: 100%;
  justify-content: center;
  margin: 0 50px 122px;
}

.company-card {
  max-width: 390px;
  width: 100%;
  min-height: 250px;
  border-radius: 20px;
  background-color: white;
  box-shadow: 5px 12px 20px 0px rgba(0, 0, 0, 0.1);
  margin-right: 25px;
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  padding: 20px;
}

.company-logo {
  width: 75px;
  height: auto;
}

.company-card-title{
  margin-top: 20px;
  margin-bottom: 0;
  font-size: 24px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
}

.company-card-description{
  margin-bottom: 0;
  margin-top: 9px;
  font-size: 14px;
  font-family: "Inter Tight", sans-serif;
  opacity: 0.5;
  width: 100%;
}
.speaker-cards {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  justify-content: space-around;
  margin: 0 50px 190px;
}

.speaker-card {
  max-width: 280px;
  width: 100%;
  min-height: 414px;
  background-color: transparent;
  margin-right: 25px;
  margin-bottom: 76px;
  display: flex;
  flex-direction: column;
  text-align: left;
  align-items: center;
}

.speaker-photo {
  width: 286px;
  height: auto;
  border-radius: 20px;
  margin-bottom: 20px;
}

.speaker-info{
  width: 100%;
  min-height: 125px;
  height: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
}

.speaker-name{
  font-size: 24px;
  font-family: "Inter Tight", sans-serif;
  font-weight: normal;
  margin: 0 0 0 16px;
}

.speaker-description{
  font-size: 14px;
  font-family: "Inter Tight", sans-serif;
  opacity: 0.5;
  margin-left: 16px;
}

@media (max-width: 1300px) {
  .company-cards{
    width: 90%;
  }
  .speaker-cards{
    width: 90%;
  }
}

@media (max-width: 430px) {
  .company-cards {
    flex-direction: column;
    width: 100%;
    align-items: center;
    margin: 0;
  }
  .company-card{
    max-width: 260px;
    margin: 30px 0 0 0;
  }
  .members-title-block{
    margin-bottom: 30px;
    margin-top: 100px;
  }
  .speaker-cards{
    margin-top: 120px;
  }
  .speaker-card{
    margin-right: 0;
  }
  .line{
    display: none;
  }
}
</style>