<template>
    <div class="alert alert-warning alert-flash" role="alert" v-show="show">
        <strong>Sucess!</strong> {{ body }}
    </div>
</template>

<script>
    export default {
        props: ['message'],

        data() {
            return {
                body: '',
                show: false
            }
        },

        created() {
            if (this.message) {
                this.body = this.message;
                this.show = true;
            }
        }
    };
</script>

<style>
    .alert-flash{
        position: fixed;
        right: 25px;
        bottom: 25px;
    }
</style>
