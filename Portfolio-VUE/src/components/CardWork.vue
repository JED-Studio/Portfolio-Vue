

<script setup>

const props = defineProps({
  title: String,
  description: String,
  imageUrl: String,
  stack_list_title: String,
  stack_list: String,
  links: String
 
})

</script>

<template>
     <div class="item flex flex-col rounded-lg" style="box-shadow: 0 3px 6px rgba(0, 0, 0, .16), 0 3px 6px rgba(0, 0, 0, .23); background-color: #202020; overflow: hidden;">
          <img :src="imageUrl" alt="">
          <div class="p-6">
          <h3 class="mb-4 font-black text-2xl leading-tight">{{ title }}</h3>
          <p>{{ description }}
          </p>
          <div class="my-5" style="background-color: #7f5af0; padding: 1px;"></div>
          <h4 class="mb-4 font-black text-2xl leading-tight">{{ stack_list_title }}</h4>
            <ul >
              <li class="">{{ stack_list }}</li>
              <li class="">{{ links }}</li>
              <li class="">{{ links1 }}</li>
              <li class="">{{ links2 }}</li>
              <li class="">{{ links3 }}</li>
              <li class="">{{ links4 }}</li>
            </ul>
          </div>
        </div>
</template>

<style scoped>
li{
  
  margin-left: 19px ;
  list-style: square;
}


</style>