# Checkout Test Cases

## TC-01: Successful checkout with valid credit card

**Precondition:**
- User is logged in
- Product is added to the cart

**Test Steps:**
1. Navigate to the checkout page
2. Enter valid shipping information
3. Select "Credit Card" as payment method
4. Enter valid card details
5. Click on "Place Order"

**Expected Result:**
- Order is successfully placed
- Order confirmation page is displayed
- Confirmation email is sent to the user


---

## TC-02: Checkout attempt with empty cart

**Precondition:**
- User is logged in
- Cart is empty

**Test Steps:**
1. Navigate directly to the checkout page

**Expected Result:**
- User is redirected to the cart page
- Error message is displayed indicating the cart is empty


---

## TC-03: Checkout with invalid credit card details

**Precondition:**
- User is logged in
- Product is added to the cart

**Test Steps:**
1. Navigate to the checkout page
2. Enter valid shipping information
3. Select "Credit Card" as payment method
4. Enter invalid card number
5. Click on "Place Order"

**Expected Result:**
- Payment is declined
- Proper validation error message is displayed
- Order is not created


---

## TC-04: Checkout with missing mandatory shipping fields

**Precondition:**
- User is logged in
- Product is added to the cart

**Test Steps:**
1. Navigate to the checkout page
2. Leave mandatory shipping fields empty
3. Attempt to proceed to payment

**Expected Result:**
- User is not allowed to proceed
- Validation messages are displayed for required fields


---

## TC-05: Checkout page load performance

**Precondition:**
- User is logged in
- Product is added to the cart

**Test Steps:**
1. Navigate to the checkout page

**Expected Result:**
- Checkout page loads successfully
- Page load time is within acceptable limits
