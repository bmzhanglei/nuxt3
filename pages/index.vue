<template>
<div>
    <TheHeader/>
 index  <br> 
 <NuxtLink to="/detail">detail</NuxtLink>  <br>
 <NuxtLink to="/users-admin/6">admin/1</NuxtLink><br>
 <NuxtLink to="/parent/child">parent</NuxtLink><br>

 <TheFooter/>
 </div>
</template>

<script lang='ts'>
import TheHeader from "~~/components/TheHeader.vue";
export default{
    name: "index",
    components: { TheHeader }
}
</script>