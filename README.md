# Exercise 5: Big Data Visualization in Geoinformatics
## Geospatial Big Data Analysis — Interactive Geospatial Dashboard
**Bharati Vidyapeeth (Deemed to be University), Pune**  
**Institute of Environment Education and Research (BVIEER)**  

* **Course Coordinator:** Dr. Aravinth R  
* **Student Name:** [Your Name]  
* **PRN / Roll No.:** [Your Roll No.]  
* **Date:** August 23, 2026  

---

### Project Overview
This repository contains an interactive spatial dashboard showcasing commuting patterns in the San Francisco Bay Area [2]. Origin-destination data is used to analyze movement between home and work locations [2]. 

The primary visualization is an interactive 3D flow map created using **PyDeck** and the `deck.gl` **ArcLayer** [2]. Additionally, this dashboard contains a secondary interactive visualization—a **Plotly Histogram**—interpreting the distribution of commute flow magnitudes [14, 15]. Together, they are integrated into a single cohesive web dashboard published via **GitHub Pages** [2].

---

### Dataset & Key Variables
The project utilizes the Bay Area commute-route dataset [5]:
* **`lng_h` & `lat_h`**: Home longitude and latitude (Source coordinates) [6]
* **`lng_w` & `lat_w`**: Work longitude and latitude (Target coordinates) [6]
* **`S000`**: Flow magnitude / total job count (determines Arc width and tooltip data) [6]

---

### Key Features
1. **Interactive 3D Arc Map (PyDeck)** [2]:
   * **Spatial Filter**: Constrained strictly to a geographic bounding box focusing on downtown San Francisco [3].
   * **Dynamic Arc Width**: Visual line width is proportional to the job count (`S000`) [2, 11].
   * **Source-Target Color Mapping**: Arcs shift from **Orange-Red** (Home source) to **Green** (Work destination) with custom transparency values [10].
   * **3D Camera Perspective**: Adjusted using pitch (50 degrees) and bearing (45 degrees) to make overlapping routes easy to identify in 3D [11].
   * **Interactive Tooltip**: Displays the exact number of commute jobs when hovering over any individual arc [12].
2. **Commute Flow Distribution (Plotly)** [14, 15]:
   * An interactive histogram showing the distribution of commute flow values (`S000`) to highlight route popularity frequencies [14, 15].
3. **Unified Dashboard Interface (`index.html`)**:
   * A responsive grid layout incorporating both the 3D map and the histogram into an elegant, easy-to-read web template.

---

### Repository Structure
* **`index.html`**: The main entry page of the dashboard which embeds both interactive visuals in a structured grid layout.
* **`arc_layer_map.html`**: The standalone 3D PyDeck Arc map exported from the geospatial workflow [13].
* **`extra_visualization.html`**: The standalone interactive Plotly histogram showing job flow distribution [15].
* **`README.md`**: Project documentation, environment configurations, and setup instructions.

---

### How to Run Locally
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Navigate into the folder and open `index.html` in any web browser to view the interactive dashboard locally.

---

### Live Deployment
The live dashboard is compiled and deployed via **GitHub Pages** [15]. You can access the live, fully interactive version here:  
👉 **[Your Hosted GitHub Pages URL]** [17]
