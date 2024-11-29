# Logo Maker

This project generates logos using the Hugging Face API.

## Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)
- A Hugging Face API key

## Getting Started

1. **Clone the repository:**

   ```sh
   git clone https://github.com/Karsentiz/logo-maker.git
   cd logo-maker
   ```

2. **Install dependencies:**

   ```sh
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory and add your Hugging Face API key:

   ```env
   HUGGINGFACE_API_KEY=your_hugging_face_api_key
   ```

4. **Run the development server:**

   ```sh
   npm run dev
   ```

   The server will start on `http://localhost:3000`.

## Troubleshooting

- Ensure your Hugging Face API key is correctly set in the `.env` file.
- Check the console for any error messages.

## Deployment

To deploy this project using Firebase, follow these steps:

1. **Install the Firebase CLI:**

   ```sh
   npm install -g firebase-tools
   ```

2. **Login to Firebase:**

   ```sh
   firebase login
   ```

3. **Build the project:**

   ```sh
   npm run build
   ```

4. **Deploy to Firebase:**

   ```sh
   firebase deploy
   ```

### Firebase Environment Variables

To deploy using Firebase, you need to add your Hugging Face API key as a secret in Firebase:

1. Install the Firebase CLI if you haven't already:

   ```sh
   npm install -g firebase-tools
   ```

2. Log in to Firebase:

   ```sh
   firebase login
   ```

3. Set your Hugging Face API key as a secret:

   ```sh
   firebase functions:secrets:set HUGGINGFACE_API_KEY
   ```

4. Deploy your functions:

   ```sh
   firebase deploy --only functions
   ```

### GitHub Actions Environment Variables

To deploy using GitHub Actions, you need to add your Hugging Face API key as a secret in your GitHub repository:

1. Go to your repository on GitHub.
2. Click on `Settings`.
3. Click on `Secrets` in the left sidebar.
4. Click on `New repository secret`.
5. Add a new secret with the name `HUGGINGFACE_API_KEY` and your Hugging Face API key as the value.

## License

This project is licensed under the MIT License.