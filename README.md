- 👋 Hi, I’m @ihassan-9
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
- <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hotel Carbon Footprint Calculator</title>
  <style>
    /* Add CSS styling here */
  </style>
</head>
<body>
  <header>
    <h1>Hotel Carbon Footprint Calculator</h1>
    <p>Measure your hotel's carbon footprint by entering the data below.</p>
  </header>

  <section>
    <form id="carbonCalculator">
      <h2>Energy Consumption</h2>
      <label for="electricity">Electricity (kWh):</label>
      <input type="number" id="electricity" name="electricity"><br>

      <label for="naturalGas">Natural Gas (m³):</label>
      <input type="number" id="naturalGas" name="naturalGas"><br>

      <h2>Water Usage</h2>
      <label for="water">Water Usage (m³):</label>
      <input type="number" id="water" name="water"><br>

      <h2>Waste Generation</h2>
      <label for="waste">Waste Generated (kg):</label>
      <input type="number" id="waste" name="waste"><br>

      <h2>Transportation</h2>
      <label for="transport">Guest Transportation Distance (km):</label>
      <input type="number" id="transport" name="transport"><br>

      <h2>Food and Beverage</h2>
      <label for="beef">Beef Consumption (kg):</label>
      <input type="number" id="beef" name="beef"><br>

      <button type="button" onclick="calculateFootprint()">Calculate Carbon Footprint</button>
    </form>
  </section>

  <section id="results">
    <h2>Your Carbon Footprint</h2>
    <p id="output"></p>
  </section>

  <script>
    // JavaScript to calculate the carbon footprint
    function calculateFootprint() {
      const electricity = parseFloat(document.getElementById('electricity').value) || 0;
      const naturalGas = parseFloat(document.getElementById('naturalGas').value) || 0;
      const water = parseFloat(document.getElementById('water').value) || 0;
      const waste = parseFloat(document.getElementById('waste').value) || 0;
      const transport = parseFloat(document.getElementById('transport').value) || 0;
      const beef = parseFloat(document.getElementById('beef').value) || 0;

      // Example emission factors (replace with real data)
      const electricityFactor = 0.5; // kg CO2e/kWh
      const naturalGasFactor = 2; // kg CO2e/m³
      const waterFactor = 0.3; // kg CO2e/m³
      const wasteFactor = 1.9; // kg CO2e/kg
      const transportFactor = 0.25; // kg CO2e/km
      const beefFactor = 27; // kg CO2e/kg

      const energyEmissions = electricity * electricityFactor + naturalGas * naturalGasFactor;
      const waterEmissions = water * waterFactor;
      const wasteEmissions = waste * wasteFactor;
      const transportEmissions = transport * transportFactor;
      const foodEmissions = beef * beefFactor;

      const totalEmissions = energyEmissions + waterEmissions + wasteEmissions + transportEmissions + foodEmissions;

      document.getElementById('output').innerText = `Total Carbon Footprint: ${totalEmissions.toFixed(2)} kg CO2e`;
    }
  </script>
</body>
</html>



<!---
ihassan-9/ihassan-9 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
