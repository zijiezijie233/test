<template>
    <div class="hello">

    </div>
</template>

<script>
    import axios from 'axios';
    export default {
    name: 'test3',
    mounted() {
        axios({
            method: "get",
            url: "http://iwenwiki.com/api/blueberrypai/getChengpinDetails.php"
        }).then(res => {
            console.log(res.data);
        })
        }
    }
</script>

