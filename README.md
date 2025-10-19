# Arens

![Arens Logo](https://res.cloudinary.com/srourera/image/upload/t_100x100/v1759595913/ChatGPT_Image_4_oct_2025_18_38_15_gyw5ul.png)

Arens is a modern, responsive personal assistant web application that provides an intelligent chat interface for managing tasks, reminders, personal memories, and proactive messaging preferences. Built as a Progressive Web App (PWA), it offers a native app-like experience across all devices.

## ✨ Features

### 🤖 AI Chat Interface
- Real-time conversation with an AI personal assistant
- Markdown support for rich text formatting
- Image upload and file sharing capabilities
- Auto-resizing message input with mobile optimization

### 📋 Task Management
- View and manage pending tasks
- Task synchronization across devices
- Real-time updates and notifications

### 📅 Smart Reminders
- Create and manage time-based reminders
- Intelligent time formatting (relative and absolute)
- Automatic sorting by due date
- Visual time indicators

### 🧠 Personal Memory System
- Store and retrieve personal information
- Categorized memory types (Basic/Extra)
- Searchable personal data storage
- Context-aware information retrieval

### 💬 Proactive Messaging
- Configurable proactivity preferences
- Intelligent message timing
- Personalized interaction rules

### 📱 Progressive Web App (PWA)
- Installable on mobile devices
- Offline-ready functionality
- Native app-like experience
- iOS and Android optimized

## 🚀 Getting Started

### Prerequisites
- Modern web browser with JavaScript enabled
- Internet connection for API functionality

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd arens
   ```

2. **Serve the application:**
   Since this is a client-side application, you can serve it using any static file server:

   **Using Python:**
   ```bash
   python -m http.server 8000
   ```

   **Using Node.js (http-server):**
   ```bash
   npx http-server
   ```

   **Using PHP:**
   ```bash
   php -S localhost:8000
   ```

3. **Access the application:**
   Open your browser and navigate to `http://localhost:8000`

### Mobile Installation (PWA)

**On iOS:**
1. Open the app in Safari
2. Tap the Share button
3. Select "Add to Home Screen"

**On Android:**
1. Open the app in Chrome
2. Tap the menu (three dots)
3. Select "Add to Home Screen"

## 🏗️ Architecture

### Frontend Technologies
- **Vue.js 3** - Progressive JavaScript framework
- **Marked.js** - Markdown parser for rich text support
- **Vanilla CSS** - Custom styling with modern CSS features
- **PWA APIs** - Service worker and manifest for app-like experience

### Backend Integration
- RESTful API integration with n8n workflows
- Token-based authentication system
- Real-time data synchronization
- File upload and processing capabilities

### Key Components

#### Main Application (`index.html`)
- **Authentication System**: Token-based login with localStorage persistence
- **Chat Interface**: Real-time messaging with AI assistant
- **User Management**: Profile creation and session management
- **File Handling**: Image upload and processing
- **Responsive Design**: Mobile-first approach with touch optimization

#### User Information Panel (`arens-user-info.html`)
- **Task Display**: Pending tasks with formatting
- **Reminder Management**: Time-based reminders with smart formatting
- **Memory Storage**: Personal data categorization and display
- **Proactivity Rules**: User preference management

## 🔧 Configuration

### Environment Setup
The application connects to external APIs for backend functionality. Key endpoints include:

- **Main Assistant**: `https://n8n.ridaflows.com/webhook/personal-assistant`
- **Messages Sync**: `https://n8n.ridaflows.com/webhook/personal-assistant-messages`
- **Reminders**: `https://n8n.ridaflows.com/webhook/personal-assistant-reminders`
- **Tasks**: `https://n8n.ridaflows.com/webhook/personal-assistant-pending-tasks`
- **Memories**: `https://n8n.ridaflows.com/webhook/personal-assistant-memories`
- **Proactivity**: `https://n8n.ridaflows.com/webhook/personal-assistant-proactivity-rules`

### Authentication
The application uses header-based authentication with the `x-authorization-arens` token.

## 📱 Usage

### First Time Setup
1. Enter your authentication token when prompted
2. Create a user profile with your name and username
3. Start chatting with your personal assistant

### Daily Usage
- **Send Messages**: Type in the chat input and press the send button
- **Upload Images**: Click the image button to share photos
- **View Information**: Click the user info button to see tasks, reminders, and memories
- **Manage Sessions**: Use the logout button to switch users

### Features in Detail

#### Chat Interface
- Supports text messages and image uploads
- Markdown formatting for AI responses
- Auto-scroll to latest messages
- Message timestamps and delivery indicators

#### Task Management
- View pending tasks in the user info panel
- Tasks sync automatically every 30 seconds
- Formatted display with line breaks and styling

#### Reminders System
- Smart time formatting (e.g., "In 5 minutes", "Tomorrow at 3:00 PM")
- Automatic sorting by due date
- Visual indicators for urgency

## 🎨 Customization

### Styling
The application uses a custom CSS design system with:
- **Color Scheme**: Warm browns and oranges (`#cd853f`, `#d2691e`)
- **Typography**: System fonts with careful hierarchy
- **Animations**: Smooth transitions and micro-interactions
- **Responsive Design**: Mobile-first with touch-friendly interfaces

### Theming
Key CSS custom properties can be modified in the `<style>` sections for:
- Primary colors and gradients
- Font sizes and spacing
- Border radius and shadows
- Animation timing and effects

## 🔒 Security

- Token-based authentication with localStorage
- Secure HTTPS API endpoints
- File upload validation and size limits
- XSS protection through proper content handling

## 📊 Performance

### Optimization Features
- Lazy loading of user information
- Efficient message synchronization
- Optimized image handling
- Minimal external dependencies

### Monitoring
- Console logging for debugging
- Error handling for network issues
- Graceful degradation for offline scenarios

## 🤝 Contributing

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly on multiple devices
5. Submit a pull request

### Code Style
- Use semantic HTML structure
- Follow Vue.js best practices
- Maintain responsive design principles
- Include appropriate ARIA labels for accessibility

## 📄 License

This project is private and proprietary. All rights reserved.

## 🆘 Support

For support and questions:
- Check the browser console for error messages
- Ensure stable internet connection
- Verify authentication token validity
- Test on different browsers if issues persist

## 🔄 Updates

The application automatically syncs data every 30 seconds and checks for updates when the browser tab becomes visible again.

---

**Arens** - Your intelligent personal assistant, available wherever you are. 🤖✨