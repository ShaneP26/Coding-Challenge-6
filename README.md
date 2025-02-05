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
// Task 3 - Employee Bonus Calculation

// Arrow function to calculate bonus
const calculateBonus = (salary, performanceRating) => {
    let bonusPercentage = 0;
    if (performanceRating === "Excellent") {
        bonusPercentage = 0.2;
    } else if (performanceRating === "Good") {
        bonusPercentage = 0.1;
    } else if (performanceRating === "Average") {
        bonusPercentage = 0.05;
    }
    const bonus = salary * bonusPercentage;
    console.log(`Bonus: $${bonus}`);
};

// Test Data
calculateBonus(5000, "Excellent");  // Expected output: "Bonus: $1000"
calculateBonus(7000, "Good");       // Expected output: "Bonus: $700"

// Task 4 - Subscription Pricing Model

// Function to calculate subscription cost
function calculateSubscriptionCost(plan, months, discount = 0) {
    let costPerMonth;
    if (plan === "Basic") {
        costPerMonth = 10;
    } else if (plan === "Premium") {
        costPerMonth = 20;
    } else if (plan === "Enterprise") {
        costPerMonth = 50;
    }

    const totalCost = (costPerMonth * months) - discount;
    console.log(`Total Cost: $${totalCost}`);
}

// Test Data
calculateSubscriptionCost("Basic", 6, 10);   // Expected output: "Total Cost: $50"
calculateSubscriptionCost("Premium", 12, 0); // Expected output: "Total Cost: $240"

// Task 5 - Currency Conversion

// Function to convert currency
function convertCurrency(amount, exchangeRate) {
    const convertedAmount = amount * exchangeRate;
    console.log(`Converted Amount: $${convertedAmount.toFixed(2)}`);
}

// Test Data
convertCurrency(100, 1.1);  // Expected output: "Converted Amount: $110.00"
convertCurrency(250, 0.85); // Expected output: "Converted Amount: $212.50"
// Task 6 - Higher-Order Function for Bulk Orders

// Higher-order function to apply bulk discount
function applyBulkDiscount(orders, discountFunction) {
    return orders.map(order => discountFunction(order));
}

// Test Data
let orders = [200, 600, 1200, 450, 800];
let discountedOrders = applyBulkDiscount(orders, amount => amount > 500 ? amount * 0.9 : amount);
console.log(discountedOrders); // Expected output: [200, 540, 1080, 450, 720]

// Task 7 - Business Expense Tracker

// Function to create expense tracker
function createExpenseTracker() {
    let totalExpenses = 0;
    return function(expense) {
        totalExpenses += expense;
        return `Total Expenses: $${totalExpenses}`;
    };
}

// Test Data
let tracker = createExpenseTracker();
console.log(tracker(200)); // Expected output: "Total Expenses: $200"
console.log(tracker(150)); // Expected output: "Total Expenses: $350"

// Task 8 - Employee Promotion Evaluation

// Recursive function to calculate years to promotion
function calculateYearsToPromotion(employeeLevel) {
    if (employeeLevel >= 10) {
        return `Years to Level 10: 0`;
    }
    return `Years to Level 10: ${(10 - employeeLevel) * 2}`;
}

// Test Data
console.log(calculateYearsToPromotion(7));  // Expected output: "Years to Level 10: 6"
console.log(calculateYearsToPromotion(5));  // Expected output: "Years to Level 10: 10"
