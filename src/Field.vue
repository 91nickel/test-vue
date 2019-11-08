<template>
  <div>
    <h3>{{msg}}</h3>
    <input type="text" :value="msg" v-on:input="changeMess">
    <p>{{ mess }}</p>
  </div>
</template>

<script>
    export default {
        props: ['msg'],
        data() {
            return {
                mess: ''
            };
        },
        methods: {
            changeMess(event){
                this.mess = event.target.value;
                this.$emit('messChange', this.mess);
            }
        }
    }
</script>
