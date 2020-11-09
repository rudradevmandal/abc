# Welcome to Dumb it Down!

Here at Dumb it Down, we try to takle the notion of boring research papers. We take We try to expand and break down research papers in an easy-to-understand way. In short, we simplify groundbreaking research papers.


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
eyJoaXN0b3J5IjpbMjA1NjYyNzE5NiwxMDUzMTg3Mzc2LDQ1OD
YzMDY5MCwtMTA5MjYzMjQ5NCwtMzMyNDU1MzYzXX0=
-->