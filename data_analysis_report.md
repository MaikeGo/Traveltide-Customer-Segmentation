## **Customer Segmentation Analysis Report**

### **1. Introduction**
The goal of this project was to identify distinct customer segments for the **Traveltide website**, enabling more targeted marketing strategies to improve customer retention and generate repeat business. Our approach combined exploratory data analysis (EDA) with user behavior metrics to create actionable segments.

### **2. Data Overview and Cohort Filtering**
- The data consisted of sessions from the **Traveltide website**, capturing user interactions such as bookings, searches, and cancellations over multiple years.
- We applied a cohort filter, focusing on users with sessions after **January 4th, 2023**, who had at least **8 sessions**. This resulted in a dataset with **49,211 sessions**, involving **5,998 unique users** and **16,099 unique trip IDs**.

### **3. Exploratory Data Analysis (EDA)**
Our EDA consisted of the following key steps:

#### 3.1 **Data Inspection**
- Conducted an initial check for data types, missing values, and overall structure.
- Validated the format and range of critical columns (e.g., `trip_id`, `departure_date`, `check_in_date`) to identify any data quality issues.

#### 3.2 **Data Cleaning and Validation**
- **Nights Count:** Recalculated the `nights` column based on check-in and check-out dates due to discrepancies.
- **Cancellation Rows:** Identified irregularities where cancellation rows contained misleading data. Excluded these from calculations when necessary.
- **Discount Data:** Verified whether discounts offered were actually used by comparing the `discount_percentage` and `discount_offered` columns for both flights and hotels.

#### 3.3 **User Behavior Analysis**
- **Booking Preferences:** Assessed whether users booked flights only, hotels only, or both. Found that **75.62%** of trips included both flight and hotel bookings, with only 0.03% being hotel-only trips.
- **Gender Bias:** Noticed a significant gender imbalance in our data, with 88.2% of users identified as female (`F`), 11.6% as male (`M`), and 0.2% as other (`O`).
This bias may impact the generalizability of our findings and should be taken into account in future analyses.
- **Trip Activity:** Analyzed the distribution of sessions and bookings, revealing that users booked an average of 4 trips within 8 sessions.
- **Demographics:** Explored gender, marital status, and family status distribution, noting a high proportion of solo travelers.
- **Discount Analysis:** Examined the impact of flight and hotel discounts on booking behavior, finding that **hotel discounts had a greater influence on conversions than flight discounts.** This suggests that hotel-related perks might be more effective for certain segments.

### **4. Aggregating User Metrics**
We aggregated key metrics at the user level to facilitate segmentation. These included:
- **Demographics:** Age, marital status, and children status.
- **Booking Behavior:** Count of flights, hotels, total trips, solo vs. group trips, etc.
- **Discount Sensitivity:** Calculated `discount_usage_rate` and `discount_response_rate` for both flights and hotels.
- **Spending Behavior:** Calculated total spending (`total_trip_usd`), average spending per seat, and per hotel room.
- **Engagement Metrics:** Average page clicks across all sessions vs. booking sessions.

### **5. Customer Segmentation**
Using the aggregated metrics, we developed the following segments based on spending patterns, responsiveness to discounts, and trip characteristics:
1. **Zerobookers**: Users with no bookings (potential for conversion).
2. **Big Spenders**: High-value users spending above average on flights and hotels.
3. **Bargain Hunters (High-Spenders)**: Users who respond to discounts but still spend significantly.
4. **Bargain Hunters (Budget)**: Users who seek discounts and have lower spending overall.
5. **Luxury Lovers**: Users who prefer premium experiences with higher spending on hotels, flights, or longer stays.
6. **Other Frequent Travelers**: Users who travel frequently but don’t fit into other segments.
7. **Other Infrequent Travelers**: Users who travel less frequently but may still be active.

### **6. Segment Analysis**
- **Bargain Hunters** showed significant discount responsiveness, while **Luxury Lovers** were less influenced by discounts but appreciated premium experiences.
- **Zero Bookers** were typically younger or older users, representing an opportunity to attract new customers.
- **Big Spenders** contributed disproportionately to total revenue, indicating high retention value.
- We used distribution plots and boxplots to visualize spending behavior, booking frequency, and discount sensitivity across all segments.

### **7. Perk Assignment and Recommendations**
Based on the segment characteristics and marketing's proposed perks, we assigned perks to each group and provided tailored recommendations (refer to the executive summary). Given the strong influence of hotel discounts on bookings, we recommend focusing on these perks for groups sensitive to price.

### **8. Limitations and Considerations**
- The analysis is based on historical data, and customer behaviors may change over time. Some segments, such as **Zero Bookers**, do not have enough data points to predict future behavior accurately.
- Additionally, there is some overlap and fuzziness between segments, which may be refined further through ongoing testing and additional analysis.
- Discount responsiveness and preferences might differ by user segment, travel season, or booking circumstances. Therefore, it's essential to conduct **A/B testing** to validate the effectiveness of these perks and make data-driven adjustments as needed.
- Further analysis should be conducted on other variables such as booking seasonality, user demographics, and trip purpose to refine targeting.

### **9. Conclusion and Next Steps**
The segmentation provides a foundation for personalized marketing strategies, but continuous analysis and testing will be crucial to refining these segments and ensuring they remain relevant over time.
