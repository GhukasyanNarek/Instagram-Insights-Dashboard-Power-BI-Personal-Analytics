# Instagram Insights Dashboard — Power BI Personal Analytics

This project is a data analytics dashboard built using Microsoft Power BI, analyzing personal Instagram data downloaded via Meta's data export tool. It demonstrates the full pipeline of data modeling, DAX development, and visual analytics using a star schema.

## 🔍 Project Overview

The dashboard explores two main areas of user activity on Instagram:

1. **Connections and Follow Activity** — summarizing interactions such as followers gained, close friends added, and removed suggestions.
2. **Story Interactions** — covering how the user engaged with story polls, quizzes, sliders, and likes.

## 🧩 Data Model

The data is structured in a **star schema** with the following components:

### Fact Tables
- `FactActivity`: Contains interactions like followers, close friends, and removed suggestions.
- `FactStoryActivity`: Records all story-based interactions (polls, quizzes, likes, sliders).

### Dimension Tables
- `DimUser`: Metadata about users interacted with.
- `DimActivityType`: Types of user-related activities.
- `DimStoryTypeID`: Types of story interactions.
- `DimDate`: Standard date attributes for slicing and aggregation.

## 📊 Visualizations

- **Trend Visualizations**: Line charts showing new followers over time.
- **Categorical Visuals**: Pie and bar charts summarizing types of activities.
- **Tabular Views**: Tables displaying aggregated interaction details.
- **Interactive Slicers**: Filters by date, activity type, and story type, including dynamic defaults.

## 🛠 Features & Techniques

- Developed using both **Advanced Editor (M)** and **Power Query interface** to contrast modeling techniques.
- Applied diverse **DAX Measures**:
  - Aggregations
  - Relationship-aware calculations
  - Time intelligence functions
- Used **calculated columns** for custom time-of-day classification and user categorization.
- Created a **dedicated measure table** for clarity and reusability.
- Implemented **static vs dynamic visuals**, keeping some insights always visible regardless of filter state.

<pre><code>## 📁 Project Structure

```
📁 Instagram-PowerBI-Dashboard/
├── BI_main.pbix                         # Power BI dashboard file
├── PowerBI_InstagramActivityMetadata.pdf  # Metadata and design explanation
├── raw_data/                          # Contains downloaded Instagram archive files
│   └── [extracted .json or .csv files]
```
</code></pre>


## Instructions
Since this project is based on my personal Instagram archive, I am not able to share the raw_data/ folder due to privacy and data protection reasons.

## 📊 Demonstration

<p align="center">
  <img src="https://github.com/user-attachments/assets/ce8baff7-3bdf-4ca9-bbc6-471afc3b5205" 
       alt="Relationship Schema" width="700"/>
</p>
<p align="center">
  <em>Figure 1: One-to-Many schema connecting dimension tables (User, Date, ActivityType, StoryTypeID) to fact tables (Activity, StoryActivity).</em>
</p>


<p align="center">
  <img src="https://github.com/user-attachments/assets/99427bd5-d1b3-42a7-b687-add9d07bc651" 
       alt="Connections and Activity Dashboard" width="700"/>
</p>
<p align="center">
  <em>Figure 2: Summary of connections and follow activities — including followers, close friends, and removed suggestions, along with trend analysis by year and a slicer that helps to filter the data.</em>
</p>


<p align="center">
  <img src="https://github.com/user-attachments/assets/cec428a9-54bc-41ac-9159-1c54de0c941d" 
       alt="Story Interactions" width="700"/>
</p>
<p align="center">
  <em>Figure 3: Story interaction insights categorized by type (polls, quizzes, sliders, likes) and user-based engagement, alongside two slicers that filter by date and story type.</em>
</p>




## 📌 Author

- **Narek Ghukasyan**
- February 2025

## 📜 License

This repository is for educational purposes only. The Instagram data used here is privately owned and not to be redistributed.

---

Feel free to use this as inspiration for your own personal data projects!
