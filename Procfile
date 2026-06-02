web: gunicorn run:app
<!doctype html>
<html>
  <head>
    <title>Fetch API Example</title>
  </head>
  <body>
    <h2>Users List</h2>
    <button onclick="loadUsers()">Load Users</button>
    <ul id="userList"></ul>
    <script>
      function loadUsers() {
        fetch("https://jsonplaceholder.typicode.com/users")
          .then((response) => response.json())
          .then((data) => {
            let output = "";
            data.forEach((user) => {
              output += `<li>${user.name} - ${user.email}</li>`;
            });
            document.getElementById("userList").innerHTML = output;
          })
          .catch((error) => {
            console.log(error);
          });
      }
    </script>
  </body>
</html>