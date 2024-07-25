

<script>
export default {
  name: 'CardWork',
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}




</script>

<template>
     <div class="item flex flex-col rounded-lg" style="box-shadow: 0 3px 6px rgba(0, 0, 0, .16), 0 3px 6px rgba(0, 0, 0, .23); background-color: #202020; overflow: hidden;">
          <img :src="item" alt="">
          <div class="p-6">
          <h3 class="mb-4 font-black text-2xl leading-tight"></h3>
          <p>
          </p>
          <div class="my-5" style="background-color: #7f5af0; padding: 1px;"></div>
          <h4 class="mb-4 font-black text-2xl leading-tight"></h4>
            <ul >
              <li class=""><span></span></li>
              <li class="" ><span></span></li>
              <li class="" ><span></span></li>
              <li class="" ><span></span></li>
              <li class="" ><span></span></li>
              <li class="" ><span></span></li>
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