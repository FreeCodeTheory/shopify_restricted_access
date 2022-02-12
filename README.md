# Shopify Restricted Access

This could be pretty useful if you want to restrict the access of your store to specific customers.

### PART ONE

1. Open `theme.liquid` 
2. **Wrap** the `{{ content_for_layout }}` or any part you want to hide
3. Apply a simple `if else` condition using the `customer` liquid object. The complete layout or template or section you choose will be visible **ONLY IF** the user is a customer **AND IF** he is a customer with a specific tag ("Pro, B2B, VIP" or whatever you want). 

### PART TWO
At this step, you could have some siutations depending on the usecase and the general architecture of the Shopify Theme you use
For example if users desire to activate their account or recover their password, the following sections are contained **inside** the `{{ content_for_layout }}`
=> {% section 'main-customers-reset-password' %}
=> {% section 'main-customers-activate-account' %}		

4. So just think about a good way to include the different options.
