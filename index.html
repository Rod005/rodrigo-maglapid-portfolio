const menuBtn = document.querySelector('.menu-btn');
const navLinks = document.querySelector('.nav-links');
const themeBtn = document.querySelector('.theme-btn');
const root = document.documentElement;

menuBtn?.addEventListener('click', () => {
  const open = navLinks.classList.toggle('open');
  menuBtn.setAttribute('aria-expanded', String(open));
});

document.querySelectorAll('.nav-links a').forEach(link => {
  link.addEventListener('click', () => navLinks.classList.remove('open'));
});

document.getElementById('year').textContent = new Date().getFullYear();

const savedTheme = localStorage.getItem('portfolio-theme');
if (savedTheme === 'light') root.classList.add('light');
themeBtn?.addEventListener('click', () => {
  root.classList.toggle('light');
  localStorage.setItem('portfolio-theme', root.classList.contains('light') ? 'light' : 'dark');
});

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) entry.target.classList.add('visible');
  });
}, { threshold: 0.12 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

const counters = document.querySelectorAll('[data-count]');
const counterObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (!entry.isIntersecting) return;
    const el = entry.target;
    const target = Number(el.dataset.count || 0);
    let current = 0;
    const step = Math.max(1, Math.ceil(target / 30));
    const timer = setInterval(() => {
      current = Math.min(target, current + step);
      el.textContent = `${current}+`;
      if (current >= target) clearInterval(timer);
    }, 35);
    counterObserver.unobserve(el);
  });
}, { threshold: 0.8 });
counters.forEach(el => counterObserver.observe(el));

const glow = document.querySelector('.cursor-glow');
window.addEventListener('pointermove', event => {
  if (!glow) return;
  glow.style.left = `${event.clientX}px`;
  glow.style.top = `${event.clientY}px`;
});

if (matchMedia('(pointer:fine)').matches) {
  document.querySelectorAll('.tilt-card').forEach(card => {
    card.addEventListener('pointermove', event => {
      const rect = card.getBoundingClientRect();
      const x = (event.clientX - rect.left) / rect.width - 0.5;
      const y = (event.clientY - rect.top) / rect.height - 0.5;
      card.style.transform = `perspective(1000px) rotateX(${y * -4}deg) rotateY(${x * 4}deg) translateY(-3px)`;
    });
    card.addEventListener('pointerleave', () => {
      card.style.transform = '';
    });
  });
}

const form = document.getElementById('contact-form');
const nextInput = document.getElementById('form-next');
if (nextInput) nextInput.value = `${window.location.origin}${window.location.pathname}?sent=1#contact`;
if (new URLSearchParams(window.location.search).get('sent') === '1') {
  const note = document.getElementById('form-note');
  if (note) note.textContent = 'Thank you. Your inquiry was submitted successfully.';
}
if (form) {
  form.addEventListener('submit', () => {
    const button = form.querySelector('button[type="submit"]');
    button.disabled = true;
    button.innerHTML = 'Sending...';
  });
}
