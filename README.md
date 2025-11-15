# project-2-flex
# 🌌 Responsive Flexbox Layout Project

A comprehensive responsive web layout demonstrating advanced flexbox techniques with a space exploration theme.

## 📋 Project Overview

This project showcases a fully responsive 6-row layout built entirely with CSS Flexbox. Each row demonstrates different flexbox configurations and responsive design patterns, adapting seamlessly across desktop, tablet, and mobile devices.

## 🎯 Learning Objectives

- Master CSS Flexbox properties (`flex-grow`, `flex-shrink`, `flex-basis`)
- Implement responsive design using media queries
- Utilize the `order` property for layout reordering
- Create flexible, maintainable layouts without fixed widths
- Apply modern design principles with gradients and animations

## 📐 Layout Structure

### Row 1: Four Equal Columns
- **Desktop:** 4 items × 25% width each
- **Tablet:** 2 items × 50% width (2×2 grid)
- **Mobile:** 1 item × 100% width (stacked)
- **Flex Property:** `flex: 1 1 calc(25% - 20px)`

### Row 2: Two Equal Columns
- **Desktop:** 2 items × 50% width each
- **Tablet:** 1 item × 100% width (stacked)
- **Mobile:** 1 item × 100% width (stacked)
- **Flex Property:** `flex: 1 1 calc(50% - 20px)`

### Row 3: Asymmetric Layout (1:3 ratio)
- **Desktop:** 1 column (25%) + 3 columns (75%)
- **Tablet:** Full width stacked
- **Mobile:** Full width stacked
- **Flex Properties:**
  - Item 1: `flex: 1 1 calc(25% - 20px)`
  - Item 2: `flex: 3 1 calc(75% - 20px)`

### Row 4: Full-Width Single Item
- **All Devices:** 100% width
- **Flex Property:** `flex: 1 1 100%`
- Perfect for hero sections or important announcements

### Row 5: Three-Column with Order Change ⭐
- **Desktop:** 1 column (25%) + 2 columns (50%) + 1 column (25%)
- **Tablet/Mobile:** Stacked with **reordered items**
- **Key Feature:** Uses `order` property to change visual sequence
  - Desktop order: Left → Center → Right
  - Mobile order: **Center → Left → Right**
- **Flex Properties:**
  - Items 1 & 3: `flex: 1 1 calc(25% - 20px)`
  - Item 2: `flex: 2 1 calc(50% - 20px)`

### Row 6: Creative Five-Item Layout
- **Desktop:** 5 items with varying widths (20%, 40%, 20%, 20%, 20%)
- **Tablet:** 2 columns
- **Mobile:** Stacked
- **Unique Feature:** More than 4 items per row with custom flex-basis calculations
- Demonstrates advanced flex properties and design creativity

## 🔧 Key CSS Properties Used

### Flexbox Container Properties
```css
display: flex;
flex-wrap: wrap;
gap: 20px;
```

### Flexbox Item Properties
```css
flex: [flex-grow] [flex-shrink] [flex-basis];
order: [number];
min-width: [value];
```

### Responsive Breakpoints
- **Desktop:** > 768px
- **Tablet:** ≤ 768px
- **Mobile:** ≤ 480px

## 🎨 Design Features

- **Modern Gradient Backgrounds:** Each item uses unique CSS gradients
- **Hover Effects:** Smooth transform animations on hover
- **Responsive Typography:** Font sizes adapt to screen size
- **Accessible:** Proper semantic HTML and contrast ratios
- **Performance:** Pure CSS, no JavaScript dependencies

## 💡 The `order` Property

Row 5 demonstrates the powerful `order` property, which controls the visual order of flex items without changing the HTML structure.

**Desktop Layout:**
```
[Item 1] [Item 2 - Center] [Item 3]
 order:1    order:2         order:3
```

**Mobile Layout:**
```
[Item 2 - Center]  ← order:1 (appears first)
[Item 1]           ← order:2
[Item 3]           ← order:3
```

This is useful for:
- Prioritizing content on mobile devices
- Maintaining semantic HTML order while changing visual presentation
- Creating different reading flows for different screen sizes

## 🚀 How to Use

1. **Clone or download** the project files
2. Open `index.html` in your web browser
3. **Resize your browser window** to see responsive behavior
4. Inspect the code to understand flexbox calculations

## 📱 Testing Responsive Design

### Browser DevTools Method
1. Open browser DevTools (F12 or Right-click → Inspect)
2. Click the device toolbar icon (Ctrl+Shift+M / Cmd+Shift+M)
3. Select different device presets or drag to resize
4. Watch how each row adapts

### Manual Testing
- **Desktop:** Window wider than 768px
- **Tablet:** Window between 481px and 768px
- **Mobile:** Window 480px or less

## 📊 Flex-Basis Calculations

The `calc()` function allows precise sizing with gaps:

```css
/* 4 columns with 20px gaps */
flex: 1 1 calc(25% - 20px);

/* 2 columns with 20px gaps */
flex: 1 1 calc(50% - 20px);

/* 3:1 ratio */
flex: 3 1 calc(75% - 20px);  /* Larger item */
flex: 1 1 calc(25% - 20px);  /* Smaller item */
```

The gap is subtracted to account for the `gap: 20px` property on the flex container.

## 🎓 Best Practices Demonstrated

1. **Mobile-First Approach:** Base styles work for mobile, enhanced for larger screens
2. **Flexible Units:** Using percentages and calc() instead of fixed pixels
3. **Min-Width Safety:** Prevents items from becoming too small
4. **Semantic HTML:** Proper use of headings and content structure
5. **CSS Organization:** Logical grouping of related styles
6. **Performance:** Hardware-accelerated transforms for animations

## 🔍 Browser Compatibility

- ✅ Chrome/Edge (Modern versions)
- ✅ Firefox (Modern versions)
- ✅ Safari (Modern versions)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

**Note:** Flexbox has excellent browser support (97%+ globally). The `gap` property is supported in all modern browsers (2021+).

## 📚 Additional Resources

- [MDN Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS-Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox Froggy](https://flexboxfroggy.com/) - Interactive learning game
- [Can I Use - Flexbox](https://caniuse.com/flexbox)

## 🎯 Project Requirements Met

- ✅ Row 3: 1 column × 3 column layout
- ✅ Row 4: 4 column wide single item
- ✅ Row 5: 1 × 2 × 1 column layout with order change
- ✅ Row 6: Creative unique layout (5 items with varying widths)
- ✅ Desktop, tablet, and mobile responsive breakpoints
- ✅ Use of flexbox properties from MDN documentation
- ✅ Order property for layout reordering

## 🌟 Future Enhancements

- Add CSS Grid for alternative layout approach
- Implement dark/light theme toggle
- Add more interactive elements
- Create additional creative row variations
- Add CSS animations and transitions

## 👨‍💻 Author

COMP584 - Web Development Project
Space Theme Flexbox Layout

## 📄 License

This project is created for educational purposes.

---

**Happy Coding! 🚀** Resize your browser and watch the magic happen!
