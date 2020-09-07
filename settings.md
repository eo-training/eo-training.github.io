---
title: "Settings"
---

<div>

<div>
<label for="autoPlayAudio">Auto-play audio</label>
<input type="checkbox" id="autoPlayAudioCheckbox" onclick="toggleAudio()">
</div>

<p id="text" style="display:none">Checkbox is CHECKED!</p>

<button onclick="enableAudio()">Enable Audio</button>
<button onclick="disableAudio()">Disable Audio</button>

</div>


<script>
let autoPlayAudioCheckbox = document.querySelector("#autoPlayAudioCheckbox");
let audioState = localStorage.getItem("autoPlayAudio");
let text = document.getElementById("text");

if (audioState == "disabled") {
	autoPlayAudioCheckbox.checked = false;
}
else {
	autoPlayAudioCheckbox.checked = true;
	text.style.display = "block";
}

function toggleAudio() {
	if (autoPlayAudioCheckbox.checked == true) {
		localStorage.setItem("autoPlayAudio", "enabled");
		text.style.display = "block";
	}
	if (autoPlayAudioCheckbox.checked == false) {
		localStorage.setItem("autoPlayAudio", "disabled");
		text.style.display = "none";
	}
}

function enableAudio() {
	localStorage.setItem("autoPlayAudio", "enabled");
}

function disableAudio() {
	localStorage.setItem("autoPlayAudio", "disabled");
}

</script>