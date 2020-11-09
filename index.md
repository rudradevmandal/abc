<button class="btn js-toggle-dark-mode">Click to Enter the Dark Side</button>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Click to Enter the Dark Side';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Take me to the Bright Side';
  }
});
</script>
# Welcome to Dumb it Down!

Here at Dumb it Down, we try to takle the notion of boring research papers. We take a research paper that had had a significant imact on the progress of science and break it into simpler segements which are fun to read and easy-to-understand, with a pinch of humor baked into it. In short, we simplify groundbreaking research papers.





<!--stackedit_data:
eyJoaXN0b3J5IjpbNjM2MjgxNTM2LC05OTMwNTI3NCwxMDUzMT
g3Mzc2LDQ1ODYzMDY5MCwtMTA5MjYzMjQ5NCwtMzMyNDU1MzYz
XX0=
-->