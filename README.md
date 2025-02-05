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
// Task 2 - Sales Tax Computation

// Function expression to calculate sales tax
const calculateSalesTax = function(amount, taxRate) {
    const tax = amount * taxRate;
    console.log(`Sales Tax: $${tax}`);
};

// Test Data
calculateSalesTax(100, 0.07);  // Expected output: "Sales Tax: $7"
calculateSalesTax(500, 0.1);   // Expected output: "Sales Tax: $50"
