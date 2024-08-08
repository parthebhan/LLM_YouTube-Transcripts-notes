# **Transform YouTube 📹 Transcripts into Impactful Detailed Notes**


### Purpose

This Streamlit application enables users to transform YouTube video transcripts into detailed, summarized notes. It extracts the transcript from a YouTube video, processes it using Google's Generative AI, and provides a concise summary of the video’s content.

[![Streamlit App](https://img.shields.io/badge/Streamlit_App-YouTube_Transcripts_to_Notes-ff69b4.svg?style=for-the-badge&logo=Streamlit)](https://llmyoutubetranscriptstonotes-idrmcgcobzcx4gezvhaw64.streamlit.app/)

### Dependencies

- **Streamlit**: For creating the interactive web application.
- **YouTubeTranscriptApi**: For fetching transcripts from YouTube videos.
- **google.generativeai**: For accessing Google's Generative AI models.

### Main Functions and Workflow

#### 1. **`extract_transcript_details(youtube_video_url)`**
   - **Purpose**: Extracts the transcript text from a given YouTube video URL.
   - **Implementation**:
     - **Extract video ID**: Extracts the video ID from the YouTube URL. `# Extracts the video ID from the YouTube URL.`
     - **Retrieve transcript**: Uses `YouTubeTranscriptApi.get_transcript` to retrieve the transcript text. `# Uses YouTubeTranscriptApi.get_transcript to retrieve the transcript text.`
     - **Concatenate text**: Concatenates all text segments from the transcript into a single string. `# Concatenates all text segments from the transcript into a single string.`
     - **Error handling**: Handles exceptions and errors during transcript retrieval. `# Handles exceptions and errors during transcript retrieval.`

#### 2. **`generate_gemini_content(transcript_text, prompt)`**
   - **Purpose**: Generates a summary of the transcript text using Google’s Generative AI.
   - **Implementation**:
     - **Initialize model**: Initializes the Google Generative AI model (`gemini-1.5-pro-latest`). `# Initializes the Google Generative AI model (gemini-1.5-pro-latest).`
     - **Generate summary**: Generates a summary based on the provided prompt and the transcript text. `# Generates a summary based on the provided prompt and the transcript text.`
     - **Return summary**: Returns the generated summary text. `# Returns the generated summary text.`

#### 3. **Streamlit Interface**
   - **Purpose**: Sets up the web interface for user interaction.
   - **Implementation**:
     - **Display title**: **`st.title`** displays the title of the application. `# Displays the title of the application.`
     - **Text input**: **`st.text_input`** provides a field for users to enter the YouTube video link. `# Provides a field for users to enter the YouTube video link.`
     - **Display thumbnail**: **`st.image`** shows a thumbnail image of the YouTube video (based on the video ID) when a URL is provided. `# Shows a thumbnail image of the YouTube video (based on the video ID) when a URL is provided.`
     - **Button**: **`st.button`** triggers the processing of the YouTube transcript and generates the summary when clicked. `# Triggers the processing of the YouTube transcript and generates the summary when clicked.`
     - **Display summary title**: **`st.markdown`** displays the title for the detailed notes section. `# Displays the title for the detailed notes section.`
     - **Output summary**: **`st.write`** outputs the generated summary of the video. `# Outputs the generated summary of the video.`

### Usage

1. **Enter YouTube Link**: Users enter a YouTube video link in the text input field. `# Users enter a YouTube video link in the text input field.`
2. **Display Thumbnail**: A thumbnail image of the video is displayed. `# A thumbnail image of the video is displayed.`
3. **Generate Notes**: Clicking the "Get Detailed Notes" button initiates transcript extraction and summary generation. `# Clicking the "Get Detailed Notes" button initiates transcript extraction and summary generation.`
4. **View Summary**: The application displays the detailed notes based on the transcript of the video. `# The application displays the detailed notes based on the transcript of the video.`

### Summary

This application leverages AI to summarize YouTube video transcripts into impactful notes. It provides a seamless way to extract, process, and summarize video content, enhancing the accessibility and usability of video information.

### Author

This app was created by `Parthebhan Pari`.

### Notes

- **Gemini Pro Model**: The app uses the Gemini Pro model from Google's GenerativeAI API to generate summaries. `# The app uses the Gemini Pro model from Google's GenerativeAI API to generate summaries.`
- **Internet Connection**: Ensure you have a stable internet connection to interact with the Gemini Pro model. `# Ensure you have a stable internet connection to interact with the Gemini Pro model.`
- **API Key Security**: Handle and store your API key securely to prevent unauthorized access. `# Handle and store your API key securely to prevent unauthorized access.`



## 🔗 Connect with Me

Feel free to connect with me on LinkedIn:

[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://parthebhan143.wixsite.com/datainsights)

[![LinkedIn Profile](https://img.shields.io/badge/LinkedIn_Profile-000?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/parthebhan)

[![Kaggle Profile](https://img.shields.io/badge/Kaggle_Profile-000?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/parthebhan)

[![Tableau Profile](https://img.shields.io/badge/Tableau_Profile-000?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/parthebhan.pari/vizzes)
