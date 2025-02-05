# Coding-Challenge-6
// Task 1 - Business Profit Calculation

// Function to calculate profit
function calculateProfit(costPrice, sellingPrice, unitsSold) {
    const profit = (sellingPrice - costPrice) * unitsSold;
    console.log(`Total Profit: $${profit}`);
}

// Test Data
calculateProfit(20, 30, 100);  // Expected output: "Total Profit: $1000"
calculateProfit(50, 70, 200);  // Expected output: "Total Profit: $4000"
