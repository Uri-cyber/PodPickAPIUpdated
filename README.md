# PodcastAI - AI-Powered Podcast Discovery

A comprehensive podcast discovery platform with AI-powered recommendations using Anthropic's Claude API.

## 🚀 Features

- **AI-Powered Recommendations**: Get personalized podcast suggestions using natural language queries
- **Multiple Interfaces**: 
  - Simple React app
  - Full-featured Next.js application
  - RESTful API server
- **Smart Search**: Describe what you're interested in and get relevant podcast recommendations
- **Modern UI**: Clean, responsive design with Tailwind CSS

## 📁 Project Structure

```
PodcastAI/
├── home/uri/
│   ├── index.js                    # Simple API server (port 3001)
│   └── express-server/
│       ├── index.js                # React app server (port 3000)
│       ├── src/                    # React components
│       ├── public/                 # Static files
│       ├── webpack.config.js       # Webpack configuration
│       └── podpicksai/            # Next.js application
│           ├── pages/             # Next.js pages
│           ├── components/        # React components
│           ├── utils/             # API utilities
│           └── styles/            # CSS styles
```

## 🛠 Setup & Installation

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Anthropic API key

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd PodcastAI
   ```

2. **Install dependencies for all projects**
   ```bash
   # Install API server dependencies
   cd home/uri
   npm install

   # Install React app dependencies
   cd ../express-server
   npm install

   # Install Next.js app dependencies
   cd podpicksai
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cd home/uri/express-server/podpicksai
   cp ../../../.env.example .env.local
   # Edit .env.local and add your Anthropic API key
   ```

## 🚀 Running the Applications

### Start All Services

1. **API Server** (port 3001)
   ```bash
   cd home/uri
   node index.js
   ```

2. **React App** (port 3000)
   ```bash
   cd home/uri/express-server
   npm run build  # Build first
   node index.js
   ```

3. **Next.js PodcastAI App** (port 3000 - alternative to React app)
   ```bash
   cd home/uri/express-server/podpicksai
   npm run dev
   ```

### Available URLs

- **API Server**: `http://localhost:3001`
  - `GET /` - Hello World
  - `GET /api/users` - Sample users data

- **PodcastAI App**: `http://localhost:3000`
  - `/` - Home page with navigation
  - `/basic` - Basic podcast discovery page
  - `/test` - Component test page

## 🔑 API Configuration

1. Get your Anthropic API key from [Anthropic Console](https://console.anthropic.com/)
2. Copy `.env.example` to `.env.local` in the `podpicksai` directory
3. Replace `your-api-key-here` with your actual API key

## 🧪 Usage

1. **Browse Podcasts**: Visit the basic page to see sample podcasts
2. **AI Recommendations**: Use natural language to describe what you're looking for
3. **API Integration**: The app uses Anthropic's Claude API for intelligent recommendations

## 🛠 Built With

- **Frontend**: React, Next.js, Tailwind CSS
- **Backend**: Node.js, Express.js
- **AI**: Anthropic Claude API
- **Build Tools**: Webpack, Babel

## 📝 Development

### Building for Production

```bash
# Build React app
cd home/uri/express-server
npm run build

# Build Next.js app
cd podpicksai
npm run build
npm start
```

## 🔧 Troubleshooting

- **Port conflicts**: Make sure only one app runs on port 3000 at a time
- **API errors**: Verify your Anthropic API key is correctly set in `.env.local`
- **Build issues**: Run `npm install` in each project directory

## 📄 License

This project is licensed under the ISC License.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request