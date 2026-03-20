# my-website
index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Future Science Engineers (FSE)</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: #0a0f1c;
    color: #e0f2f1;
    overflow-x: hidden;
}

/* Animated Background */
body::before {
    content: "";
    position: fixed;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(56,189,248,0.1) 1px, transparent 1px);
    background-size: 40px 40px;
    animation: moveBg 20s linear infinite;
    z-index: -1;
}
@keyframes moveBg {
    0% { transform: translate(0,0); }
    100% { transform: translate(-50px,-50px); }
}

/* Sidebar */
.sidebar {
    position: fixed;
    width: 200px;
    height: 100%;
    background: #020617;
    padding-top: 20px;
}

.sidebar a {
    display: block;
    color: #38bdf8;
    padding: 15px;
    text-decoration: none;
    font-weight: bold;
}

.sidebar a:hover {
    background: #1e293b;
    color: white;
}

/* Content */
.content {
    margin-left: 210px;
    padding: 20px;
}

/* Header */
.header {
    text-align: center;
    font-size: 42px;
    font-weight: bold;
    color: #38bdf8;
    text-shadow: 0 0 20px #38bdf8;
}

/* Section */
section {
    margin: 50px 0;
}

/* Cards */
.card {
    background: rgba(2,6,23,0.9);
    border-radius: 15px;
    padding: 20px;
    margin: 10px;
    display: inline-block;
    width: 240px;
    box-shadow: 0 0 20px rgba(56,189,248,0.2);
    transition: 0.3s;
}
.card:hover {
    transform: scale(1.05);
}

/* Form */
input, textarea {
    width: 90%;
    padding: 10px;
    margin: 10px;
    border-radius: 5px;
    border: none;
}

/* Button */
button {
    padding: 10px 20px;
    background: #38bdf8;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

/* Popup */
.popup {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    background: #020617;
    padding: 30px;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0 0 25px #38bdf8;
    transition: 0.3s;
}
.popup.active {
    transform: translate(-50%, -50%) scale(1);
}

/* Mobile */
@media (max-width: 700px) {
    .sidebar {
        width: 100%;
        height: auto;
        position: relative;
        display: flex;
        justify-content: space-around;
    }
    .content {
        margin-left: 0;
    }
}
</style>

</head>

<body>

<!-- Sidebar -->
<div class="sidebar">
<a href="#home">Home</a>
<a href="#members">Members</a>
<a href="#about">About</a>
<a href="#feedback">Feedback</a>
</div>

<div class="content">

<div class="header">
🚀 Future Science Engineers (FSE)
</div>

<!-- HOME -->
<section id="home">
<h2>Welcome</h2>
<p>
We are a technical school science expo team focused on innovation and robotics.
We currently have <b>6 operating members</b> and one live project running, with more coming soon.
</p>

<p>
📞 7005422453 <br>
📷 Instagram: futu.reengineer1 <br>
▶ YouTube: www.youtube.com/@futurescienceengineers
</p>
</section>

<!-- MEMBERS -->
<section id="members">
<h2>Our Team</h2>

<div class="card"><h3>Suham Das</h3><p>Group Leader</p></div>
<div class="card"><h3>Deeptanu Majumdhar</h3><p>Code Assistant</p></div>
<div class="card"><h3>Pradyush Paul</h3><p>Architecture Engineer</p></div>
<div class="card"><h3>Samyudeep Bishwass</h3><p>Architecture Engineer</p></div>
<div class="card"><h3>Naichitra Roy</h3><p>Color Design Engineer</p></div>
<div class="card"><h3>Pratyusha Banik</h3><p>Color Design Engineer</p></div>

</section>

<!-- ABOUT -->
<section id="about">
<h2>About</h2>
<p>
Future Science Engineers (FSE) is a student-led innovation team working on robotics and technical systems.
We are continuously building and improving projects for the future.
</p>
</section>

<!-- FEEDBACK -->
<section id="feedback">
<h2>Feedback Dashboard</h2>

<form id="form" action="https://formsubmit.co/featurescienceingenier@gmail.com" method="POST">
<input type="text" name="name" placeholder="Your Name" required>
<input type="email" name="email" placeholder="Your Email" required>
<textarea name="message" placeholder="Your Feedback" rows="5" required></textarea>

<input type="hidden" name="_captcha" value="false">

<button type="submit">Submit Feedback</button>
</form>

</section>

</div>

<!-- POPUP -->
<div class="popup" id="popup">
<h2>🎉 Thank You!</h2>
<p>Your feedback has been submitted successfully.<br>We appreciate your support!</p>
<button onclick="closePopup()">Close</button>
</div>

<script>
const form = document.getElementById("form");
const popup = document.getElementById("popup");

form.addEventListener("submit", function() {
    setTimeout(() => {
        popup.classList.add("active");
    }, 500);
});

function closePopup() {
    popup.classList.remove("active");
}
</script>

</body>
</html>
