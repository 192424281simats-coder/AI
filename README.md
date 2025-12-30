<!DOCTYPE html>
<html>
<head>
  <title>AI College Enquiry Chatbot</title>
  <style>
    body { font-family: Arial; background: #eef; }
    .box {
      width: 450px;
      margin: 30px auto;
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 0 8px rgba(0,0,0,0.2);
    }
    #chat {
      height: 300px;
      overflow-y: auto;
      border: 1px solid #aaa;
      padding: 8px;
      margin-bottom: 10px;
      background: #fafafa;
    }
    input { width: 75%; padding: 8px; }
    button { padding: 8px; }
    .header {
      font-size: 18px;
      font-weight: bold;
      text-align: center;
      margin-bottom: 8px;
    }
  </style>
</head>
<body>

<div class="box">
  <div class="header">
    🎓 College Enquiry Chatbot<br>
    👤 Dileep Kumar Deshaboina<br>
    🎓 Saveetha University
  </div>
  <div id="chat"></div>
  <input id="msg" placeholder="Ask about attendance, courses, food..." />
  <button onclick="send()">Send</button>
</div>

<script>
function send() {
  let user = document.getElementById("msg").value.toLowerCase();
  let chat = document.getElementById("chat");

  chat.innerHTML += "<b>You:</b> " + user + "<br>";

  let reply = "Sorry, I don't understand. Ask about attendance, courses, classrooms, food, faculty, timings, or contact.";

  if (user.includes("attendance")) {
    reply = "Attendance system is online. Students must mark daily before 9 AM.";
  }
  else if (user.includes("course")) {
    reply = "We offer: B.E. CSE, ECE, EEE, Mechanical, Civil, and AI.";
  }
  else if (user.includes("classroom")) {
    reply = "Classrooms are in Block A and Block B, ground to 3rd floor.";
  }
  else if (user.includes("food") || user.includes("restaurant")) {
    reply = "The campus cafeteria is open 8 AM–8 PM serving Indian & fast food.";
  }
  else if (user.includes("faculty")) {
    reply = "Faculty rooms are in the main academic block (2nd floor).";
  }
  else if (user.includes("timing")) {
    reply = "College timing: 8:30 AM – 4:30 PM (Mon–Fri)";
  }
  else if (user.includes("contact")) {
    reply = "Main contact: +91 98765 43210 or email info@saveetha.ac.in.";
  }

  chat.innerHTML += "<b>Bot:</b> " + reply + "<br><br>";
  document.getElementById("msg").value = "";
}
</script>

</body>
</html>
