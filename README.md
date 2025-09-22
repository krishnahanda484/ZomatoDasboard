Zomato Sales Performance Analysis Dashboard
📖 Project Overview
This project isn't just a collection of charts; it's a strategic tool designed to answer one critical question: How can we turn millions of Zomato orders into clear, simple, and profitable business decisions?

The primary objective is to empower everyone—from a regional manager in Delhi to a C-level executive—to understand sales performance without needing to be a data expert. This dashboard cuts through the noise of raw data, revealing key trends, identifying top-performing areas, and uncovering hidden opportunities at a glance.

🚀 Live Dashboard & PBIX File
The best way to understand this dashboard is to use it. You can download the fully interactive Power BI file (.pbix) from the link below.

➡️ Download the PBIX File: Zomato Dashboard PBIX on Google Drive

(Note: You will need to install the free Microsoft Power BI Desktop application to open and interact with the file.)

🖼️ Dashboard Preview
✨ Key Features & Functionality (Explained for Everyone)
This dashboard was built with a focus on intuitive design and powerful, interactive features. Here’s a breakdown of what each feature does and, more importantly, why it matters.

1. High-Level KPI Cards
What it is: The three large numbers at the top: Total Sales Amount, Total Quantity of items sold, and Total Order Count.

Why it matters: This is the 5-second health check of the business. Without looking at anything else, a manager can instantly know the overall performance, answering the most basic question: "How are we doing?"

2. Dynamic Metric Toggling (Amount vs. Quantity)
What it is: Two simple buttons that switch the entire dashboard's focus between the total money earned (Amount) and the total number of items sold (Quantity).

Why it matters: A business might be selling a huge number of cheap items (high quantity) but not making much money (low amount). This toggle lets us see both sides of the story. It helps us understand if our revenue is driven by high-volume sales or by high-value items.

3. Geospatial Filtering & Analysis
What it is: A search bar to filter by city and a chart showing the top localities.

Why it matters: Zomato is a city-based business. A manager for Delhi doesn't need to see data from Mumbai. This feature allows them to zoom in on their specific area of responsibility, making the data relevant and actionable for them.

4. Dynamic "Top N" Slicers
What it is: Buttons that instantly filter the localities chart to show only the Top 5, 10, 20, 50, or 100 performing areas.

Why it matters: Imagine a list of over 200 neighborhoods. Finding the most important ones is like finding a needle in a haystack. These slicers allow a manager to instantly identify their star performers (the Top 5) or find the areas that need the most attention, without any manual sorting.

5. Trend Analysis Visuals (By Month & Year)
What it is: Line charts showing sales performance over months and years.

Why it matters: This is like a time machine for sales data. The "Sale by Month" chart helps us spot patterns, like a consistent sales dip in August. This isn't a problem; it's a predictable insight. The marketing team can now proactively launch a promotion in July to boost August's numbers.

🛠️ The "Magic" Behind the Dashboard (Technical Deep-Dive)
The dashboard's interactivity is powered by Data Analysis Expressions (DAX) in Power BI. While the user experience is simple, the underlying logic is robust. Here are a few key formulas that make it work.

1. Base Measure for Total Sales
This is the foundational building block. It simply adds up all the values in the 'Amount' column. Every other sales-related calculation is built on this.

Total Sales = 
SUM('Sales'[Amount])

2. Dynamic "Top N" Ranking Measure
This formula acts like a judge in a competition. It looks at all the localities and assigns each one a rank (from #1 downwards) based on their total sales. This is crucial for the "Top N" slicers to work.

Locality Rank = 
RANKX(
    ALLSELECTED('Locations'[Locality]),
    [Total Sales],
    ,
    DESC,
    Dense
)

3. Measure to Filter Visuals based on "Top N" Selection
This is the "bouncer" for the localities chart. It checks the rank of each locality from the formula above. Then, it looks at which "Top N" button the user has clicked (e.g., "Top 10"). If the locality's rank is within that range (10 or less), it lets it into the chart. Otherwise, it's hidden.

Is In Top N = 
VAR SelectedTopN = SELECTEDVALUE('Top N Slicer'[Value], 100) // Default to 100
RETURN
IF(
    [Locality Rank] <= SelectedTopN,
    1,
    0
)

(This measure is then used in the chart's filter pane, set to only show values where the result is 1.)

🚀 How to Use This File
Download: Click the Google Drive link to download the Zomato Dashboard.pbix file.

Install Power BI: Download and install the free Power BI Desktop application.

Open: Open the .pbix file you downloaded.

Interact & Explore: Click on anything! Use the slicers, search for a city, and see how the entire dashboard responds in real-time.
