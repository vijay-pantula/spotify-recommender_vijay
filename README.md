# 🎵 Spotify Recommendation System

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.41.1-red?style=flat&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.6.0-orange?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![GitHub last commit](https://img.shields.io/github/last-commit/vijay-pantula/spotify-recommender_vijay)](https://github.com/vijay-pantula/spotify-recommender_vijay/commits/main)

---

## 💡 Overview

This project presents an intuitive web application designed to recommend Spotify tracks. Users can discover new music by inputting a track name, artist, or genre. The system utilizes a K-Nearest Neighbors (KNN) machine learning model, trained on a synthetic dataset of Spotify track features to identify and suggest acoustically similar songs. The entire application is built using Streamlit, offering an interactive and user-friendly experience directly in your web browser.

**Live Demo :** [https://spotify-recommender-vijay-pantula.streamlit.app/]

---

## ✨ Features

* **Track-based Recommendations:** Input a song title to receive a list of similar tracks.
* **Artist-based Recommendations:** Explore other tracks associated with a specified artist.
* **Genre-based Recommendations:** Discover songs belonging to a particular music genre.
* **Interactive UI:** Built with Streamlit for a user-friendly web experience.
* **Pre-trained Model:** Leverages a pre-trained K-Nearest Neighbors model for fast recommendations.

---

## 📸 Screenshots / Demo

![image](https://github.com/user-attachments/assets/6d3086f5-74b0-4f5c-8028-e6e3d300143d)


---

## 🚀 Quick Start

Get the Spotify Recommendation System up and running in a few simple steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/vijay-pantula/spotify-recommender_vijay.git](https://github.com/vijay-pantula/spotify-recommender_vijay.git)
    cd spotify-recommender_vijay
    ```
2.  **Set up the environment:**
    ```bash
    # Create a virtual environment
    python -m venv venv
    # Activate the environment (Windows)
    .\venv\Scripts\activate
    # For macOS/Linux, use: source venv/bin/activate
    # Install dependencies
    pip install -r requirements.txt
    ```
3.  **Run the app:**
    ```bash
    streamlit run app.py
    ```
    The application will automatically open in your default web browser at `http://localhost:8501`.

---

## ⚙️ Detailed Setup and Installation

For a more comprehensive setup guide, including Development Container usage:

### Prerequisites

* **Python 3.8+**: Essential for running the application.
* **Git**: For cloning the repository.
* **Docker Desktop** (Optional, but recommended for Dev Containers): For isolated development environments.

### Option 1: Local Setup

This method involves setting up the environment directly on your local machine.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/vijay-pantula/spotify-recommender_vijay.git](https://github.com/vijay-pantula/spotify-recommender_vijay.git)
    cd spotify-recommender_vijay
    ```
    *If you already have the files locally and pushed them, ensure your command prompt is in the `spotify-recommender_vijay` directory (or wherever your `app.py` resides).*

2.  **Create and Activate a Virtual Environment:**
    It's highly recommended to use a virtual environment to manage project-specific Python packages and avoid conflicts.
    ```bash
    python -m venv venv
    ```
    *Activate the environment:*
    * **On Windows (Command Prompt/PowerShell):**
        ```bash
        .\venv\Scripts\activate
        ```
    * **On macOS/Linux (Bash/Zsh):**
        ```bash
        source venv/bin/activate
        ```
    Your command prompt will preface the path with `(venv)`, indicating the virtual environment is active.

3.  **Install Project Dependencies:**
    All required Python libraries are listed in the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Streamlit Application:**
    ```bash
    streamlit run app.py
    ```
    This command will launch the Streamlit app. Your default web browser should automatically open to `http://localhost:8501`. If not, manually copy and paste this URL into your browser.

### Option 2: Using a Development Container (VS Code Dev Containers / GitHub Codespaces)

This method provides a consistent, isolated, and pre-configured development environment using Docker. It's ideal for quick setup and ensuring all dependencies are met without affecting your local system.

1.  **Install Docker:** Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/) for your operating system.
2.  **Install VS Code (if not already):** Download and install [Visual Studio Code](https://code.visualstudio.com/).
3.  **Install Dev Containers Extension:** In VS Code, navigate to the Extensions view (Ctrl+Shift+X / Cmd+Shift+X), search for "Dev Containers" by Microsoft, and install it.
4.  **Open Project in Container:**
    * Open the cloned project folder (`spotify-recommender_vijay`) in VS Code (`File > Open Folder...`).
    * VS Code will detect the `.devcontainer` folder and prompt you: "Folder contains a Dev Container configuration file. Reopen in Container?". Click **"Reopen in Container"**.
    * If you don't see the prompt, open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P), type "Dev Containers: Reopen in Container", and select it.
5.  **Wait for Setup:** VS Code will now build the Docker image and configure the environment. This process can take several minutes for the initial setup.
6.  **Access the Application:** The `devcontainer.json` is pre-configured to automatically run `streamlit run app.py` and forward port `8501`. A new tab or a preview window within VS Code should open, displaying the Streamlit application. You can also manually open your browser to `http://localhost:8501`.

---

## 📊 Data and Model

* **`spotify_synthetic_data.csv`:** This project relies on a synthetic dataset of Spotify tracks. It includes various numerical audio features (such as `danceability`, `energy`, `loudness`, `tempo`, etc.) and metadata like `track_name`, `artist_name`, and `genre`. This data serves as the foundation for both model training and recommendation generation.
* **`knn.pkl`:** A pre-trained K-Nearest Neighbors (KNN) machine learning model is utilized to find similar tracks. The model was trained on the standardized audio features from `spotify_synthetic_data.csv`. Prior to training, `sklearn.preprocessing.StandardScaler` was applied to normalize the features, which is crucial for distance-based algorithms like KNN.

---

## 📂 Project Structure

![image](https://github.com/user-attachments/assets/a763b2b1-857f-49ff-ac46-e13292526ec3)


---

## 🚀 Future Enhancements

* **Responsive UI Refinement:** Further optimize the Streamlit layout to ensure a seamless and intuitive user experience across all device sizes, especially mobile.
* **Enhanced Error Handling & User Feedback:** Provide more user-friendly messages and intelligent suggestions (e.g., "Did you mean X?" for unfound inputs).
* **Interactive Visualizations:** Integrate charts (e.g., Plotly, Altair) to visually compare audio features of input vs. recommended tracks.
* **Spotify API Integration:** A significant upgrade would be to connect to the official Spotify API to fetch real-time track data, allowing recommendations from Spotify's entire catalog and potentially offering song previews.
* **Advanced Recommendation Algorithms:** Explore and implement more sophisticated recommendation models, such as matrix factorization or deep learning approaches, for potentially higher accuracy.

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements, new features, or encounter any bugs, please feel free to:

1.  **Fork** the repository.
2.  **Create a new branch** (`git checkout -b feature/your-feature` or `bugfix/issue-fix`).
3.  **Make your changes**.
4.  **Commit** your changes with a clear message (`git commit -m 'feat: Add new feature'`).
5.  **Push** to your branch (`git push origin feature/your-feature`).
6.  **Open a Pull Request**.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 📧 Contact

For any questions, feedback, or collaborations, feel free to reach out to [vijay-pantula](https://github.com/vijay-pantula).

---
