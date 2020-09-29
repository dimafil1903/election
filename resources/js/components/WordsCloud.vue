<template>
    <div class="chart">
        <word-cloud-chart
            :data="wordCloudData"
            :size-range="[0,50]"
        />
    </div>
</template>

<script>


    // import wordsCloud from "dr-vue-echarts"

    export default {
        name: 'Base',
        data() {
            return {
                wordCloudData: this.party()

            }

        },
        methods: {
            party: function () {
                let arr = []
                for (let i=1; i<=10; i++){
                    arr.push({
                        name: 'Партия '+i,
                        value: Math.floor(Math.random() * Math.floor(100)),
                    })

                }
                return arr
            }
        }
    }
</script>

<style scoped>
    .chart {
        width: 100%;
        height: 300px;
    }
</style>
