# My-To-Do-App
https://purushothamvmitti05.github.io/My-To-Do-App.github.io/

Todo List Application
A simple, elegant todo list application built with vanilla JavaScript, featuring local storage persistence and a clean user interface.

✨ Features
Add Todos - Quickly add tasks by typing and pressing enter
Mark as Complete - Click the checkbox to mark tasks as done
Delete Todos - Remove tasks with a single click
Local Storage - Todos persist across browser sessions
Theme Support - Light and dark theme switching (commented out in current version)
Responsive Design - Works seamlessly on desktop and mobile devices
Empty State - Friendly UI when no todos exist
📁 File Structure
todo-app/
│
├── index.html          # Main HTML structure
├── script.js           # JavaScript functionality
└── style.css           # Styling and theme variables
🚀 Getting Started
Prerequisites
Modern web browser (Chrome, Firefox, Safari, Edge)
No server or build tools required!
Installation
Download or clone the files
Open index.html in your web browser
Start adding todos!
That's it! No dependencies or installation required.

🎯 How to Use
Adding a Todo
Type your task in the input field at the bottom
Press Enter or click outside the field
Your todo appears in the list above
Marking as Complete
Click the circular checkbox next to any todo
The text will strike through to indicate completion
Click again to mark as incomplete
Deleting a Todo
Click the trash icon on the right side of any todo
The item is immediately removed from the list
💻 Code Overview
HTML Structure (index.html)
Navigation bar (theme switch commented out)
Todo list container (<ul class="todo-list">)
Empty state display with icon and instructions
Input form for adding new todos
Font Awesome icons for visual elements
JavaScript Functionality (script.js)
Main Functions:

myFunction(x) - Adds a new todo to the array
renderTodo(todo) - Renders/updates a todo in the DOM
toggleDone(id) - Toggles the checked state
deleteTodo(id) - Removes a todo from the list
localStorage integration for data persistence
Event Listeners:

Form submit for adding todos
Click events for checking/deleting todos
DOMContentLoaded for loading saved todos
Theme switch (commented out)
CSS Styling (style.css)
Features:

CSS custom properties for theming
Light and dark theme support
Responsive design with media queries
Flexbox layout
Smooth transitions and animations
Theme Variables:

css
[data-theme="light"] {
    --bg-color: #fff;
    --color: #333;
    --svgcolor: #111;
}

[data-theme="dark"] {
    --bg-color: #333333;
    --color: #e9dcdc;
    --svgcolor: #fff;
}
🎨 Customization
Change Colors
Light Theme:

css
[data-theme="light"] {
    --bg-color: #fff;        /* Background color */
    --color: #333;           /* Text color */
    --svgcolor: #111;        /* Icon color */
}
Dark Theme:

css
[data-theme="dark"] {
    --bg-color: #333333;     /* Background color */
    --color: #e9dcdc;        /* Text color */
    --svgcolor: #fff;        /* Icon color */
}
Enable Theme Switcher
Uncomment the theme switcher code in index.html:

html
<nav>
    <div class="theme-switch-wrapper">
        <label class="theme-switch" for="checkbox">
            <input type="checkbox" id="checkbox" />
            <div class="slider round"></div>
        </label>
        <em>Switch Theme</em>
    </div>
</nav>
Modify Input Placeholder
html
<input autofocus type="text" class="inputselect" placeholder="Your custom text">
Change App Title
html
<h1 class="app-title">My Todo</h1>
📱 Responsive Design
The app adapts to different screen sizes:

Desktop (>608px):

Full-width container (max 700px)
Large title (80px)
Full description text
Mobile (<608px):

90% width container
Smaller title (3rem)
Compact description (1.5rem)
Hidden theme toggle text
🔧 Technical Details
Data Structure
Each todo is stored as an object:

javascript
{
    x: "Todo text",
    checked: false,
    id: 1234567890,  // Timestamp
    deleted: false   // For deletion handling
}
```

### Local Storage
- Key: `"demoarray"`
- Value: JSON stringified array of todos
- Automatically syncs on every change

### DOM Manipulation
- Dynamic list item creation
- `data-key` attributes for identifying todos
- Event delegation for click handling

## 🐛 Known Issues & Notes

1. **Character Encoding:** The emoji in the empty state might appear as encoded characters (`ðŸ'‡`) in some editors
2. **Duplicate Delete Button:** There's a duplicate delete button in the HTML string (line 30 of script.js)
3. **Theme Switch:** Currently commented out but functional code exists

## 🔄 Future Enhancements

Potential improvements:
- [ ] Add todo categories/tags
- [ ] Priority levels (high, medium, low)
- [ ] Due dates and reminders
- [ ] Search/filter functionality
- [ ] Edit existing todos
- [ ] Drag and drop reordering
- [ ] Export/import todos
- [ ] Statistics (completed vs. pending)
- [ ] Multiple lists
- [ ] Sync across devices

## 🎓 Learning Concepts

This project demonstrates:
- **DOM Manipulation** - Creating, updating, removing elements
- **Event Handling** - Forms, clicks, keyboard events
- **Local Storage API** - Persisting data in the browser
- **Array Methods** - `push()`, `filter()`, `findIndex()`, `forEach()`
- **ES6+ Features** - Arrow functions, template literals, spread operator
- **CSS Variables** - For easy theming
- **Responsive Design** - Media queries and flexible layouts

## 🛠️ Troubleshooting

**Todos not saving:**
- Check if browser allows local storage
- Open Developer Tools → Application → Local Storage
- Verify `"demoarray"` key exists

**Theme not switching:**
- Uncomment theme switch code in HTML
- Verify checkbox input has id `"checkbox"`
- Check console for JavaScript errors

**Styling issues:**
- Clear browser cache
- Check if all CSS loaded (Network tab)
- Verify no CSS syntax errors

**Emojis not displaying:**
- Ensure UTF-8 encoding: `<meta charset="UTF-8">`
- Use emoji-supporting fonts
- Consider replacing with Font Awesome icons

## 📝 Code Quality Tips

**Good Practices:**
- ✅ Uses semantic HTML
- ✅ Implements local storage
- ✅ Responsive design
- ✅ Event delegation

**Could Improve:**
- Remove duplicate delete button
- Better variable naming (`demoarray` → `todos`)
- Add error handling for localStorage
- Use const/let consistently
- Add comments for complex logic

## 🌟 Credits

- **Font Awesome** - Icons (v5.15+)
- **Google Fonts** - System font stack
- **GitHub Buttons** - Social sharing (commented out)

## 📄 License

This is a learning project. Feel free to use, modify, and distribute as needed.

## 🤝 Contributing

This appears to be a learning project. If you'd like to improve it:
1. Fix the duplicate delete button
2. Improve variable naming
3. Add error handling
4. Enhance accessibility
5. Add unit tests

## 💡 Usage Examples

**Quick Task:**
```
Type: "Buy groceries" → Press Enter
Result: Added to list instantly
```

**Daily Tasks:**
```
- Morning workout ✓
- Check emails ✓
- Team meeting
- Write report
```

**Shopping List:**
```
- Milk ✓
- Bread
- Eggs ✓
- Coffee
Built for learning JavaScript fundamentals! 📚✨
