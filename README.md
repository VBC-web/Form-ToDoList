# 🚀 Productivity Hub

**Your all-in-one contact and task manager built with modern web technologies.**

## 📋 Overview

Productivity Hub is a sleek, modern single-page application that combines a professional contact form with a dynamic task management system. Built with vanilla HTML, CSS, and JavaScript, this project demonstrates advanced front-end development skills including responsive design, form validation, and interactive DOM manipulation.

## ✨ Features

### 📧 Contact Form
- **Smart Validation**: Real-time form validation with visual feedback
- **Email Verification**: Regex-based email format validation
- **Character Counter**: Dynamic character count for message field (500 max)
- **Success Notifications**: User-friendly confirmation messages
- **Error Handling**: Clear error states with descriptive messages

### ✅ Task Management
- **Add Tasks**: Intuitive task creation with Enter key support
- **Task Actions**: Complete, edit, and delete tasks seamlessly
- **Smart Filtering**: View All, Pending, or Completed tasks
- **Interactive UI**: Checkbox toggles and smooth animations
- **Persistent State**: Tasks maintained during session

### 🎨 Design & UX
- **Modern Dark Theme**: Purple gradient design with glassmorphism effects
- **Responsive Layout**: CSS Grid and Flexbox for all screen sizes
- **Smooth Animations**: Hover effects and micro-interactions
- **Custom Scrollbar**: Styled scrollbars matching the theme
- **Accessibility**: Semantic HTML and keyboard navigation support

## 🛠️ Technologies Used

- **HTML5**: Semantic markup and form elements
- **CSS3**: 
  - Grid and Flexbox layouts
  - Custom properties and gradients
  - Animations and transitions
  - Media queries for responsiveness
- **JavaScript ES6+**:
  - Class-based architecture
  - DOM manipulation
  - Event handling
  - Form validation
  - Local state management

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required!

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/vikaschoudhary/productivity-hub.git
   ```

2. **Navigate to project directory**
   ```bash
   cd productivity-hub
   ```

3. **Open in browser**
   ```bash
   # Simply open index.html in your preferred browser
   # Or use a local server:
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

## 📁 Project Structure

```
productivity-hub/ 
│
├── index.html          # Main HTML file with embedded CSS and JS
├── README.md           # Project documentation

```


## 🎯 Key Learning Objectives

This project demonstrates proficiency in:

1. **HTML Forms**: Various input types, validation attributes, and semantic structure
2. **CSS Layouts**: Modern layout techniques with Grid and Flexbox
3. **Responsive Design**: Mobile-first approach with media queries
4. **JavaScript DOM**: Dynamic content manipulation and event handling
5. **Form Validation**: Client-side validation with regex patterns
6. **User Experience**: Smooth animations and intuitive interactions

## 🌟 Features Showcase

### Form Validation
```javascript
validateField(field) {
    const formGroup = field.parentElement;
    let isValid = true;

    if (field.type === 'email') {
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        isValid = field.value.trim() !== '' && emailRegex.test(field.value);
    } else {
        isValid = field.value.trim() !== '';
    }

    // Visual feedback implementation
    formGroup.classList.toggle('error', !isValid);
    return isValid;
}
```

### Task Management
```javascript
addTask() {
    const text = this.taskInput.value.trim();
    if (!text) return;

    const task = {
        id: Date.now(),
        text: text,
        completed: false,
        createdAt: new Date()
    };

    this.tasks.push(task);
    this.renderTasks();
}
```

## 📱 Responsive Design

The application is fully responsive and works seamlessly across:
- **Desktop**: Full two-column layout
- **Tablet**: Optimized spacing and interactions
- **Mobile**: Single-column stack with touch-friendly buttons

## 🎨 Color Palette

```css
:root {
    --primary-gradient: linear-gradient(135deg, #8b5cf6, #a855f7, #c084fc);
    --background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
    --card-bg: rgba(30, 41, 59, 0.4);
    --text-primary: #ffffff;
    --text-secondary: #9ca3af;
    --accent: #8b5cf6;
}
```

## 🚧 Future Enhancements

- [ ] Local Storage persistence for tasks
- [ ] Drag and drop task reordering
- [ ] Task categories and tags
- [ ] Due dates and reminders
- [ ] Export tasks to various formats
- [ ] Dark/Light theme toggle
- [ ] Progressive Web App (PWA) features

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🙏 Acknowledgments

- Inspired by modern productivity applications
- Design influenced by glassmorphism and dark UI trends
- Built as part of web development skill enhancement

---

⭐ **Star this repository if you found it helpful!**

**Built with ❤️ by Vikas Choudhary**
