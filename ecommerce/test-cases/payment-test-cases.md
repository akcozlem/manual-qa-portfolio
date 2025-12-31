# Payment Test Cases

## TC-PAY-01: Successful payment with valid credit card

**Precondition:**
- User is logged in
- Product is added to cart
- User is on checkout page

**Test Steps:**
1. Select credit card as payment method
2. Enter valid card number, expiry date and CVV
3. Click on "Place Order"

**Expected Result:**
- Payment is processed successfully
- Order confirmation page is displayed


---

## TC-PAY-02: Payment declined with invalid card number

**Precondition:**
- User is logged in
- Product is added to cart

**Test Steps:**
1. Select credit card as payment method
2. Enter invalid card number
3. Click on "Place Order"

**Expected Result:**
- Payment is declined
- Error message is displayed (exact wording may vary)
- Order is not created


---

## TC-PAY-03: Payment attempt with expired card

**Precondition:**
- User is logged in
- Product is added to cart

**Test Steps:**
1. Select credit card as payment method
2. Enter expired card details
3. Attempt to complete payment

**Expected Result:**
- Payment is declined
- User is informed that the card is expired


---

## TC-PAY-04: Network interruption during payment process

**Precondition:**
- User is logged in
- Product is added to cart

**Test Steps:**
1. Select credit card as payment method
2. Enter valid card details
3. Simulate network interruption during payment
4. Attempt to complete order

**Expected Result:**
- Payment is not completed
- User receives a clear error or retry message
- Order is not duplicated


---

## TC-PAY-05: Retry payment after initial failure

**Precondition:**
- Previous payment attempt has failed

**Test Steps:**
1. Retry payment with valid card details

**Expected Result:**
- Payment is completed successfully
- Only one order is created
