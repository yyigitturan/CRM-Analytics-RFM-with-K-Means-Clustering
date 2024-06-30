# CRM-Analytics-RFM-with-K-Means-Clustering

<a id="contents_tabel"></a>    
<div style="border-radius:10px; padding: 15px; background-color: #FFFFFF; font-size:130%; text-align:left">

<h2 align="left"><font color=#34e3af>Table of Contents:</font></h2>
    
* [Step 1 | Introduction](#introduction)
    - [Step 1.1 | Importing Necessary Libraries](#libraries) 
    - [Step 1.2 | Loading the Dataset](#read_dataset)
* [Step 2 | Exploratory Data Analysis](#eda) 
    - [Step 2.1 | Missing Values](#missing) 
    - [Step 2.2 | Removing Duplicated Values](#duplicated)
    - [Step 2.3 | Visualization](#visualize) 
* [Step 3 | CRM Analytics ](#crm_analytics)
    - [Step 3.1 | RFM Analysis](#rfm_analysis)
    - [Step 3.2 | Define RFM Metrics ](#rfm_metrics)
    - [Step 3.3 | Define Segmentation Map](#segment)
    - [Step 3.4 | Visualization](#visualization)
* [Step 4 | Customer Segmentation with K-Means](#cltv)
    - [Step 4.1 | Define BG-NBD Model Features](#bg_nbd)
    - [Step 4.2 | Define Gamma-Gamma Model](#gamma)
* [Step 5 | Customer Segmentation with K-Means](#kmeans)
    - [Step 5.1 | Create your model and segment your customers](#create_segment)
    - [Step 5.2 | Visualization](#visual_segment)
* [Step 6 | Conclusion](#conclusion)

<a id="introduction"></a>
# <b><span style='color:#09ba85'>Step 1 |</span><span style='color:#34e3af'> Introduction</span></b>
⬆️ [Tabel of Contents](#contents_tabel)

In this project, we delve deep into the thriving sector of online retail by analyzing a transactional dataset from a UK-based retailer, available at the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail). This dataset documents all transactions between 2010 and 2011. Our primary objective is to amplify the efficiency of marketing strategies and boost sales through customer segmentation.

By leveraging advanced CRM analytics, we aim to understand customer behavior, identify key segments, and tailor marketing efforts to enhance customer satisfaction and retention. This project will involve a comprehensive analysis including RFM (Recency, Frequency, Monetary) analysis, customer lifetime value prediction, and clustering techniques to provide actionable insights for data-driven decision making. 

<a id="read_dataset"></a>
# <b><span style='color:#09ba85'>Step 1.2 |</span><span style='color:#34e3af'> Reading Dataset</span></b>
⬆️ [Tabel of Contents](#contents_tabel)

<span style="color:#31A919;
             font-size:160%;
             font-family:Verdana;">
📃 Variable Description
    
- **InvoiceNo:** Invoice number that consists 6 digits. If this code starts with letter 'c', it indicates a cancellation.
- **StockCode:** Product code that consists 5 digits.
- **Description:** Product name.
- **Quantity:** The quantities of each product per transaction.
- **InvoiceDate:** Represents the day and time when each transaction was generated.
- **UnitPrice:** Product price per unit.
- **CustomerID:** Customer number that consists 5 digits. Each customer has a unique customer ID.
- **Country:** Name of the country where each customer resides.

<a id="crm_analytics"></a>
# <b><span style='color:#09ba85'>Step 3 |</span><span style='color:#34e3af'> CRM Analytics</span></b>
⬆️ [Tabel of Contents](#contents_tabel)


CRM analytics are data that demonstrate your company’s sales and customer service performance. CRM analytics also presents customer data that you can use to inform smarter business decisions. Typically, you’ll use CRM software to obtain CRM analytics and automate all your data collection and report generation.    
    
<span style="color:#31A919;
             font-size:160%;
             font-family:Verdana;">
Benefits of CRM Analysis
    
The primary benefit of CRM analysis is that you can use it to inform your sales, customer service and marketing processes. You can use your CRM analytics to improve your methods via:

- **Customer service evaluations.** CRM analytics fill you in on your customer service team’s performance. If you see figures that your team could improve, implement practices that push your team toward these goals.
- **Accurate customer data.** Whether you’re using your customer data for demographic marketing or email marketing, you need to know whether you’re reaching the right person. CRM analysis ensures you’re doing just that.
- **Thorough customer analytics.** How much does your customer usually spend per quarter with you? Are they buying the same products time and time again, or does it vary? With CRM analytics, you’ll get firm answers to these questions, and you can use what you learn to refine your marketing strategies.
- **Efficient lead generation.** Your CRM analysis can tell you which of your marketing efforts most strongly correlate to purchases. If you see one approach correlating strongly to purchases but have only targeted a sliver of your customers with that approach, try that method more – your sales might increase.

  
<a id="rfm_analysis"></a>
# <b><span style='color:#09ba85'>Step 3.1 |</span><span style='color:#34e3af'> RFM Analysis </span></b>
⬆️ [Tabel of Contents](#contents_tabel)

RFM stands for **Recency**, **Frequency**, and **Monetary** value, each corresponding to some key customer trait. These RFM metrics are important indicators of a customer’s behavior because frequency and monetary value affects a customer’s lifetime value, and recency affects retention, a measure of engagement.   

RFM factors illustrate these facts:

- The more recent the purchase, the more responsive the customer is to promotions
- The more frequently the customer buys, the more engaged and satisfied they are
- Monetary value differentiates heavy spenders from low-value purchasers

<span style="color:#31A919;
             font-size:160%;
             font-family:Verdana;">

<a id="segment"></a>
# <b><span style='color:#09ba85'>Step 3.3 |</span><span style='color:#34e3af'> Define Segmentation Map </span></b>
⬆️ [Tabel of Contents](#contents_tabel)







By segmenting customers based on their RFM scores, we can develop targeted marketing strategies that address the specific needs and preferences of each segment. This approach not only improves customer satisfaction but also optimizes marketing expenditure by focusing resources on the most promising customer groups. 






<a id="visualization"></a>
# <b><span style='color:#09ba85'>Step 3.4 |</span><span style='color:#34e3af'> Visualization </span></b>
⬆️ [Tabel of Contents](#contents_tabel)


- **Personalized Marketing Campaigns:** Use RFM segments to create personalized marketing campaigns that cater to the unique preferences of each customer group.
- **Loyalty Programs:** Develop loyalty programs that reward frequent purchasers and high-value customers to foster long-term loyalty and increase customer retention.
- **Promotional Strategies:** Design timely and relevant promotional strategies for customers who have recently interacted with the brand to boost engagement and conversion rates.




<a id="cltv"></a>
# <b><span style='color:#09ba85'>Step 4 |</span><span style='color:#34e3af'> Customer Lifetime Value </span></b>
⬆️ [Tabel of Contents](#contents_tabel)

Customer Lifetime Value (CLTV) analysis is crucial for estimating the total value customers bring to a business, guiding strategic decision-making. In this project, CLTV analysis has deepened our understanding of customer segmentation and helped us optimize future revenue potential.






#%% md
Customer Lifetime Value (CLTV) analysis is crucial for estimating the total value customers bring to a business, guiding strategic decision-making. In this project, CLTV analysis has deepened our understanding of customer segmentation and helped us optimize future revenue potential. 
#%%
# today date- inovoicedate.min()
#%%
cltv_df = df.groupby("CustomerID").agg(
    {
        "InvoiceDate": [
            lambda x: (x.max() - x.min()).days,
            lambda x: (today_date - x.min()).days,
        ],
        "InvoiceNo": "nunique",
        "TotalPrice": "sum",
    }
)

cltv_df.columns = cltv_df.columns.droplevel(0)
cltv_df.columns = ["recency", "T", "frequency", "monetary"]
cltv_df.head()
#%%

#%%
#Average Order Value
cltv_df["monetary"] = cltv_df["monetary"] / cltv_df["frequency"]

#Recency & Tenure
cltv_df["recency"] = cltv_df["recency"] / 7
cltv_df["T"] = cltv_df["T"] / 7

#Frequency
cltv_df = cltv_df[(cltv_df['frequency'] > 1)]
#%%

#%% md
<a id="bg_nbd"></a>
# <b><span style='color:#09ba85'>Step 4.1 |</span><span style='color:#34e3af'> Define BG-NBD Model </span></b>
⬆️ [Tabel of Contents](#contents_tabel)
#%%
BGF = BetaGeoFitter(penalizer_coef=0.001)  # avoid overfitting

BGF.fit(cltv_df["frequency"], cltv_df["recency"], cltv_df["T"])
#%%
BGF.conditional_expected_number_of_purchases_up_to_time(
    #week
    1, cltv_df["frequency"], cltv_df["recency"], cltv_df["T"]
).sort_values(ascending=False).head(10).to_frame(
    "Expected Number of Transactions"
).reset_index()
#%%

#%%
BGF.conditional_expected_number_of_purchases_up_to_time(
    4, cltv_df["frequency"], cltv_df["recency"], cltv_df["T"]
).sort_values(ascending=False).head(10).to_frame(
    "Expected Number of Transactions"
).reset_index()
#%%

#%% md
<a id="gamma"></a>
# <b><span style='color:#09ba85'>Step 4.2 |</span><span style='color:#34e3af'> Define Gamma-Gamma Model </span></b>
⬆️ [Tabel of Contents](#contents_tabel)
#%%
ggf = GammaGammaFitter(penalizer_coef=0.01)
#%%
cltv_df = cltv_df[cltv_df['monetary'] > 0]
#%%
ggf.fit(cltv_df['frequency'], cltv_df['monetary'])
#%%
# Expected average profit

cltv_df["expected_average_profit"] = ggf.conditional_expected_average_profit(cltv_df['frequency'],
                                                                             cltv_df['monetary'])
#%%
cltv_df.head()
#%%

#%%
cltv_df["clv"] = ggf.customer_lifetime_value(BGF,
                                   cltv_df['frequency'],
                                   cltv_df['recency'],
                                   cltv_df['T'],
                                   cltv_df['monetary'],
                                   time=3,  
                                   freq="W", 
                                   discount_rate=0.01)
#%%
cltv_df = cltv_df.reset_index()
cltv_df.head()
#%%

#%%
cltv_df["cltv_segment"] = pd.qcut(cltv_df["clv"], 4, labels=["D", "C", "B", "A"])
#%%
cltv_df.groupby("cltv_segment").agg({"count", "mean", "sum"})
#%%

#%% md
In this project, we identified four customer segments (A, B, C, and D) based on the CLTV analysis. Here are the insights and recommendations for each segment:

**Segment A: High Value, High Engagement**

Characteristics:
- **High Recency:** Recent purchases.
- **High Frequency:** Frequent purchases.
- **High Monetary Value:** High spending.

**Segment B: Moderate Value, Moderate Engagement**

Characteristics:
- **Moderate Recency:** Fairly recent purchases.
- **Moderate Frequency:** Moderate purchase frequency.
- **Moderate Monetary Value:** Moderate spending.


**Segment C: Low Value, Low Engagement**

Characteristics:
- **Low Recency:** Less recent purchases.
- **Low Frequency:** Infrequent purchases.
- **Low Monetary Value:** Low spending.


**Segment D: New Customers**

Characteristics:
- **Recent Acquisition:** Newly acquired customers.
- **Undefined Frequency and Monetary Value:** Insufficient data to determine patterns.



<a id="conclusion"></a>
# <b><span style='color:#09ba85'>Step 6 |</span><span style='color:#34e3af'> Conclusion </span></b>
⬆️ [Tabel of Contents](#contents_tabel)


This project has provided a comprehensive analysis of customer behavior through the lens of CRM analytics, focusing on customer segmentation, RFM analysis, and Customer Lifetime Value (CLTV) estimation. Here are the key takeaways and their implications for future strategic decisions:

1. **Customer Segmentation:**
   - The segmentation process revealed four distinct customer segments (A, B, C, D) with varying levels of value and engagement.
   - Segment A consists of high-value, highly engaged customers who contribute significantly to the business's revenue and require personalized strategies to maintain their loyalty.
   - Segment B includes moderately valuable customers with the potential for growth through targeted marketing efforts.
   - Segment C contains low-value, low-engagement customers who are at risk of churning but can be reactivated with specialized campaigns.
   - Segment D represents new customers, highlighting the need for effective onboarding and nurturing strategies to convert them into loyal clients.

2. **RFM Analysis:**
   - RFM analysis provided deep insights into customer purchasing behavior, revealing the importance of recent, frequent, and high-value transactions.
   - These insights guided the development of targeted marketing strategies, ensuring that resources are allocated efficiently to maximize ROI.

3. **CLTV Estimation:**
   - CLTV analysis emphasized the long-term value of customers, helping to prioritize high-potential segments.
   - The analysis supports strategic planning and resource allocation by identifying customers who are likely to contribute the most to future revenue.



             
