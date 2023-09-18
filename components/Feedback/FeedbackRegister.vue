<template>
  <div class="feedback__register">
    <div class="register__title">Залиште заявку, і ми підберемо для вас умови зі знижкою</div>
    <form class="register__form" @submit.prevent="submitForm()">
      <v-input 
        v-model="formData.name" 
        type="text" 
        placeholder="Ваше і'мя" 
        label="Ваше ім’я"
        :isValid="isNameValid"
        :errorMessage="nameErrorMessage"
        @input="validateName()"
        ></v-input>
      <v-input 
        v-model="formData.phone" 
        type="text" 
        placeholder="Введіть Ваш номер телефону" 
        label="Номер телефону"
        :isValid ="isPhoneValid"
        :errorMessage="phoneErrorMessage"
        @input="validatePhone()"
        />
      <v-input 
        v-model="formData.email" 
        type="text" 
        placeholder="Введіть Ваш e-mail" 
        label="Ваш e-mail"
        :isValid="isEmailValid"
        :errorMessage="emailErrorMessage"
        @input="validateEmail()"
        />
        <div class="submit">  
          <v-button type="submit" buttonClass="default">Зареєструватись</v-button>
          <div v-if="statusSubmit" class="status-submit">{{statusSubmit}}</div>
        </div>
    </form>
  </div>

</template>

<script setup>
const statusSubmit=ref(null);
const formData = reactive({
  name: '',
  phone: '',
  email: '',
});

const isNameValid = ref(false);
const isPhoneValid = ref(false);
const isEmailValid = ref(false);
const nameErrorMessage = ref('');
const phoneErrorMessage = ref('');
const emailErrorMessage = ref('');
function checkValidationForm(){
  validateName()
  validatePhone()
  validateEmail()
}
function validateName() {
  const nameRegex = /^[A-Za-zА-ЯЁІЇЄа-яёіїє][a-zа-яёіїє'’]*$/;
    if (formData.name == ''){
      nameErrorMessage.value = 'Поле не може бути пустим';
      isNameValid.value = false;
    }
    else if (!nameRegex.test(formData.name)) {
      nameErrorMessage.value = 'Ім\'я введено некоректно';
      isNameValid.value = false;
    } else {
      nameErrorMessage.value = '';
      isNameValid.value = true;
    }
};
function validatePhone() {
  const phoneRegex = /^\+?\d{7,15}$/;
    if (formData.phone == ''){
      phoneErrorMessage.value = 'Поле не може бути пустим';
      isPhoneValid.value = false;
    }
    else if (!phoneRegex.test(formData.phone)) {
      phoneErrorMessage.value = 'Дані некоректні. Від 7 до 15 цифр';
      isPhoneValid.value = false;
    } else {
      isPhoneValid.value = true;
      phoneErrorMessage.value = '';
    }
};
function validateEmail() {
  const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
    if (formData.email == ''){
      emailErrorMessage.value = 'Поле не може бути пустим';
      isEmailValid.value = false;
    }
    else if (!emailRegex.test(formData.email)) {
      emailErrorMessage.value = 'Дані некоректні. Приклад qwerty@gmail.com';
      isEmailValid.value = false;
    } else {
      isEmailValid.value = true;
      emailErrorMessage.value = '';
    }
};
async function submitForm() {
  checkValidationForm()
  if( isNameValid.value && isPhoneValid.value && isEmailValid.value)
  {
    try {
      const response = await fetch('https://7eminar.ua/api/clients/campaign/test', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json;charset=utf-8',
        },
        body: JSON.stringify(formData),
      })
      if (response.ok) {
        statusSubmit.value='Дані успішно надіслані';
        formData.name = formData.phone = formData.email = '';
      } else {
        statusSubmit.value='Не вдалося надіслати дані';
      }
      console.log('Response:', response);
    } catch (error) {
        console.error('Error:', error);
        statusSubmit.value='Ошибка';
    }finally{
      setTimeout(() => {
        statusSubmit.value = null;
      }, 5000);
    }
  }
}
</script>

<style lang="scss" scoped>
  .feedback__register{
    @media screen and (min-width: 500px) {
      padding: 0 24px;
    }
    .register__title{
      font-family: "eUkraineHead", sans-serif;
      font-size: 24px;
      width: 100%;
      font-weight: 600;
      line-height: 140%;
      @media screen and (min-width: 500px) {
          font-size: 23px;
          max-width: 490px;
      }
    }
    .register__form{
      max-width: 350px;
      display: flex;
      flex-direction: column;
      margin-top: 24px;
      gap: 16px;
      @media screen and (min-width: 500px) {
         max-width: 490px;
      }
      @media screen and (min-width: 1200px) {
         max-width: 1000%;
      }
      
      .submit{
        margin-top: 8px;
        display: flex;
        align-items: center;
        .status-submit{
          margin-left: 15px;
        }
        .v-button{
        width: max-content;
   
        }
      }
    }
  }
</style>