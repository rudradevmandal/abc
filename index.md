# Welcome to Dumb it Down!

We try to expand and break down research papers in an easy-to-understand way. In short, we simplify groundbreaking research papers.


<button class="btn js-toggle-dark-mode">Click to Enter the Dark Side</button>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Click to Enter the Dark Side';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Return to the bright side';
  }
});
</script>

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA1MzE4NzM3Niw0NTg2MzA2OTAsLTEwOT
I2MzI0OTQsLTMzMjQ1NTM2M119
-->