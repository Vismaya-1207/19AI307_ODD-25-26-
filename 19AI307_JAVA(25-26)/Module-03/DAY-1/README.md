# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To build an inheritance-based Java program that calculates the final price of gold for different types of customers (Regular and Premium), applying respective discounts and showing cashback for premium customers.

## ALGORITHM :
1.Start the program.

2.Import Scanner and DecimalFormat.

3.Create a Customer class with attributes: customerId, name, purchaseWeight, and goldRatePerGram.

4.Create methods in Customer: getDiscountRate(), calculateFinalPrice(), and display().

5.Create RegularCustomer class that extends Customer and overrides getDiscountRate().

6.Create PremiumCustomer class that extends Customer, overrides getDiscountRate(), and adds calculateCashback() and display().

7.In main(), read customer type, id, name, purchase weight, and gold rate.

8.Based on customer type, create the appropriate object and call display().

9.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by:VISMAYA.V
RegisterNumber:212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100.0;
        return purchaseWeight * (goldRatePerGram - discountAmount);
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 2;
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String customerType = sc.nextLine().trim(); 
        String customerId = sc.nextLine();
        String name = sc.nextLine();
        double purchaseWeight = Double.parseDouble(sc.nextLine());
        double goldRate = Double.parseDouble(sc.nextLine());

        if (customerType.equalsIgnoreCase("Premium")) {
            PremiumCustomer p = new PremiumCustomer(customerId, name, purchaseWeight, goldRate);
            p.display("Premium"); 
        } else if (customerType.equalsIgnoreCase("Regular")) {
            RegularCustomer r = new RegularCustomer(customerId, name, purchaseWeight, goldRate);
            r.display("Regular");
        } else {
            Customer c = new Customer(customerId, name, purchaseWeight, goldRate);
            c.display("Standard");
        }

        sc.close();
    }
}

```
## OUTPUT:
<img width="1280" height="843" alt="image" src="https://github.com/user-attachments/assets/8e368017-6785-4d62-ad00-b8d7978f24b4" />



## RESULT:
Therefore,the program was executed successfully.
