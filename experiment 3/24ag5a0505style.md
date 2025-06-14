/* Set a monospace font for the entire page */
body {
    font-family: monospace;
}

/* Main content section styling */
main {
    background-color: #efefef; /* Light gray background for the main section */
    color: #330000; /* Dark red text color for content */
    margin-left: 10px; /* Add 10px space on the left side */
    height: 60vh; /* Set the height to 60% of the viewport height */
}

/* Header and footer shared styling */
header, footer {
    background-color: #000d57; /* Deep blue background color */
    color: #fff; /* White text color */
    padding: 1rem; /* Add padding around the header/footer */
    height: 50px; /* Set the height of header and footer to 50px */
}

/* Specific styling for header and nav */
header, nav {
    margin-bottom: 10px; /* Add 10px space below header and nav */
    flex-basis: 50%; /* Set the width of header and nav to 50% of their container */
}

/* Footer additional margin at the top */
footer {
    margin-top: 10px; /* Add 10px space above footer */
}

/* Navigation section styling */
nav {
    background-color: #fff; /* White background for navigation */
    color: #000; /* Black text color for navigation */
    padding: 1rem; /* Add padding inside the navigation bar */
    height: 20px; /* Set the height of the navigation bar to 20px */
}

/* Sidebar sections (left and right) styling */
.sidebar1, .sidebar2 {
    flex-basis: 10%; /* Set the width of sidebars to 10% of the container */
    background-color: #fff; /* White background for sidebars */
    color: #000; /* Black text color for sidebars */
}

/* Additional margin to the left of the second sidebar */
.sidebar2 {
    margin-left: 10px; /* Add 10px space to the left of the second sidebar */
}

/* Container to hold both sidebars and content */
.container1 {
    display: flex; /* Use flexbox to align child elements horizontally */
}

/* Main content container styling */
.container2 {
    display: flex; /* Use flexbox to align child elements vertically */
    flex-direction: column; /* Arrange child elements vertically */
    flex: 1; /* Allow the container to take up remaining space */
}

/* Flexbox alignment for header, nav, main, sidebars, and footer */
header, nav, main, .sidebar1, .sidebar2, footer {
    display: flex; /* Use flexbox for these elements */
    align-items: center; /* Vertically center content within each element */
    justify-content: center; /* Horizontally center content within each element */
    border-radius: 10px; /* Round the corners of each element with a 10px radius */
}

/* Wrapper that contains the main page layout */
.wrapper {
    display: flex; /* Use flexbox to arrange child elements */
    flex-direction: column; /* Arrange child elements vertically */
    font-weight: 600; /* Set a semi-bold font weight for the wrapper content */
}
