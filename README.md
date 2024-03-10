# UnusualSpends Design

## OOMD Design For Unsual money spend using credit card By comparing categories.

## States

### Private:
1. `userName`: String - Represents the name of the user.
2. `userEmail`: String - Represents the email address of the user.
3. `cardNumber`: String - Represents the credit card number associated with the user.

### Public:
1. `categories`: Enum->Represents spending categories.
2. `totalSpent`: Double->Represents the total amount spent.
3. `spentOnEachCategory`: Map<Enum, Double> - Represents the amount spent on each category.
4. `currentMonthSpent`: Double - Represents the total amount spent in the current month.
5. `lastMonthSpent`: Double - Represents the total amount spent in the last month.

### Behaviors

#### Public:
1. `getUserName()`: String - Returns the user's name.
2. `getCreditCardNumber()`: String - Returns the user's credit card number.
3. `getUserEmail()`: String - Returns the user's email address.
4. `getTotalSpent()`: Double - Returns the total amount spent.
5. `getSpentOnEachCategory()`: Map<Enum, Double> - Returns the amount spent on each category.
6. `getCurrentMonthSpent()`: Double - Returns the total amount spent in the current month.
7. `getLastMonthSpent()`: Double - Returns the total amount spent in the last month.
8. `sendMessage()`: Method to send a notification using the specified notification service.

## Polymorphism
The `sendMessage()` can be overridden like to Send Mail also and can Send Message through various Different Channels of Communivation.


## Java Class and Methods Example

This Is how it looks Like

```java
public class UnUsualSpend{
    private String userName;
    private String userEmail;
    private String cardNumber;
    provate Enum categories;
    private Double totalSpent;
    private Map<Enum, Double> spentOnEachCategory;
    private Double currentMonthSpent;
    private Double lastMonthSpent;

    public UnUsualSpend(String userName, String userEmail, String cardNumber){
        this.userName = userName;
        this.userEmail = userEmail;
        this.cardNumber = cardNumber;
    }
    public String getUserName() {
        return userName;
    }
    public String getUserEmail() {
        return userEmail;
    }
    public String getCardNumber() {
        return cardNumber;
    }

    public Enum getCategories() {
        return categories;
    }
    public Double getTotalSpent() {
        return totalSpent;
    }
    public Map<Enum, Double> getSpentOnEachCategory() {
        return spentOnEachCategory;
    }
    public Double getCurrentMonthSpent() {
        return currentMonthSpent;
    }
    public Double getLastMonthSpent() {
        return lastMonthSpent;
    }
    public void sendMessage() {
        service.sendNotification(userEmail, "Unusual spending....");
    }
}







