<script lang="ts" setup>
import {reactive} from "vue"
import type {Student} from "@/models/student"

const student:Student = reactive({
  name:'',
  lastName:'',
  email:'',
  sex: 'male',
  address: '',
  city: '',
  postal_code: 0,
  institute: ''
});

const validationRules = {
  name: (value:string) => value.trim() !== '',
  lastName: (value:string) => value.trim() !== '',
  email: (value:string) => /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/.test(value),
  sex: (value:'male' | 'female') => value !== 'male' && value !== 'female',
  address: (value:string) => value.trim() !== '',
  city: (value:string) => value.trim() !== '',
  postal_code: (value:number) => value !== 0,
  institute: (value:string) => value.trim() !== ''
};
const onSubmit = ()=>{
  const errors = {};
  Object.keys(validationRules).forEach((field, index: number) => {
  const fieldValue = Object.values(student)[index] as string | number;;
  const validationRule = Object.values(validationRules)[index] as (value: string | number) => boolean;
  if (!validationRule(fieldValue)) {
    Object.keys(errors)[index] = `Please enter your ${field}`;
  }
});
  if (Object.keys(errors).length > 0) {
    alert(Object.values(errors).join(', '));
  } else {
    alert('Form submitted successfully!');
    console.log(Object.values(student).map((value) => value).join(', '));
  }
};
</script>
<template>
  <form @submit.prevent="onSubmit">
    <label for="fname">Nom</label>
    <input type="text" id="lname" name="lastname" placeholder="Your last name.." v-model="student.lastName"/>
    <label for="lname">Prénom</label>
    <input type="text" id="fname" name="firstname" placeholder="Your first name.." v-model="student.name" required/>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" placeholder="Your email.." v-model="student.email" required/>
    <label for="">Sex</label>
    <br>
      <label for="sex_male">male</label>
      <input type="radio" id="sex_male" name="male" value="male" v-model="student.sex" required>
      <br>
      <label for="sex_female">female</label>
      <input type="radio" id="sex_female" name="male" value="female" v-model="student.sex" required>
    <br>
    <label for="address">Address</label>
    <input type="text" id="address" name="address" placeholder="Your last name.." v-model="student.address" required/>
    <label for="postal">Postal Code</label>
    <input type="text" id="postal" name="postal" placeholder="Your first name.." v-model="student.postal_code" required/>
    <label for="city">City</label>
    <input type="text" id="city" name="city" placeholder="Your City.." v-model="student.city" required/>
    <label for="institute">Institute Name</label>
    <input type="text" id="institute" name="institute" placeholder="Your Institute Name.." v-model="student.institute" required/>
      <button type="submit">Submit</button>
  </form>
</template>
<style scoped>
input[type='text'],
select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type='email'] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type='submit'] {
  width: 100%;
  background-color: #4caf50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type='submit']:hover {
  background-color: #45a049;
}

div {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}
</style>
