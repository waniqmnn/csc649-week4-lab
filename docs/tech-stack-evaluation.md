# Tech Stack Evaluation

## Project

Microplastic Detection and Quantitative Analysis System using Microscopic Image Processing

## Requirements that drive the decision

- FR-01: The system must allow users to upload microscopic images of water samples for analysis.
- FR-02: The system must detect visible particles and calculate their count and image-based measurements.
- FR-03: The system must display analysis results and support comparisons between samples.
- NFR-01: The system must provide a clear and easy-to-use web interface.
- NFR-02: The system must be developed within the project timeline and with minimal hosting costs.

## Options

- Option A: Static website using HTML, CSS and JavaScript on GitHub Pages.
- Option B: Python Flask web application with OpenCV, machine learning and SQLite on Render.
- Option C: Python Streamlit web application with OpenCV and machine learning on Streamlit Community Cloud.

## Decision matrix

Weight: how important the criterion is for YOUR project (1 = low, 5 = high).

Score: how well each option does (1 = poor, 5 = excellent).

Weighted score = weight x score. Add them up for each option.

| Criterion | Weight | A score | B score | C score |
|------------------------------------|--------|---------|---------|---------|
| Fits my requirements | 5 | 2 | 5 | 4 |
| Skills I already have | 4 | 5 | 4 | 4 |
| Time to build before my deadline | 5 | 5 | 3 | 5 |
| Free hosting and tools | 4 | 5 | 4 | 5 |
| Performance and security needs | 4 | 2 | 3 | 3 |
| Room to grow later | 3 | 2 | 5 | 3 |
| **Total (weighted)** | | **84** | **95** | **98** |

## Decision record

- **Context:** The project requires a web application that can accept microscopic images, detect visible particles, calculate measurements and display analysis results. The project has a limited timeline and budget, with no guaranteed access to laboratory equipment.

- **Decision:** Option C, a Python Streamlit web application with OpenCV and a suitable machine learning model, hosted on Streamlit Community Cloud.

- **Reasons:** Option C achieves the highest weighted score of 98. Streamlit provides a straightforward way to build image-upload functions and display analysis results. Python also supports the image processing and machine learning libraries required by the project. Its free hosting option suits the project's limited budget.

- **Consequences:** Image uploads, particle measurements and sample comparisons should be easier to develop. However, Streamlit offers less flexibility for a customised interface than Flask. Large images or complex models may also require more processing time and memory.

- **Risks and next review:** Free hosting may have limited memory, processing capacity and availability. I will test the selected model with the public dataset and review its processing time and deployment requirements before finalising the technology stack. I would reconsider Flask if the project needs a more customised interface or greater control over the backend.