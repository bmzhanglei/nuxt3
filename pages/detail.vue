
<template>
<div>
  
detail page---{{foo}}
<!-- <ul><li v-for='(item,index) in d' :key='index'>{{item.login}}</li></ul> -->
</div>
</template>
<script lang="ts" setup>
import { useFoo } from '../composables/index';

interface User{
    avatar_url:string,
    login:string
}
type Tuser = Array<User> 
const dynamic= 20
// $fetch('/api/count').then(res=>{
//     console.log(res)
// })

const {data}= await useAsyncData('names', () => $fetch('/api/c.json'),{defer:false,server:false})

const foo = useFoo()


onMounted(()=>{
    console.log(data.value)
})
// const { data:userData } = await useFetch('https://api.github.com/users')
// const d = userData.value as Tuser
</script>
