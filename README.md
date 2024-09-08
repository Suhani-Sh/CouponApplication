# CouponApplication
Coupon Application for MonkCommerce
README
Overview
This project implements a coupon management system that allows users to apply coupons to their shopping carts. The system handles various aspects of coupon validation and application, ensuring that coupons are applicable based on certain criteria.

Implemented Cases
Apply Coupon to Cart:

Functionality: Applies a coupon to a cart if the coupon is valid and applicable.
Details:
Validates that the cart is not null.
Retrieves the coupon based on its ID.
Checks if the coupon is applicable based on expiration date, minimum cart value, and category.
Applies the discount to the cart's total amount.
Returns the updated cart with the applied discount.
Retrieve Applicable Coupons:

Functionality: Retrieves a list of coupons that are applicable based on the given request.
Details:
Filters coupons based on code, type, expiration date, minimum cart value, and applicable categories.
Returns a list of coupons that meet the criteria.
Unimplemented Cases
Coupon Expiration Handling:

Reason: The current implementation only checks if the coupon is not expired, but it doesn’t handle scenarios where coupons become invalid once expired.
Detailed Error Handling for Specific Coupon Criteria:

Reason: The current error handling is generic. Detailed error messages for specific criteria (e.g., invalid minimum cart value) are not yet implemented.
User-Specific Coupon Restrictions:

Reason: The system does not yet handle user-specific coupon restrictions, such as limiting the number of times a coupon can be used by a single user.
Limitations
Date and Time Precision:

Limitation: The system uses LocalDateTime for date comparisons, which may not account for timezone differences or daylight saving changes.
Performance with Large Data Sets:

Limitation: The filtering logic operates in-memory on a list of all coupons, which may not be efficient for large data sets. A more scalable solution would involve database-level filtering.
Coupon Code Uniqueness:

Limitation: The current implementation assumes that coupon codes are unique, but there is no enforcement or validation of uniqueness within the system.
Assumptions
Valid Coupon Codes:

Assumption: It is assumed that coupon codes are always valid and correctly formatted when received.
Cart and Coupon Consistency:

Assumption: The system assumes that the cart and coupon data are consistent and correctly populated in the database.
Request Data Integrity:

Assumption: It is assumed that the data in the CouponRequest object is always complete and correctly formatted.
Non-null Values:

Assumption: The system assumes that critical values (e.g., expiration date, minimum cart value) are not null and are correctly set in the database.
This documentation provides a clear and comprehensive overview of the implemented functionality, limitations, and assumptions, helping users and developers understand the current state of the project.
