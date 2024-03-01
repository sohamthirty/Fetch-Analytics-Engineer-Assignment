# Fetch Rewards Coding Exercise - Analytics Engineer
- • Demonstrate how you reason about data and how you communicate your understanding of a specific data set to others.

## Requirements
**First:** 
- • Review Existing Unstructured Data and Diagram a New Structured Relational Data Model
- • Review the 3 sample data files provided below. Develop a simplified, structured, relational diagram to represent how you would model the data in a data warehouse.

**Second:** 
- • Write a query that directly answers a predetermined question from a business stakeholder
- 1. What are the top 5 brands by receipts scanned for most recent month?
- 2. How does the ranking of the top 5 brands by receipts scanned for the recent month compare to the ranking for the previous month?
- 3. When considering average spend from receipts with 'rewardsReceiptStatus’ of ‘Accepted’ or ‘Rejected’, which is greater?
- 4. When considering total number of items purchased from receipts with 'rewardsReceiptStatus’ of ‘Accepted’ or ‘Rejected’, which is greater?
- 5. Which brand has the most spend among users who were created within the past 6 months?
- 6. Which brand has the most transactions among users who were created within the past 6 months?

**Third:** 
- • Evaluate Data Quality Issues in the Data Provided

**Fourth:** 
- • Communicate with Stakeholders
- • Construct an email or slack message that is understandable to a product or business leader who isn’t familiar with your day to day work. This part of the exercise should show off how you communicate and reason about data with others. 
- 1. What questions do you have about the data?
- 2. How did you discover the data quality issues?
- 3. What do you need to know to resolve the data quality issues?
- 4. What other information would you need to help you optimize the data assets you're trying to create?
- 5. What performance and scaling concerns do you anticipate in production and how do you plan to address them?


## The Data
**receipts.json.gz**
- • _id: uuid for this receipt
- • bonusPointsEarned: Number of bonus points that were awarded upon receipt completion
- • bonusPointsEarnedReason: event that triggered bonus points
- • createDate: The date that the event was created
- • dateScanned: Date that the user scanned their receipt
- • finishedDate: Date that the receipt finished processing
- • modifyDate: The date the event was modified
- • pointsAwardedDate: The date we awarded points for the transaction
- • pointsEarned: The number of points earned for the receipt
- • purchaseDate: the date of the purchase
- • purchasedItemCount: Count of number of items on the receipt
- • rewardsReceiptItemList: The items that were purchased on the receipt
- • rewardsReceiptStatus: status of the receipt through receipt validation and processing
- • totalSpent: The total amount on the receipt
- • userId: string id back to the User collection for the user who scanned the receipt

**users.json.gz:**
- • _id: user Id
- • state: state abbreviation
- • createdDate: when the user created their account
- • lastLogin: last time the user was recorded logging in to the app
- • role: constant value set to 'CONSUMER'
- • active: indicates if the user is active; only Fetch will de-activate an account with this flag

**brands.json.gz:**
- • _id: brand uuid
- • barcode: the barcode on the item
- • brandCode: String that corresponds with the brand column in a partner product file
- • category: The category name for which the brand sells products in
- • categoryCode: The category code that references a BrandCategory
- • cpg: reference to CPG collection
- • topBrand: Boolean indicator for whether the brand should be featured as a 'top brand'
- • name: Brand name
