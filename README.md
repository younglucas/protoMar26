# Blog Calendar

A modern blog website featuring an interactive calendar of blog posts and a topic request system where readers can suggest and vote on topics they'd like to see covered.

## Features

✨ **Interactive Calendar**
- Visual calendar displaying all blog posts
- Navigate between months
- See blog post indicators on calendar dates
- Click on dates to see post details

📝 **Blog Posts Management**
- Display posts organized by date
- View upcoming and past posts
- List of posts for the current month in the sidebar

💡 **Topic Request System**
- Submit requests for blog post topics
- Vote on existing topic requests
- See trending topics with vote counts
- Community-driven content creation

📱 **Responsive Design**
- Works on desktop and mobile devices
- Beautiful gradient UI
- Clean and intuitive interface

## Project Structure

```
younglucas/protoMar26/
├── index.html          # Main HTML file
├── styles.css          # Styling
├── app.js              # Frontend JavaScript logic
├── server.js           # Express.js backend server
├── package.json        # Project dependencies
└── README.md          # This file
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/younglucas/protoMar26.git
cd protoMar26
```

2. Install dependencies:
```bash
npm install
```

## Usage

### Frontend Only (Static)
Simply open `index.html` in your browser to use the calendar and request system with in-memory data.

### Full Stack (with Backend)

1. Start the server:
```bash
npm start
```

2. Open your browser and navigate to:
```
http://localhost:3000
```

The server will run on port 3000 by default (or use PORT environment variable).

## API Endpoints

### Blog Posts
- `GET /api/posts` - Get all blog posts
- `GET /api/posts/:year/:month` - Get posts for specific month
- `GET /api/posts/:id` - Get a specific post
- `POST /api/posts` - Create new post
- `PUT /api/posts/:id` - Update a post
- `DELETE /api/posts/:id` - Delete a post

### Topic Requests
- `GET /api/requests` - Get all topic requests (sorted by votes)
- `POST /api/requests` - Create new request or add vote
- `DELETE /api/requests/:id` - Delete a request

### Health
- `GET /api/health` - API health check

## Example API Requests

### Create a Blog Post
```bash
curl -X POST http://localhost:3000/api/posts \
  -H "Content-Type: application/json" \
  -d '{
    "date": "2026-04-01",
    "title": "My New Blog Post",
    "content": "Post content here..."
  }'
```

### Submit a Topic Request
```bash
curl -X POST http://localhost:3000/api/requests \
  -H "Content-Type: application/json" \
  -d '{
    "topic": "Web Performance Optimization",
    "description": "Tips and tricks for faster websites"
  }'
```

### Get Posts for March 2026
```bash
curl http://localhost:3000/api/posts/2026/03
```

## Sample Data

The application comes with sample blog posts and topic requests:

**Sample Posts:**
- March 5, 2026: Getting Started with Web Development
- March 12, 2026: Advanced JavaScript Patterns
- March 19, 2026: CSS Grid Layout Mastery
- March 26, 2026: React Hooks Deep Dive

**Sample Requests:**
- Machine Learning Basics (45 votes)
- TypeScript for Beginners (32 votes)
- API Design Best Practices (28 votes)

## Technologies Used

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Backend:** Node.js, Express.js
- **Middleware:** CORS, Body Parser

## Development

To run with automatic restart on file changes:
```bash
npm run dev
```

This requires `nodemon` to be installed (included in devDependencies).

## Future Enhancements

- User authentication and accounts
- Email notifications for new posts
- Comment system on posts
- Admin panel for managing posts
- Search functionality
- Tag-based categorization
- Social media integration
- Analytics and engagement metrics

## License

MIT

## Author

younglucas