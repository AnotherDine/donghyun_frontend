<template>
    <div>
        <ul>
            <li v-for="data in dataList" :key="data.id">{{ data.name }}</li>
        </ul>
    </div>
</template>
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
-->