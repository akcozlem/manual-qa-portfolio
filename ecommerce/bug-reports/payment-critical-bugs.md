# Critical Payment Bug Reports

---

## BUG-01: Order is created even when payment fails

**Severity:** Critical  
**Priority:** High  
**Environment:** Staging  
**Browser:** Chrome 120  

**Precondition:**
- User is logged in
- Product is added to cart

**Steps to Reproduce:**
1. Navigate to checkout page
2. Enter valid shipping information
3. Select credit card as payment method
4. Enter invalid card details
5. Click on "Place Order"

**Actual Result:**
- Payment fails
- Order is still created in the system

**Expected Result:**
- Payment should be declined
- Order should NOT be created

**Notes:**
- This issue may cause financial inconsistencies
- Observed intermittently during multiple test attempts

---

## BUG-02: No error message displayed when payment is declined

**Severity:** Major  
**Priority:** Medium  
**Environment:** Staging  
**Browser:** Firefox  

**Precondition:**
- User is logged in
- Product is added to cart

**Steps to Reproduce:**
1. Navigate to checkout page
2. Select credit card payment
3. Enter invalid card information
4. Click on "Place Order"

**Actual Result:**
- Payment is declined
- No error message is shown to the user

**Expected Result:**
- Clear error message should be displayed
- User should be prompted to retry payment

**Notes:**
- Issue impacts user experience
