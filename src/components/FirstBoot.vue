<template>
    <div>
        <ul>
            <li v-for="data in dataList" :key="data.id">{{ data.name }}</li>
        </ul>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataList: [],
        };
    },

    mounted() {
        this.fetchData();
    },

    methods: {
        async fetchData() {
            try {
                const response = await this.$http.get('/api/data');
                this.dataList = response.data;
            } catch (error) {
                console.error('Error fetching data:', error);
            }
        },
    },
}
</script>
<!--
<script>
import axios from 'axios';
export default {
    data() {
        return {
            dataList: [],
        };
    },

    mounted() {
        this.fetchData();
    },

    methods: {
        async fetchData() {
            try {
                const response = await axios.get('http://ec2-3-36-216-183.ap-northeast-2.compute.amazonaws.com:8080/api/data');
                this.dataList = response.data;
            } catch (error) {
                console.error('Error fetching data:', error);
            }
        },
    },
}
</script>
-->