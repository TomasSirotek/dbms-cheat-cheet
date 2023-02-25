***

#### Classes should be open for extension but closed for modifications 

* Real life example : 

*You need to implement a feature that calculates the total shipping cost for a customer's order.

1. In order to make code open for extension but closed for modification, you can define an interface called `ShippingCostCalculator`:

``` java 

public interface ShippingCostCalculator {
    double calculateShippingCost(Product product, int quantity);
}
```

2. This allows to implement different shipping cost calculators as seperate classes each implementing `ShippingCostCalculator`:

``` java 

public class ElectronicsShippingCostCalculator implements ShippingCostCalculator {
    public double calculateShippingCost(Product product, int quantity) {
        // calculate shipping cost based on weight and size of electronics product
    }
}
```

3. In class called `Order` we can use shipping calculators 

``` java 

public class Order {
    private Map<Class<? extends Product>, ShippingCostCalculator> shippingCostCalculators;
    
    public Order() {
        this.shippingCostCalculators = new HashMap<>();
	    this.shippingCostCalculators.put(ElectronicsProduct.class,new ElectronicsShippingCostCalculator());
        // add other shipping cost calculators for other types of products
    }
    
    public double calculateTotalShippingCost(List<OrderItem> orderItems) {
        double totalShippingCost = 0;
        for (OrderItem orderItem : orderItems) {
            Product product = orderItem.getProduct();
            int quantity = orderItem.getQuantity();
            ShippingCostCalculator calculator = shippingCostCalculators.get(product.getClass());
            totalShippingCost += calculator.calculateShippingCost(product, quantity);
        }
        return totalShippingCost;
    }
}

```

* With this design, you can easily add new types of products and shipping cost calculators by creating new subclasses and implementing new `ShippingCostCalculator` classes, without having to modify the `Order` class.
