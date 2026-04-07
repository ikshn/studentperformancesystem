# 📚 Student Performance System

https://ikshn.github.io/studentperformancesystem/

An aesthetic, fully-functional student performance management system built with HTML, CSS, JavaScript, and JSON data storage.

## 🚀 New Features: Login System & Role-Based Access

### Authentication
- **Secure Login**: Users must login before accessing the system
- **Role-Based Access**: Different permissions for Students and Teachers
- **Session Management**: Login state persists across browser sessions

### User Roles

#### 👨‍🎓 Student Access
- **Username**: `student`
- **Password**: `student`
- **Permissions**:
  - View Dashboard (read-only)
  - Take Quizzes
  - View Leaderboard
  - View Achievements
  - View Student Information

#### 👨‍🏫 Teacher Access
- **Username**: `teacher` or `admin`
- **Password**: `teacher` or `admin`
- **Permissions** (All Student permissions plus):
  - Add new students
  - Delete students
  - Create new quizzes
  - Access Analytics section
  - Full student management

## Features

### 1. **Dashboard** 📊
- Display key statistics at a glance
- Total number of students
- Average performance score
- Top performing student
- Total quizzes completed
- Recent student activities and updates

### 2. **Student Management** 👥 (Teacher Only)
- Add new students with their performance scores
- View all students with score visualization
- Beautiful progress bars showing score percentages
- Delete students from the system
- Real-time data persistence using localStorage

### 3. **Quiz Feature** ✅
- Four different quizzes available:
  - Mathematics Basics (5 questions)
  - General Knowledge (5 questions)
  - Science & Technology (5 questions)
  - Java Basic (5 questions)
- Interactive quiz interface with:
  - Step-by-step question progression
  - Multiple choice options
  - Real-time feedback (correct/incorrect answers highlighted)
  - Progress indicator showing current question
  - Automatic score calculation
- Quiz results display with:
  - Final score percentage
  - Number of correct answers
  - Ability to attempt other quizzes
- **Teacher Feature**: Create custom quizzes with multiple questions

### 4. **Performance Analytics** 📈 (Teacher Only)
- Visual representation of student performance
- Bar chart showing all students' scores
- Score table with sorted rankings
- Easy comparison of student performance

### 5. **Additional Features**
- **Student Information & Attendance**: Track quiz attempts and attendance
- **Leaderboard**: Rank students by performance
- **Achievements**: Unlock badges for milestones
- **Dark Mode**: Toggle between light and dark themes
- **Responsive Design**: Works on all device sizes

## Technical Details

### Technologies Used
- **HTML5**: Semantic structure and layout
- **CSS3**: Modern, responsive design with gradients, animations, and flexbox/grid
- **JavaScript**: Full application logic and interactivity
- **JSON**: Data storage in `data.json` and localStorage for persistence

### Data Storage
- Uses browser's **localStorage** for persistent data storage
- JSON format for quiz data and student information
- Automatic data preservation across browser sessions

### Aesthetic Design
- Modern gradient design (Purple & Blue)
- Smooth animations and transitions
- Responsive design for mobile, tablet, and desktop

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (for local development)

### Installation & Usage

1. **Clone or Download** the repository
2. **Open terminal** in the project directory
3. **Start local server**:
   ```bash
   python -m http.server 8000
   ```
4. **Open browser** and navigate to: `http://localhost:8000`
5. **Login** with one of the following credentials:

#### Student Login
- Username: `student`
- Password: `student`
- Role: Student

#### Teacher Login
- Username: `teacher` (or `admin`)
- Password: `teacher` (or `admin`)
- Role: Teacher

### Features by Role

#### For Students:
- ✅ View Dashboard
- ✅ Take Quizzes
- ✅ View Leaderboard
- ✅ View Achievements
- ✅ View Student Information

#### For Teachers:
- ✅ All Student features
- ✅ Add/Delete Students
- ✅ Create New Quizzes
- ✅ Access Analytics
- ✅ Full System Management

## 📱 Screenshots

*(Add screenshots of login page, dashboard, quiz interface, etc.)*
- Professional card-based layout
- Intuitive navigation

## How to Use

### Getting Started
1. Open `index.html` in a modern web browser
2. Start by exploring the Dashboard to see initial statistics

### Adding Students
1. Navigate to the "Students" tab
2. Enter student name and score (0-100)
3. Click "Add Student" button
4. Student will appear in the grid with visual score representation

### Taking a Quiz
1. Navigate to the "Quiz" tab
2. Click on any available quiz to start
3. Read each question carefully and select your answer
4. Receive instant feedback on your selection
5. Progress through all questions
6. View your final score and results
7. Try another quiz or return to dashboard

### Viewing Analytics
1. Navigate to the "Analytics" tab
2. See visual representation of student performance
3. View ranked score table for all students

## Features & Storage

### JSON Storage Structure
```json
{
  "quizzes": [
    {
      "id": 1,
      "title": "Quiz Title",
      "questions": [
        {
          "question": "Question text?",
          "options": ["A", "B", "C", "D"],
          "correct": 0
        }
      ]
    }
  ],
  "students": [
    {
      "id": 1,
      "name": "Student Name",
      "score": 85,
      "quizzesCompleted": 2,
      "lastActivity": "Activity description"
    }
  ]
}
```

### Data Persistence
- All student data is automatically saved to localStorage
- Each student's performance is tracked
- Quiz attempts are recorded and factored into overall score
- Data persists across browser sessions

## Customization

### Add More Quizzes
Edit `script.js` and add new quiz objects to the `quizzesData` array with:
- Unique ID
- Quiz title and description
- Array of questions with options and correct answer index

### Modify Styling
- Edit `style.css` to change colors, fonts, or layout
- All colors use CSS variables concept for easy customization
- Responsive breakpoints included for mobile optimization

### Extend Features
- Add user authentication
- Export student data to CSV
- Add difficulty levels for quizzes
- Implement timed quizzes
- Add progress charts over time

## Browser Compatibility
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Any modern browser with ES6 support and localStorage

## File Structure
```
student-performance/
├── index.html        # Main HTML structure
├── style.css         # Complete styling and animations
├── script.js         # All JavaScript functionality
├── data.json         # Quiz and sample student data
└── README.md         # Documentation
```

## Tips & Tricks
- Data is stored locally in your browser - clearing browser data will reset everything
- Try adding multiple students to see the analytics update
- Each quiz attempt updates student scores (average of attempts)
- Delete specific students to test data management features

## Enjoy Your Performance Management System! 🚀
