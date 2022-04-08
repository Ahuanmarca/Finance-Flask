# Pset 9 from CS50x
https://cs50.harvard.edu/x/2022/

## Description
Web App created with Python and the Flask framework that allows the user to quote stocks, buy and sell stocks, see a list of owned stocks and see a history of transactions.

## Specification
- **register**
    - User must input username. Renders apology is blank or already exists.
    - User must input password and then confirm. Renders apology if either input is blank or the passwords don't match.
    - Submits user's input via ```POST``` to register.
    - ```INSERT``` the new user into ```users```, storing a hash of the user's password, not the password itself. Hash the user's password with ```generate_password_hash```
- **quote**
    - Require stock's symbol implemented as a text field whose ```name``` is ```symbol```
    - Sumbits the user's input via ```POST``` to ```/quote``` 
- **buy**
    - Requires stock's symbol. Renders apology if blank or invalid symbol
    - Require a number of stocks. Renders apology if invalid input or not enough cash
    - Submits via ```POST```
- **index** displays for logged user...
    - which stocks the user owns
    - number of shares owned
    - current price of each stock
    - total value of each holding
    - user's current cash balance and grand total
- **sell**
    - Requires stock symbol as ```select``` menu
    - Requires number of shares to sell
    - Render apology if user tries to sell more stocks than he owns, or if somehow tries to sell a symbol that is not on it's portfolio
    - Submits via ```POST```
- **history** displays for logged user...
    - rows with transactions
    - each row shows whether a stock was bought or sold, the stock's symbol, purchase or sell price, number of shares bought or sold, the date and time of the transaction
- **personal touch**
    - Allows the user to change password
    - The Index Page shows colored text if the holding has won or lost money

