# Ai-education-project-
📄 RESEARCH PROJECT: AI in Education: Enhancing Student Understanding Through AI-Assisted Learning  A classroom-based experimental project on AI-assisted learning in developing school environments.  
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>AI in Education Project</title>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #f4f6f9;
    color: #333;
}

header {
    background: #0a192f;
    color: white;
    padding: 20px;
    text-align: center;
}

section {
    padding: 20px;
    margin: 20px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

h2 {
    color: #0a192f;
}

.card {
    margin-top: 15px;
    padding: 15px;
    border-left: 4px solid #0a192f;
    background: #fafafa;
}

button {
    padding: 10px;
    margin-top: 10px;
    background: #0a192f;
    color: white;
    border: none;
    cursor: pointer;
}

input, textarea {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
}
</style>

</head>

<body>

<header>
    <h1>AI in Education Project</h1>
    <p>By Ramon Rasaki Olayiwola</p>
</header>

<!-- PROJECT OVERVIEW -->
<section>
<h2>📘 Project Overview</h2>
<p>
This project explores how AI-assisted teaching improves student understanding,
engagement, and learning outcomes in real classroom environments.
</p>
</section>

<!-- IMAGE UPLOAD -->
<section>
<h2>🖼 Upload Classroom Photos</h2>
<input type="file" id="imageUpload" accept="image/*">
<div id="imagePreview"></div>
</section>

<!-- VIDEO UPLOAD -->
<section>
<h2>🎥 Upload Classroom Videos</h2>
<input type="file" id="videoUpload" accept="video/*">
<div id="videoPreview"></div>
</section>

<!-- PDF SECTION -->
<section>
<h2>📄 Upload / Link PDFs</h2>
<input type="file" id="pdfUpload" accept="application/pdf">
<div id="pdfList"></div>
</section>

<!-- CHARTS -->
<section>
<h2>📊 Data & Charts</h2>
<p>Add screenshots of your Google Form charts below:</p>
<input type="file" id="chartUpload" accept="image/*">
<div id="chartPreview"></div>
</section>

<!-- NOTES -->
<section>
<h2>📝 Personal Notes / Journal</h2>
<textarea id="notes" rows="6" placeholder="Write your teaching reflections..."></textarea>
<button onclick="saveNote()">Save Note</button>
<div id="savedNotes"></div>
</section>

<!-- LINKS -->
<section>
<h2>🔗 External Links</h2>
<input type="text" id="linkInput" placeholder="Paste link (Google Form, YouTube, etc)">
<button onclick="addLink()">Add Link</button>
<ul id="linkList"></ul>
</section>

<script>

// IMAGE UPLOAD
document.getElementById("imageUpload").onchange = function(event) {
    let file = event.target.files[0];
    let img = document.createElement("img");
    img.src = URL.createObjectURL(file);
    img.width = 200;
    document.getElementById("imagePreview").appendChild(img);
};

// VIDEO UPLOAD
document.getElementById("videoUpload").onchange = function(event) {
    let file = event.target.files[0];
    let video = document.createElement("video");
    video.src = URL.createObjectURL(file);
    video.controls = true;
    video.width = 300;
    document.getElementById("videoPreview").appendChild(video);
};

// PDF UPLOAD
document.getElementById("pdfUpload").onchange = function(event) {
    let file = event.target.files[0];
    let link = document.createElement("a");
    link.href = URL.createObjectURL(file);
    link.textContent = file.name;
    link.target = "_blank";
    document.getElementById("pdfList").appendChild(link);
};

// CHART UPLOAD
document.getElementById("chartUpload").onchange = function(event) {
    let file = event.target.files[0];
    let img = document.createElement("img");
    img.src = URL.createObjectURL(file);
    img.width = 300;
    document.getElementById("chartPreview").appendChild(img);
};

// NOTES SYSTEM
function saveNote() {
    let note = document.getElementById("notes").value;
    let div = document.createElement("div");
    div.className = "card";
    div.textContent = note;
    document.getElementById("savedNotes").appendChild(div);
}

// LINK SYSTEM
function addLink() {
    let link = document.getElementById("linkInput").value;
    let li = document.createElement("li");
    let a = document.createElement("a");
    a.href = link;
    a.textContent = link;
    a.target = "_blank";
    li.appendChild(a);
    document.getElementById("linkList").appendChild(li);
}

</script>

</body>
</html>
