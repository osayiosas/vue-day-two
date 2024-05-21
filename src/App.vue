<script setup>
import ViewModelVue from './components/ViewModel.vue'
import StaticProps from './components/StaticProps.vue'
import DynamicPropsVue from './components/DynamicProps.vue'

import { ref } from 'vue'

const firstName = ref('idiaghe')
const lastName = ref('osayi')

const myFavoriteNumber = ref(10)

import ChangePropsValueVue from './components/ChangePropsValue.vue'

import PropsVaildation from './components/PropsVaildation.vue'

import ComplexProps from './components/ComplexProps.vue'

import CustomVaildator from './components/CustomVaildator.vue'
import ComponentEvent from './components/ComponentEvent.vue'



let count = ref (0)

import FormComponent from './components/FormComponent.vue'

const formHandler = (username, email, password) => {
  console.log('username: ',username)
  console.log('email: ',email)
  console.log('password:', password)

}

import SlotMethods from './components/SlotMethods.vue'

import FallbackContent from './components/FallbackContent.vue'

import NameSlotComponent from './components/NameSlotComponent.vue'
</script>

<template>
  <ViewModelVue />

  <StaticProps name="Osayi" />

  <DynamicPropsVue :firstName="firstName" :lastName="lastName" />
  <hr />
  <ChangePropsValueVue :myFavoriteNumber="myFavoriteNumber" />

  <PropsVaildation fullName="Osaigbovo idiaghe" :age="20" :Country="Nigeria" />

  <ComplexProps
    :friends="['Ola', 'Osayi', 'joan', 'Ernest']"
    :userInfo="{
      name: 'Ola',
      age: 20,
      country: ['Nigeria']
    }"
  />

  <CustomVaildator name="Osaigbovo" :age="20" password="Immpossible" />
  <hr />
  <h1>count: {{ count }}</h1>
  <ComponentEvent @IncremenrtCounter="count++" />

  <hr>

  <FormComponent @userInfo="formHandler" />

  <hr>

  <SlotMethods>
    <h1>conent 1</h1>
  </SlotMethods>

  <hr>

  <FallbackContent>
  </FallbackContent>

  <hr>

  <FallbackContent>
    <h1> This is the fallback component content</h1>
  </FallbackContent>

  <hr>

  <NameSlotComponent>
    <!-- v-slot:0ne -->
    <template v-slot:one>
      <h1> This is the first slot</h1>
    </template >
    <!-- #two  -->

     <template #two>
      <h1> This is the second slot</h1>
    </template >
  </NameSlotComponent>

  
</template>
