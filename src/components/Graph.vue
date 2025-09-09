<template>
  <div id="myChart" style="width: 400px; height: 400px"></div>
</template>

<script>
import Chart from "chart.js/auto";

const apiKey = import.meta.env.VITE_API_KEY;

async function getData() {
  const url = `https://www.alphavantage.co/query?function=TIME_SERIES_INTRADAY&symbol=IBM&interval=5min&apikey=${apiKey}`;

  try {
    const response = await fetch(url);
    if (!response.ok) throw new Error("Response status: " + response.status);

    const result = await response.json();
    console.log(result);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}

// Call the function
getData();
</script>
