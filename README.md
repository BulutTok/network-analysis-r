
# Asheville Airbnb Network Analysis

## Overview

This repository contains an R Markdown document, **Visualizing a Network.Rmd**, that demonstrates how to perform network analysis and visualization on Airbnb review data from Asheville. The analysis uses the dataset **asheville_reviews.csv** to explore relationships between Airbnb guests and listings. The workflow covers data import, cleaning, network construction, static visualization, and interpretation of key network metrics.

## Data Description

The dataset, **asheville_reviews.csv**, contains Airbnb reviews for properties in Asheville. Key columns include:

- **review_id:** Unique identifier for each review.
- **user_id:** Unique identifier for the guest who submitted the review.
- **listing_id:** Unique identifier for the Airbnb property.
- **date:** The date when the review was posted.
- **rating:** Numerical rating given to the listing (commonly on a scale from 1 to 5).
- **review_text:** The textual content of the review.
- **Additional Metadata:** Other relevant fields (such as property type, neighborhood, etc.). *(Adjust the descriptions according to your actual dataset.)*

## Project Workflow

### 1. Data Import and Preparation
- **Loading Data:**  
  The R Markdown file reads the CSV file using functions such as `read.csv()` or `readr::read_csv()`.
- **Data Cleaning:**  
  Steps include handling missing values, formatting date fields, and filtering records to focus on the most relevant data.
- **Preprocessing:**  
  The data is structured to enable network analysis by linking reviews to both guests and Airbnb listings.

### 2. Network Construction
- **Defining Nodes and Edges:**  
  - **Nodes:** Represent users (guests) and Airbnb listings.  
  - **Edges:** Represent interactions (e.g., a user reviewing a listing).
- **Graph Creation:**  
  The `igraph` package is used to build and analyze the network.

### 3. Network Visualization
- **Static Visualizations:**  
  The project creates publication-quality static network plots using the `ggraph` package. These visualizations highlight the structure of the network and key relationships between nodes.

### 4. Analysis and Results
- **Network Metrics:**  
  - **Degree Centrality:** Identifies the most connected guests or listings.  
  - **Betweenness Centrality:** Highlights nodes that act as bridges within the network.  
  - **Community Detection:** Uncovers clusters or groups that may indicate popular neighborhoods or active user groups.
- **Key Findings:**  
  - Identification of influential Airbnb listings and highly active users.
  - Discovery of community structures that reveal guest behavior trends and neighborhood popularity.
- **Visualization Outputs:**  
  The document includes several static plots and summary tables that detail these findings.

## Requirements

### Software
- **R** (version 3.6 or higher)
- **RStudio** (recommended for an enhanced development environment)

### R Packages

Before running the analysis, install the following packages if they are not already available:
```r
install.packages("tidyverse")    # For data manipulation and visualization
install.packages("igraph")       # For network analysis
install.packages("ggraph")       # For static network visualization
install.packages("rmarkdown")    # For rendering the R Markdown document
```

## How to Run

1. **Clone or Download the Repository:**
   ```bash
   git clone https://github.com/yourusername/ashville-airbnb.git
   ```
2. **Open in RStudio:**
   - Launch RStudio and open the file **Visualizing a Network.Rmd**.
3. **Knit the Document:**
   - Click on the **Knit** button in RStudio to render the document into HTML, PDF, or another supported format.
4. **Explore the Results:**
   - Review the network visualizations and analysis results presented in the output document.

## File Structure

```
ashville-airbnb/
│
├── Visualizing a Network.Rmd   # Main R Markdown file for network analysis
├── asheville_reviews.csv        # Airbnb reviews dataset for Asheville
└── README.md                    # This detailed README file
```

## Contact

For questions, feedback, or contributions, please reach out to:

**Bulut Tok**  
Email: buluttok2013@gmail.com

## Acknowledgements

- **RStudio:** For providing a robust development environment.
- **igraph:** For enabling comprehensive network analysis.
- **ggraph:** For facilitating elegant static network visualizations.

