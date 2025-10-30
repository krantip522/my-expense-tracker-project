# Full Stack Expense Tracker
A fully functional web-based expense tracker that includes secure user authentication, efficient expense management, and interactive data visualization. Developed using pure HTML, CSS, and JavaScript to ensure lightweight performance and wide browser compatibility.
# Features:-
## Authentication System:
User Registration: Create new accounts with email and password
Secure Login: Email/password authentication with validation
Session Management: Persistent login state across browser sessions
Form Validation: Real-time validation with error messages
Data Isolation: Each user has separate, private expense data
## Expense Management
Add Expenses: Quick and easy expense entry with categorization
View Expenses: Comprehensive table view with sorting (latest first)
Edit Expenses: In-place editing with modal interface
Delete Expenses: Safe deletion with confirmation dialogs
Real-time Totals: Automatic calculation and display of total expenses
Rich Data: Track category, amount, comments, and timestamps
## User Experience
Modern UI: Clean, professional interface with gradient backgrounds
Responsive Design: Works perfectly on desktop, tablet, and mobile
Tab Navigation: Intuitive tab-based interface for different functions
Loading States: Smooth transitions and feedback messages
Accessibility: Proper form labels and keyboard navigation

## 🚀 Quick Start

### Option 1: Direct Usage
1. **Download** the HTML file
2. **Open** it in any modern web browser
3. **Create an account** or use demo credentials:
   - Email: `demo@example.com`
   - Password: `password123`
4. **Start tracking** your expenses!

### Option 2: Local Development
```bash
# Clone or download the project
git clone <your-repo-url>

# Navigate to project directory
cd expense-tracker

# Open with live server (VS Code extension) or any local server
# Or simply open the HTML file in your browser
```


# Project Structure:-
expense-tracker/
│
├── index.html          # Main application file
├── README.md           # Project documentation
└── assets/             # for additional assets
    ├── screenshots/    # Application screenshots
    └── icons/          # App icons

    ## 💾 Data Storage

The application uses **localStorage** for data persistence:
- **Users Data**: `users` - Array of all registered users
- **Current Session**: `currentUser` - Currently logged-in user
- **User Expenses**: `expenses_<email>` - Individual expense data per user

### Data Structure

#### User Object
```javascript
{
  name: "John Doe",
  email: "john@example.com",
  password: "hashedPassword"
}
```

#### Expense Object
```javascript
{
  id: "1640995200000",
  category: "Food",
  amount: 25.50,
  comments: "Lunch at restaurant",
  createdAt: "12/31/2023, 10:00:00 AM",
  updatedAt: "12/31/2023, 10:00:00 AM"
}
```

## 🎯 Available Categories

- 🍕 **Food** - Meals, groceries, dining out
- 🚗 **Transportation** - Gas, public transport, rideshares
- 🎬 **Entertainment** - Movies, games, subscriptions
- 🛍️ **Shopping** - Clothes, electronics, personal items
- 📄 **Bills** - Utilities, rent, phone bills
- 🏥 **Healthcare** - Medical expenses, prescriptions
- 📚 **Education** - Books, courses, tuition
- 📦 **Other** - Miscellaneous expenses

## 🛠️ Technical Details

### Dependencies
- **Chart.js 3.9.1** - For pie chart visualization (loaded from CDN)
- **Modern Web Browser** - With localStorage support

### Browser Compatibility
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
  
## 📱 Responsive Design

The application is fully responsive and optimized for:
- **Desktop** (1200px+) - Full featured interface
- **Tablet** (768px - 1199px) - Adapted layout
- **Mobile** (< 768px) - Optimized for touch interaction

## 🔒 Security Features

- **Client-side Authentication** - Basic email/password validation
- **Data Isolation** - Users can only access their own data
- **Form Validation** - Input sanitization and validation
- **Password Confirmation** - Ensures password accuracy during signup

> **Note**: This is a client-side application suitable for personal use. For production use with multiple users, implement server-side authentication and database storage.

## 🎨 Customization

### Adding New Categories
Edit the category dropdown in the HTML:
```html
<select id="category" required>
    <option value="YourCategory">Your Category</option>
    <!-- Add more categories here -->
</select>
```

### Styling Modifications
The CSS uses CSS custom properties for easy theming:
```css
:root {
    --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    --success-color: #28a745;
    --danger-color: #dc3545;
}
```

### Chart Customization
Modify the Chart.js configuration in the `updateChart()` function:
```javascript
// Custom colors for chart segments
const colors = [
    '#FF6384', '#36A2EB', '#FFCE56', '#4BC0C0',
    // Add your custom colors here
];
```

## 🐛 Troubleshooting

### Common Issues

**Q: My data disappeared after closing the browser**
A: Ensure your browser allows localStorage and isn't in private/incognito mode.

**Q: Charts not displaying properly**
A: Check that Chart.js CDN is accessible and loading properly.

**Q: Can't login with correct credentials**
A: Clear your browser's localStorage or check browser console for errors.

**Q: Application not responsive on mobile**
A: Ensure you're using a modern browser with proper viewport support.

### Browser Console Debugging
Open developer tools (F12) and check the console for any error messages.

## 🚀 Deployment

### GitHub Pages
1. Upload the HTML file to a GitHub repository
2. Go to Settings > Pages
3. Select source branch
4. Access your app at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop the HTML file to Netlify
2. Get instant deployment with custom domain options

### Local Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

## 📈 Future Enhancements

### Planned Features
- [ ] **Export Data** - CSV/Excel export functionality
- [ ] **Import Data** - Bulk import from files
- [ ] **Budget Tracking** - Set and monitor budgets per category
- [ ] **Recurring Expenses** - Support for monthly/weekly recurring items
- [ ] **Multi-currency** - Support for different currencies
- [ ] **Dark Mode** - Toggle between light and dark themes
- [ ] **Advanced Analytics** - Monthly trends and spending patterns
- [ ] **Data Backup** - Cloud sync capabilities

### Technical Improvements
- [ ] **PWA Support** - Make it installable as a mobile app
- [ ] **Offline Mode** - Work without internet connection
- [ ] **Performance** - Virtual scrolling for large datasets
- [ ] **Security** - Enhanced client-side encryption
- [ ] **Testing** - Unit and integration tests

## 🤝 Contributing

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request


<div align="center">

**Made with ❤️ for better expense tracking**

[⭐ Star this repo](https://github.com/your-username/expense-tracker) if you found it helpful!

</div>
