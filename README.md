
# 📘 Gemini AI Image Analyzer

## 📖 Overview
The **Gemini AI Image Analyzer** is a cutting-edge Python-based desktop application that leverages advanced **Gemini AI** for powerful image analysis. This tool offers seamless text extraction from images, leveraging **Google Translate API** for multi-language translation and **pyttsx3** for text-to-speech conversion. 

Whether you're extracting text from an image or translating it into multiple languages, **Gemini AI Image Analyzer** empowers users to easily convert images into readable, translatable, and audible formats. 

The user-friendly **Tkinter** GUI provides a smooth and intuitive experience for anyone looking to process images and audio, making this tool ideal for individuals and professionals alike.

✨ **Key Features**
- **AI-Powered Text Extraction**: Extracts text from images using Gemini AI’s generative models.
- **Multi-Language Translation**: Translates the extracted text into over 50 different languages via Google Translate API.
- **Text-to-Speech**: Converts the extracted or translated text into lifelike speech with **pyttsx3**.
- **Save Results**: Save the extracted, translated text as a text file for future reference.
- **Real-Time Image Processing**: AI-driven processing that provides fast and accurate text extraction and translation.
- **Multi-Threaded Architecture**: Ensures smooth, non-blocking operations for text extraction, translation, and speech synthesis.
- **Responsive GUI**: The application provides an interactive interface with intuitive controls for image upload, language selection, and speech playback.

🛠️ **Technologies Used**
- **Python**: The primary programming language for the project.
- **Gemini AI**: AI-powered image text extraction and analysis.
- **Google Translate API**: Used for translating the extracted text into multiple languages.
- **pyttsx3**: Converts extracted or translated text into human-like speech.
- **Tkinter**: Provides the graphical user interface (GUI) for easy interaction.
- **Pillow**: Used for image manipulation and preparation before processing.
- **threading**: Ensures that text extraction, translation, and speech synthesis run concurrently, without blocking the GUI.

📁 **Folder Structure**
```
📦 Gemini-AI-Image-Analyzer
├── 📂 audiobooks/           # Stores generated MP3 files for text-to-speech output
├── 📄 main.py               # Main application logic, including text extraction, translation, and speech synthesis
├── 📄 requirements.txt      # List of required dependencies for the project
└── 📄 README.md             # Project documentation (this file)
```

📸 **Screenshots**
![Main Window](screenshot_1.png)  
*The main window displaying the image upload, text extraction, translation, and speech playback features.*

## ⚙️ **Installation and Setup**
Follow the instructions below to get **Gemini AI Image Analyzer** up and running on your local machine.

### 1️⃣ Clone the Repository
Clone the repository from GitHub to your local machine:
```bash
git clone https://github.com/your-username/Gemini-AI-Image-Analyzer.git
cd Gemini-AI-Image-Analyzer
```

### 2️⃣ Set Up a Virtual Environment (Optional but Recommended)
Creating a virtual environment ensures that dependencies are isolated from your system Python. Run the following commands:
```bash
python -m venv venv
source venv/bin/activate  # For Linux/MacOS
venv\Scripts\activate     # For Windows
```

