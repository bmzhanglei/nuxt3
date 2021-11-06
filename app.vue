<template>
 <div class="app-main">


   <h1>Hello World!</h1>
    <Head :lang="dynamic > 50 ? 'en-GB' : 'en-US'">
      <Title>{{ dynamic }} title</Title>
      <Meta name="description" :content="`My page's ${dynamic} description`" />
    
    </Head>
     <NuxtPage/>
 </div>

  

</template>

<script lang='ts' setup>
const dynamic = 80
let meta = useMeta({
  meta: [
        { name: 'viewport', content: 'width=device-width, initial-scale=1, maximum-scale=1' }
      ],
      bodyAttrs: {
        class: 'test'
      }
})



</script>
