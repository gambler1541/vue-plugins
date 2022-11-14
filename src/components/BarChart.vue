<template>
    <canvas ref="barChart" id="barChart"></canvas>
</template>

<script>
import { Chart } from 'chart.js'

export default {
    mounted() {
        const labels = [
            'January',
            'February',
            'March',
            'April',
            'May',
            'June',
        ];

        const data = {
            labels: labels,
            datasets: [{
                label: 'My First dataset',
                backgroundColor: 'rgb(255, 99, 132)',
                borderColor: 'rgb(255, 99, 132)',
                data: [0, 10, 5, 2, 20, 30, 45],
            }]
        };

        const config = {
            type: 'bar',
            data: data,
            options: {}
        };

        const myChart = new this.$_Chart(
            // document.getElementById('barChart'),
            this.$refs.barChart,
            config
        );        
    }
}
</script>

<style>

</style>