### 3️⃣ Install Dependencies
Install the required libraries from `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Application
Once the dependencies are installed, run the application:
```bash
python main.py
```
Upon successful execution, the application window will open, and you’ll be able to start processing images.

## 📚 **How to Use the Application**
The **Gemini AI Image Analyzer** is designed to be simple and intuitive. Here’s a step-by-step guide to using the application:

1. **Launch the Application**: Run `main.py` to open the Gemini AI Image Analyzer GUI.
2. **Upload an Image**: Click the **Choose New Image** button to upload an image file from your computer. 
3. **Extract Text**: The application will automatically extract text from the image using **Gemini AI**. This will be displayed in the results window.
4. **Translate Text (Optional)**: If desired, select a target language and click **Translate Text** to translate the extracted text into the selected language.
5. **Convert Text to Speech**: Click the **Speak Result** button to listen to the extracted or translated text. The speech will be generated in real-time using **pyttsx3**.
6. **Save Results**: You can save the extracted or translated text as a `.txt` file using the **Save Results** button for future reference.

## 📋 **Algorithm**
The following is a step-by-step breakdown of how the application functions:

1️⃣ **Upload Image**
   - The user selects an image file via the file dialog. 
   - The application captures the file path and begins processing the image asynchronously.

2️⃣ **Text Extraction**
   - **Step 1**: The system first tries to extract text from the image using **Gemini AI**.
   - **Step 2**: If text extraction fails, the application uses **OCR (Optical Character Recognition)** for text extraction.
   - **Step 3**: The extracted text is displayed in the results textbox.

3️⃣ **Translation (Optional)**
   - **Step 4**: The user can choose a target language from a list of over 50 languages.
   - **Step 5**: The system translates the extracted text using the **Google Translate API**.
   - **Step 6**: The translated text is displayed in the results textbox.

4️⃣ **Text-to-Speech**
   - **Step 7**: The application uses **pyttsx3** to convert the extracted or translated text into speech.
   - **Step 8**: The speech is played in real-time, and the user can pause, resume, or stop the playback.

5️⃣ **Save Results**
   - **Step 9**: The user can save the extracted or translated text as a `.txt` file using the **Save Results** button.

## 💻 **Code Explanation**
### **main.py**
This file contains the main logic of the application, including:
- Image processing and text extraction with Gemini AI and OCR.
- Language translation using the **Google Translate API**.
- Text-to-speech conversion using **pyttsx3**.
- GUI creation using **Tkinter**.

**Key Functions**
| **Function**                  | **Description**                                                                 |
|-------------------------------|---------------------------------------------------------------------------------|
| `prep_image(image_path)`      | Prepares and processes the uploaded image for analysis.                         |
| `extract_text_from_image()`   | Extracts text from the image using Gemini AI or OCR (if needed).               |
| `translate_text()`            | Translates the extracted text into the selected language.                      |
| `speak_result()`              | Converts the extracted or translated text into speech using **pyttsx3**.       |
| `save_results_to_file()`      | Saves the extracted or translated text as a `.txt` file.                       |

## 📋 **Requirements**
Ensure you have the following dependencies installed:

- **google-generativeai**: To interact with Gemini AI for text extraction.
- **pyttsx3**: For text-to-speech conversion.
- **googletrans**: For translating text to other languages.
- **Pillow**: For image manipulation.
- **tkinter**: For building the GUI.
- **threading**: To enable non-blocking operations.

To install all dependencies, run:
```bash
pip install -r requirements.txt
```

## 📋 **Troubleshooting**
- **Issue**: Image upload results in error.  
  **Solution**: Ensure the image is in a supported format (e.g., PNG, JPEG, or TIFF). If using OCR, ensure the image is clear and contains legible text.

- **Issue**: Text-to-Speech does not work.  
  **Solution**: Ensure **pyttsx3** is properly installed. Check that your system audio is working.

## 🔮 **Possible Enhancements**
- **Language Selection for Speech**: Allow users to select the language for speech synthesis.
- **Customizable Voice Options**: Enable users to adjust the voice properties, such as pitch and rate.
- **Batch Processing**: Allow users to process multiple images at once.
- **Save Translations**: Allow saving of both original and translated texts into separate files.

## 🤝 **Contributing**
Contributions are highly welcome! If you'd like to contribute, follow these steps:

1. Fork the repository.
2. Create a new feature branch: `git checkout -b feature-name`.
3. Make your changes and commit them: `git commit -m "Added feature-name"`.
4. Push to your branch: `git push origin feature-name`.
5. Open a pull request and describe your changes.

## 📝 **License**
This project is licensed under the **MIT License**. See the LICENSE file for more information.

👤 **Author**  
GitHub: [SamirYMeshram](https://github.com/SamirYMeshram)  
Email: [samirYmeshram@gmail.com](mailto:samirYmeshram@gmail.com)
```

