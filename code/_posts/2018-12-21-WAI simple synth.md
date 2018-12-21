---
layout: post
author: esunlon
date: "December 21, 2018"
img_link : https://i.loli.net/2018/12/11/5c0f87bae2513.png
excerpt_separator: <!--more-->
---
<div class='controls'>
    <button class='start'>Start</button>
    <button class='stop' disabled>Stop</button>
</div>
<hr>
<div class='waveforms'>
    <button data-waveform='sine'>Sine</button>
    <button data-waveform='square'>Square</button>
    <button data-waveform='sawtooth'>Sawtooth</button>
    <button data-waveform='triangle'>Triangle</button>
</div>
<hr>
<div class='notes'>
    <button data-note='0'>unison</button>
    <button data-note='300'>minor-third</button>
    <button data-note='600'>tritone</button>
    <button data-note='900'>minor-seventh</button>
    <button data-note='1200'>octave</button>
</div>
<div class='display'>
    <label for='freq'>Frequency <span class='freq'>220Hz</span>
    <input class='freq-slider' name='freq' type='range' min='0' max='20000' step='1' value='220' />
    </label>
    <label for='detune'>Detune <span class='detune'>0 cents</span>
    <input class='detune-slider' name='detune' type='range' min='-1000' max='1000' step='1' value='0' />
    </label>
    <label for='gain'>Gain <span class='gain'>1</span>

        <input class='gain-slider' name='gain' type='range' min='0' max='1' step='0.1' value='1' />
    </label>
</div>
<script>
// create our AudioContext and Oscillator Nodes
var audioContext, osc, gain;
// assign our sliders and buttons to variables
var startButton = document.querySelector('.start'),
    stopButton = document.querySelector('.stop'),
    waveformButtons = document.querySelectorAll('.waveforms button'),
    freqSlider = document.querySelector('.freq-slider'),
    detuneSlider = document.querySelector('.detune-slider'),
    gainSlider = document.querySelector('.gain-slider'),
    gainDisplay = document.querySelector('.gain'),
    freqDisplay = document.querySelector('.freq'),
    detuneDisplay = document.querySelector('.detune');

// load our default value
init();

// setup start/stop
startButton.onclick = start;
stopButton.onclick = stop;

// setup waveform changes
addEventListenerBySelector('.waveforms button', 'click', function (event) {
    var type = event.target.dataset.waveform;
    changeType(type);
});

// setup note changes using detune
addEventListenerBySelector('.notes button', 'click', function (event) {
    var note = event.target.dataset.note;
    changeDetune(note);
});

// update frequency when slider moves
freqSlider.oninput = function () {
    changeFreq(freqSlider.value);
}

// detune frequency when slider moves
detuneSlider.oninput = function () {
    changeDetune(detuneSlider.value);
}

// update gain when slider moves
gainSlider.oninput = function () {
    changeGain(gainSlider.value);
}

function init() {
    audioContext = new(window.AudioContext || window.webkitAudioContext)();
    gain = audioContext.createGain();
    gain.gain.value = 1;
    osc = audioContext.createOscillator();
    osc.type = 'sine';
    osc.frequency.value = 440;
    osc.detune.value = 0;
    osc.connect(gain);
    osc.start(0);
}

// start everything by connecting to destination
function start() {
    UI('start');
    gain.connect(audioContext.destination);
}

// stop everything by connecting to destination
function stop() {
    UI('stop');
    gain.disconnect(audioContext.destination);
}

// change waveform type
function changeType(type) {
    osc.type = type;
}

// change frequency
function changeFreq(freq) {
    osc.frequency.value = freq;
    freqDisplay.innerHTML = freq + 'Hz';
}

// detune
function changeDetune(cents) {
    osc.detune.value = cents;
    detuneDisplay.innerHTML = cents + ' cents';
}

// change gain
function changeGain(volume) {
    gain.gain.value = volume;
    gainDisplay.innerHTML = volume;
}

// utilities
function addEventListenerBySelector(selector, event, fn) {
    var list = document.querySelectorAll(selector);
    for (var i = 0, len = list.length; i < len; i++) {
        list[i].addEventListener(event, fn, false);
    }
}

function UI(state) {
    switch (state) {
        case 'start':
            startButton.disabled = true;
            waveformButtons.disable = false;
            stopButton.disabled = false;
            break;
        case 'stop':
            startButton.disabled = false;
            waveformButtons.disable = true;
            stopButton.disabled = true;
            break;
    }
}

/* ios enable sound output */
	window.addEventListener('touchstart', function(){
		//create empty buffer
		var buffer = audioContext.createBuffer(1, 1, 22050);
		var source = audioContext.createBufferSource();
		source.buffer = buffer;
		source.connect(audioContext.destination);
		source.start(0);
	}, false);

</script>
