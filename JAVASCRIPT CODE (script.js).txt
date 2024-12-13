document.addEventListener('DOMContentLoaded', function () {
  const sections = document.querySelectorAll('section');
  const navLinks = document.querySelectorAll('nav a');

  navLinks.forEach(link => {
    link.addEventListener('click', function (e) {
      e.preventDefault();
      const targetSection = document.querySelector(link.getAttribute('href'));

      // Hide all sections
      sections.forEach(section => section.style.display = 'none');
      
      // Show the target section
      targetSection.style.display = 'block';
    });
  });

  // Show the News section by default
  document.querySelector('#news').style.display = 'block';
});
