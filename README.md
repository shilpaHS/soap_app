# SOAP App - Full Stack Application for SOAP Note Generation

## Overview

This is a full-stack web application that records a conversation between a clinician and a patient, processes the audio to generate a structured SOAP note using OpenAI Assistant services.

### Features:
- Audio recording with start, pause, resume, and stop functionality.
- Speech-to-text conversion using third-party APIs (Google Cloud, AssemblyAI, Deepgram, etc.).
- SOAP Note generation via OpenAI API.
- User-friendly interface with real-time transcription and SOAP note display.
- Embeddable application using an iframe.
  
---

## Project Structure

```text
soap-app/
├── soap-node/                # Backend
│   ├── server.js             # Main server file
│   ├── .gitignore            # Git ignore file for backend
│   ├── package.json          # Backend dependencies and scripts
│   ├── .env                  # Backend environment variables
│
└── soap-react/               # Frontend
    ├── public/               # Public assets
    ├── src/                  # React components and frontend logic
    ├── App.js                # Main React component
    ├── components/           # Components for AudioRecorder, Transcription, SOAPNote
    ├── .gitignore            # Git ignore file for frontend
    ├── package.json          # Frontend dependencies and scripts
    ├── index.css             # Main CSS file
    └── .env                  # Frontend environment variables

```
---

## Setup Instructions

### Prerequisites

Make sure you have Node.js installed. You can download it from [here](https://nodejs.org/).

You will also need access to:
- **Speech-to-Text API** (AssemblyAI)
- **OpenAI API** (for SOAP note generation)

### Environment Variables

#### Backend (.env)
OPENAI_API_KEY=<your_openai_api_key> 
SPEECH_TO_TEXT_API_KEY=<your_speech_to_text_api_key>



#### Frontend (.env)
REACT_APP_API_URL=<your_backend_api_url>



---

### Backend Setup (soap-node)

1. Clone the repository:
    ```bash
    git clone https://github.com/shilpaHS/soap-node.git
    cd soap-app/soap-node
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Set up environment variables:
    - Create a `.env` file and add API keys.

4. Start the backend server:
    ```bash
    node server.js
    ```

   The backend will run on `http://localhost:8081`.

### Frontend Setup (soap-react)
1. Clone the repository:
   ```bash
   git clone https://github.com/shilpaHS/soap_react
   ```

2. Navigate to the `soap_react` folder:
    ```bash
    cd soap-app/soap_react
    ```

3. Install dependencies:
    ```bash
    npm install
    ```

4. Set up environment variables:
    - Create a `.env` file with the backend API URL:
    ```
    REACT_APP_API_URL=http://localhost:3000
    ```

5. Start the frontend server:
    ```bash
    npm start
    ```

   The frontend will run on `http://localhost:3000`.

---

## Usage

1. **Audio Recording**: Use the buttons to start, pause, resume, and stop recording.
2. **Speech-to-Text**: Once the recording is stopped, the audio is sent to the backend for transcription.
3. **SOAP Note Generation**: After transcription, generate the SOAP note using the **Generate SOAP Note** button.

---

## Deployment

### Backend Deployment

**Render**.

### Frontend Deployment

 **Netlify**.

---
## Embedding in an Iframe

To embed this application in an iframe, use the following HTML snippet:

```html
<iframe 
  src="https://678a0a496c9281e1906927bf--shilpahs.netlify.app" 
  allow="microphone" 
  width="100%" 
  height="600px" 
  frameborder="0">
</iframe>

```
---

## Live Demo

You can view a live demo of the application here:
- **Backend**: [https://soap-node.onrender.com]
- **Frontend**: [https://678a0a496c9281e1906927bf--shilpahs.netlify.app/]

---

## Contributing

Feel free to fork the project, submit issues, and pull requests. Contributions are always welcome!

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



