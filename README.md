# **Transform YouTube 📹 Transcripts into Impactful Detailed Notes**

## Purpose

This Streamlit application allows users to convert YouTube video transcripts into detailed, summarized notes. It extracts the transcript from a YouTube video, processes it using Google's Generative AI, and provides a concise summary of the video’s content.

[![Streamlit App](https://img.shields.io/badge/Streamlit_App-YouTube_Transcripts_to_Notes-ff69b4.svg?style=for-the-badge&logo=Streamlit)](https://llmyoutubetranscriptstonotes-idrmcgcobzcx4gezvhaw64.streamlit.app/)

## Dependencies

- **Streamlit**: For building the interactive web application.
- **YouTubeTranscriptApi**: For retrieving transcripts from YouTube videos.
- **google.generativeai**: For leveraging Google's Generative AI models.

## Main Functions and Workflow

### 1. **`extract_transcript_details(youtube_video_url)`**
   - **Purpose**: Extracts the transcript text from a specified YouTube video URL.
   - **Implementation**:
     - **Extract video ID**: Retrieves the video ID from the YouTube URL. `# Retrieves the video ID from the YouTube URL.`
     - **Retrieve transcript**: Utilizes `YouTubeTranscriptApi.get_transcript` to fetch the transcript text. `# Utilizes YouTubeTranscriptApi.get_transcript to fetch the transcript text.`
     - **Concatenate text**: Joins all text segments from the transcript into one string. `# Joins all text segments from the transcript into one string.`
     - **Error handling**: Manages errors and exceptions during transcript extraction. `# Manages errors and exceptions during transcript extraction.`

### 2. **`generate_gemini_content(transcript_text, prompt)`**
   - **Purpose**: Generates a summary of the transcript text using Google's Generative AI.
   - **Implementation**:
     - **Initialize model**: Sets up the Google Generative AI model (`gemini-1.5-pro-latest`). `# Sets up the Google Generative AI model (gemini-1.5-pro-latest).`
     - **Generate summary**: Produces a summary based on the provided prompt and transcript text. `# Produces a summary based on the provided prompt and transcript text.`
     - **Return summary**: Outputs the generated summary text. `# Outputs the generated summary text.`

### 3. **Streamlit Interface**
   - **Purpose**: Provides the web interface for user interaction.
   - **Implementation**:
     - **Display title**: **`st.title`** sets the application's title. `# Sets the application's title.`
     - **Text input**: **`st.text_input`** allows users to input the YouTube video link. `# Allows users to input the YouTube video link.`
     - **Display thumbnail**: **`st.image`** shows the video thumbnail (based on the video ID) when a URL is provided. `# Shows the video thumbnail (based on the video ID) when a URL is provided.`
     - **Button**: **`st.button`** triggers transcript processing and summary generation. `# Triggers transcript processing and summary generation.`
     - **Display summary title**: **`st.markdown`** presents the title for the detailed notes section. `# Presents the title for the detailed notes section.`
     - **Output summary**: **`st.write`** displays the video summary. `# Displays the video summary.`

## Usage

1. **Enter YouTube Link**: Users input a YouTube video link in the text field. `# Users input a YouTube video link in the text field.`
2. **Display Thumbnail**: The video’s thumbnail is shown. `# The video’s thumbnail is shown.`
3. **Generate Notes**: Clicking "Get Detailed Notes" starts transcript extraction and summary generation. `# Clicking "Get Detailed Notes" starts transcript extraction and summary generation.`
4. **View Summary**: The application displays the detailed notes derived from the video transcript. `# The application displays the detailed notes derived from the video transcript.`

## Summary

This application uses AI to summarize YouTube video transcripts into impactful notes, enhancing video content accessibility and usability.

## Author

This app was created by `Parthebhan Pari`.

## Notes

- **Gemini Pro Model**: The app utilizes the Gemini Pro model from Google's GenerativeAI API for summaries. `# The app utilizes the Gemini Pro model from Google's GenerativeAI API for summaries.`
- **Internet Connection**: Ensure a stable internet connection to interact with the Gemini Pro model. `# Ensure a stable internet connection to interact with the Gemini Pro model.`
- **API Key Security**: Keep your API key secure to avoid unauthorized access. `# Keep your API key secure to avoid unauthorized access.`

## 🔗 Connect with Me

Feel free to connect with me on LinkedIn:

[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://parthebhan143.wixsite.com/datainsights)

[![LinkedIn Profile](https://img.shields.io/badge/LinkedIn_Profile-000?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/parthebhan)

[![Kaggle Profile](https://img.shields.io/badge/Kaggle_Profile-000?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/parthebhan)

[![Tableau Profile](https://img.shields.io/badge/Tableau_Profile-000?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/parthebhan.pari/vizzes)
