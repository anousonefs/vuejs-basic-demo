<template>
  <div id="footer" class="footer">
      <span :style="{color}">{{title}}</span>
  </div>
</template>

<script>
export default {
    name:"Footer",

    mounted(){
        setInterval(()=>{
            this.$emit("onClock", Date())
        },100)
    },

    props:[
        "title",
        "color"
    ]

}
</script>

<style>
.footer{
    font-size: 12px;
    color:black;
    padding-top: 20px;
}
</style>