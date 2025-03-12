# 📊 Enhanced User Directory - Super Challenge

## ✨ Challenge Overview
Your task is to build an enhanced user directory that leverages **jQuery AJAX**, **radio buttons**, and **looping structures** to dynamically generate and display a list of users based on user-selected criteria. This challenge combines concepts from previous lessons, including:

- **AJAX Requests** to fetch user data dynamically
- **Loops (for, while, do-while)** to iterate and display multiple users
- **Conditional Statements (if, else if, switch)** for filtering and formatting data
- **DOM Manipulation** using jQuery
- **Event Handling** to respond to user input

---

## 📖 Instructions
1. Add an **input field** where the user can specify how many random users they want to fetch (1-10).
2. Modify the existing **AJAX request** to fetch multiple users at once.
3. Display all fetched users in a **responsive grid layout**.
4. Allow users to **filter the displayed users** based on country.
5. Use **a switch statement** to categorize countries into regions (e.g., "North America", "Europe", "Asia").
6. Style everything neatly using **CSS**.

---

## 🔥 Bonus Challenge - Advanced Filtering
### "Super User Search"
Enhance the challenge by:
- Adding a **search input box** that allows filtering users by **name**.
- Implementing a **while loop** to continuously update results as the user types.
- Showing a **loading spinner** while fetching data.
- Animating the appearance of user cards using **jQuery effects**.

---

## 🖥 Example Code Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enhanced User Directory</title>
    <script src="https://code.jquery.com/jquery-3.6.4.min.js"></script>
    <link href="./style.css" rel="stylesheet">
</head>
<body>
    <h1>Enhanced User Directory</h1>
    
    <div class="controls">
        <label>Number of Users (1-10): <input type="number" id="userCount" min="1" max="10" value="1"></label>
        <div class="radio-group">
            <label><input type="radio" name="gender" value="male" checked> Male</label>
            <label><input type="radio" name="gender" value="female"> Female</label>
        </div>
        <button id="fetchUsers">Fetch Users</button>
    </div>
    
    <input type="text" id="searchBox" placeholder="Search by name...">
    
    <div id="userGrid" class="user-grid"></div>
    
    <script>
        $(document).ready(function() {
            $("#fetchUsers").click(function() {
                var gender = $("input[name='gender']:checked").val();
                var count = $("#userCount").val();
                $("#userGrid").html('<p>Loading...</p>');

                $.ajax({
                    url: `https://randomuser.me/api/?gender=${gender}&results=${count}`,
                    method: "GET",
                    success: function(data) {
                        let usersHtml = "";
                        data.results.forEach(user => {
                            usersHtml += `
                                <div class="user-card">
                                    <img src="${user.picture.medium}" alt="User Photo">
                                    <p><strong>${user.name.first} ${user.name.last}</strong></p>
                                    <p>${user.location.country}</p>
                                    <p>${user.email}</p>
                                </div>
                            `;
                        });
                        $("#userGrid").html(usersHtml);
                    },
                    error: function() {
                        alert("Error fetching users.");
                    }
                });
            });
        });
    </script>
</body>
</html>
```

---

## 🌟 Super Bonus Challenge - Region Categorization
Modify the script to categorize users based on their **country** into predefined regions (e.g., "North America", "Europe"). Use a **switch statement** to determine the region dynamically.

Example:
```javascript
function getRegion(country) {
    switch (country) {
        case "United States":
        case "Canada":
            return "North America";
        case "France":
        case "Germany":
            return "Europe";
        case "Japan":
        case "China":
            return "Asia";
        default:
            return "Other";
    }
}
```

Happy coding! 🚀

