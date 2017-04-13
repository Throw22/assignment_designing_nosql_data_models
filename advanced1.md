Your eCommerce business needs to keep track of products and their prices. The products each belong to a department. The business needs to keep track of revenue as product prices change over time. The business also needs to keep track of receipts of transactions and the number of units each product has in stock.

department {
  id: unique int
  name: string
  products: [
    product {
    id: unique int
    name: string
    currPrice: float (xx.xx price)
    historicalPrices: [price floats]
    departmentId: int
    stock: int (>= 0)
  }]
}

(transactions indexed by day)
transaction {
  date: date obj
  paymentMethod: string ('amex', 'discover', 'gift card', etc.)
  productIds: [int]
  total: float (xx.xx price)
}
