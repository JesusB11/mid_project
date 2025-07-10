# Trendify

## Introduction

This project, "Trendify," utilizes Spotify European daily top 50 data from 2021 and 2024 to identify trending artists. Our primary goal was to pinpoint artists who demonstrated significant growth in popularity over this period. We then delved deeper to identify the top 5 songs of one selected artist in both 2021 and 2024, analyzing his/her popularity across different European countries. This information was crucial for determining five optimal European countries where the identified artist could potentially have a successful tour in 2025.

## Data Used

We used two datasets sourced from Kaggle:
* **"Top Spotify Songs in 73 Countries (Daily Updated)"**: This dataset provided granular daily rank information across a wide range of countries.
* **"Spotify Charts"**: This dataset complemented our analysis by offering additional chart data.

**Comments on the Data:**
* **Main Challenges:** A significant challenge encountered was handling special characters present in the data. Being European-focused, the datasets contained many languages (e.g., Ukranian, Icelandic, Polish) with characters that were not readily recognized by SQL Workbench, requiring specific handling.
* **Strengths:** The datasets proved to be very precise, notably free of blanks and duplicates, and were well-organized, making them easy to understand and work with.
* **Weaknesses:** The main limitation of the data was its incompleteness regarding European countries. Several EU member states, such as Slovakia, Slovenia, and Croatia, were notably missing from the datasets, which limited the comprehensive scope of our European analysis.

## Questions and Conclusions

### Topic: Artists with Potential

* **Question 1:** Which trending artist from 2021 could have a successful tour in 2025?
    * **Conclusion:** Based on the comprehensive analysis of Spotify's daily top 50 data from 2021 and 2024, Billie Eilish emerged as the artist with the most significant and consistent growth, indicating strong potential for a successful European tour in 2025.

### Topic: Tour Destinations

* **Question 1:** In which countries from 2021 and 2024 was the artist still or more famous that can be considered for possible tour destination?
    * **Conclusion:** According to the results of the study, the top six countries identified as prime destinations for Billie Eilish's European tour in 2025 are Lithuania, Latvia, the UK, Belgium, Ireland, and Estonia. Her consistent popularity and sustained growth in these specific regions across both 2021 and 2024 make them ideal choices for tour stops.

## Methodology

Our methodology involved several key steps, focusing on filtering, data cleaning, and analytical visualization:

1.  **Data Acquisition:** Datasets were downloaded from Kaggle, specifically focusing on daily Spotify chart data.
2.  **Data Filtering:** The initial step in data preparation involved filtering the large datasets to create a relevant sub-dataset containing only European cities and their daily rank data for the years 2021 and 2024.
3.  **Data Cleaning (Character Handling):** A significant part of our data cleaning involved addressing special characters from various European languages (e.g., Russian, Polish) that were not recognized by SQL Workbench. This required replacing these characters and, in some cases, translating titles into English or converting them to ASCII format to ensure data consistency and readability across our tools. We used Python libraries `unidecode` and `unicodedata` for this purpose.
4.  **Analysis Techniques:**
    * We utilized **bar charts** to visually represent the popularity and importance of the identified artist (Billie Eilish) across different countries and their songs.
    * A **line graph** was employed to effectively illustrate the growth trajectory of the artist's popularity from 2021 to 2024, providing a clear visual representation of their trending status.
5.  **Tools and Libraries:**
    * **Python:** The primary programming language for data manipulation and analysis.
    * **Pandas:** Essential for data loading, cleaning, and transformation.
    * **Matplotlib / Seaborn:** Used for creating various visualizations (bar charts, line graphs).
    * **unidecode & unicodedata:** Python libraries crucial for handling and normalizing special characters.
    * **SQL Workbench:** Used for initial data exploration and potential querying.

## Overall Conclusions

The main takeaway from this project is the remarkable growth of Billie Eilish as an artist within the European Spotify landscape from 2021 to 2024. Her consistent presence and ascent in the daily top 50 rankings across multiple countries highlight her expanding global appeal. This project underscored the importance of dynamic data analysis for understanding artist trends. It also led us to reflect on how our conclusions might have differed or evolved with access to more comprehensive or granular comparison data.

## Further Questions

* Why do artists like Maneskin or other Eurovision winners, despite receiving massive international exposure through the TV show, often not sustain significant growth and remain relatively "one-hit wonders" in terms of broader chart performance?
* What are potential next steps or areas for future analysis/expansion of this project?
    * It would be highly interesting to perform a similar analysis specifically for past Eurovision winners and top participants to identify their long-term trending patterns post-contest.

## Links

* **Data Sources:**
    * [Top Spotify Songs in 73 Countries (Daily Updated)](https://www.kaggle.com/datasets/asaniczka/top-spotify-songs-in-73-countries-daily-updated/data)
    * [Spotify Charts](https://www.kaggle.com/datasets/dhruvildave/spotify-charts/data)
* **Trello Board:** [Spotify Tour Project Trello Board](https://trello.com/b/i0wdhH8F/spotify-tour-project)
* **Presentation:** [Google Colab Presentation](https://docs.google.com/presentation/d/1N6PosQo2AGtNTJx98rD2QM_jEfVM7YWYEgzCExInQi0/edit?slide=id.g362fee7ff31_0_0#slide=id.g362fee7ff31_0_0)