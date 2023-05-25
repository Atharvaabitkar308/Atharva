# Atharva
Sound item dashbord creation
HTML structure:


<!DOCTYPE html> <html> <head> <title>Sound Item Dashboard</title> <style> /* CSS styles for the dashboard */ </style> </head> <body> <h1>Sound Item Dashboard</h1> <div id="dashboard"></div> <!-- Include JavaScript libraries for graphs and progress bar --> <script src="path/to/graphing/library.js"></script> <script src="path/to/progress/bar/library.js"></script> <script src="path/to/dashboard/script.js"></script> </body> </html>                                                           
JavaScript (script.js):


// Sample data for the sound items const soundItems = [ { image: "path/to/image1.jpg", title: "Sound Item 1", unique_plays: 100, total_plays: 150, completion_rate: 0.75 }, { image: "path/to/image2.jpg", title: "Sound Item 2", unique_plays: 75, total_plays: 100, completion_rate: 0.85 }, // Add more sound items as needed ]; // Function to create the dashboard function createDashboard() { const dashboard = document.getElementById("dashboard"); // Loop through sound items and create a card for each soundItems.forEach(item => { const card = document.createElement("div"); card.classList.add("card"); const image = document.createElement("img"); image.src = item.image; card.appendChild(image); const title = document.createElement("h2"); title.textContent = item.title; card.appendChild(title); const uniquePlaysGraph = createGraph("Unique Plays", item.unique_plays); card.appendChild(uniquePlaysGraph); const totalPlaysGraph = createGraph("Total Plays", item.total_plays); card.appendChild(totalPlaysGraph); const completionRateProgressBar = createProgressBar(item.completion_rate); card.appendChild(completionRateProgressBar); dashboard.appendChild(card); }); } //
