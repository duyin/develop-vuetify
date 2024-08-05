<template>
 <div>
    <v-select
          :items="items"
          label="Solo field"
          solo
        ></v-select>
        <v-alert
  color="red"
  type="success"
  v-if="isShow"
>successful</v-alert>
 </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      items: ['Foo', 'Bar', 'Fizz', 'Buzz'],
      isShow:false,
    }),
    mounted(){
      setTimeout(()=>{
        this.isShow = true;
      },2000)
    }
  }
</script>
