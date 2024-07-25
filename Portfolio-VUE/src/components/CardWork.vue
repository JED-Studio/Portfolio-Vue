

<script setup>

const props = defineProps({
  title: String,
  description: String,
  imageUrl: String,
  stack_list_title: String,
  stack_list: String,
  links: { type: String, default: '' },
  links1: { type: String, default: '' },
  links2: { type: String, default: '' },
  links3: { type: String, default: '' },
  links4: { type: String, default: '' }
})

</script>

<template>
     <div class="item flex flex-col rounded-lg" style="box-shadow: 0 3px 6px rgba(0, 0, 0, .16), 0 3px 6px rgba(0, 0, 0, .23); background-color: #202020; overflow: hidden;">
      <div class="w-full max-w-md">
          <img :src="imageUrl" alt="" loading="lazy">
      </div>
          <div class="p-6">
          <h3 class="mb-4 font-black text-2xl leading-tight">{{ title }}</h3>
          <p>{{ description }}
          </p>
          <div class="my-5" style="background-color: #7f5af0; padding: 1px;"></div>
          <h4 class="mb-4 font-black text-2xl leading-tight">{{ stack_list_title }}</h4>
            <ul >
              <li class=""><span>{{ stack_list }}</span></li>
              <li class="" v-if="links"><span>{{ links }}</span></li>
              <li class="" v-if="links1"><span>{{ links1 }}</span></li>
              <li class="" v-if="links2"><span>{{ links2 }}</span></li>
              <li class="" v-if="links3"><span>{{ links3 }}</span></li>
              <li class="" v-if="links4"><span>{{ links4 }}</span></li>
            </ul>
          </div>
        </div>
</template>

<style scoped>
span{
  color: white;
}

li{
  color: #7f5af0;
  margin-left: 19px ;
  list-style: square;
}


</style>