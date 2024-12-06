
# Clock Using JavaScript

A visually appealing analog clock built using HTML, CSS, and JavaScript. This project demonstrates how to create a functioning clock with smooth animations.

## Features

- **Analog Clock**: A realistic analog clock design with hour, minute, and second hands.
- **Smooth Animations**: The hands move smoothly to represent real-time changes.
- **Customizable Design**: You can replace the clock background with any custom image.

## Demo

*Include a screenshot or GIF of the clock here.*  
Optionally, link to a live demo if hosted online.

## Technologies Used

- **HTML**: For the structure of the clock.
- **CSS**: To style the clock container and hands.
- **JavaScript**: Implements real-time functionality and smooth rotations.

## How It Works

### HTML

The structure includes a `div` container for the clock and three `div` elements representing the hour, minute, and second hands:
```html
<div id="clockContainer">
    <div id="hour"></div>
    <div id="minute"></div>
    <div id="second"></div>
</div>
```

### CSS

CSS styles the clock's appearance, such as the container, background image, and the hands:
```css
#clockContainer {
    height: 440px;
    width: 440px;
    background: url(clock.png) no-repeat;
    background-size: 100%;
}
#hour, #minute, #second {
    position: absolute;
    background: black;
    border-radius: 10px;
    transform-origin: bottom;
}
```

### JavaScript

JavaScript calculates the rotation of the hands based on the current time and updates their positions every second:
```javascript
setInterval(() => {
    let d = new Date();
    let hrotation = 30 * d.getHours() + d.getMinutes() / 2;
    let mrotation = 6 * d.getMinutes();
    let srotation = 6 * d.getSeconds();

    hour.style.transform = `rotate(${hrotation}deg)`;
    minute.style.transform = `rotate(${mrotation}deg)`;
    second.style.transform = `rotate(${srotation}deg)`;
}, 1000);
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/clock-using-js.git
   ```
2. Navigate to the project folder:
   ```bash
   cd clock-using-js
   ```
3. Open `index.html` in your browser to view the clock.

## How to Run

1. Save the files in the same directory:
   - `index.html`
   - `index.css`
   - `index.js`
2. Ensure that the clock background image (`clock.png`) is in the same directory.
3. Open `index.html` in your browser to see the analog clock in action.

## Future Enhancements

- Add digital time display alongside the analog clock.
- Implement themes for dark and light modes.
- Add time zone functionality to display times for different regions.

## License

This project is licensed under the [MIT License](LICENSE).
