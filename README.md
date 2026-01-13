<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Atlas Conciergerie | Airbnb & Booking Co‑Hosting in Morocco</title>
  <style>
    body { font-family: Arial, sans-serif; margin:0; line-height:1.6; }
    header { background:#0f172a; color:#fff; padding:40px 20px; text-align:center; }
    nav { background:#020617; color:#fff; padding:10px; text-align:right; }
    nav button { margin-left:10px; padding:6px 10px; cursor:pointer; }
    section { padding:40px 20px; max-width:1100px; margin:auto; }
    h2 { color:#0f172a; }
    .services, .steps { display:grid; grid-template-columns: repeat(auto-fit,minmax(220px,1fr)); gap:20px; }
    .card { border:1px solid #e5e7eb; padding:20px; border-radius:8px; }
    footer { background:#0f172a; color:#fff; text-align:center; padding:20px; }
    .cta { background:#2563eb; color:#fff; padding:12px 20px; display:inline-block; margin-top:20px; border-radius:6px; text-decoration:none; }
    .rtl { direction: rtl; text-align: right; }
  </style>
</head>
<body>

<nav>
  <button onclick="setLang('en')">EN</button>
  <button onclick="setLang('fr')">FR</button>
  <button onclick="setLang('ar')">AR</button>
</nav>

<header>
  <h1 id="title"></h1>
  <p id="subtitle"></p>
  <a href="#contact" class="cta" id="cta"></a>
</header>

<section>
  <h2 id="services_title"></h2>
  <div class="services" id="services"></div>
</section>

<section>
  <h2 id="why_title"></h2>
  <p id="why_text"></p>
</section>

<section>
  <h2 id="how_title"></h2>
  <div class="steps" id="steps"></div>
</section>

<section id="contact">
  <h2 id="contact_title"></h2>
  <p id="contact_text"></p>
  <p><strong>WhatsApp:</strong> +212 XXX XXX XXX</p>
  <p><strong>Email:</strong> contact@atlasconciergerie.com</p>
</section>

<footer>
  <p>© 2026 Atlas Conciergerie – Morocco</p>
</footer>

<script>
const content = {
  en: {
    dir: 'ltr',
    title: 'Atlas Conciergerie',
    subtitle: 'Professional Airbnb & Booking.com Co‑Hosting Services Across Morocco',
    cta: 'Free Consultation',
    services_title: 'Our Services',
    services: [
      'Listing creation & optimization',
      '24/7 guest communication',
      'Dynamic pricing management',
      'Cleaning & maintenance coordination',
      'Check‑in / Check‑out management',
      'Monthly performance reports'
    ],
    why_title: 'Why Choose Us',
    why_text: 'We maximize your rental income while delivering an exceptional guest experience, thanks to local expertise and transparent management.',
    how_title: 'How It Works',
    steps: ['Contact us','Property evaluation','Listing optimization','Full management & reporting'],
    contact_title: 'Contact Us',
    contact_text: 'Get in touch today and start earning more from your property.'
  },
  fr: {
    dir: 'ltr',
    title: 'Atlas Conciergerie',
    subtitle: 'Services professionnels de co‑hosting Airbnb & Booking.com au Maroc',
    cta: 'Consultation gratuite',
    services_title: 'Nos Services',
    services: [
      'Création et optimisation des annonces',
      'Communication voyageurs 24/7',
      'Gestion dynamique des prix',
      'Coordination ménage et maintenance',
      'Gestion check‑in / check‑out',
      'Rapports de performance mensuels'
    ],
    why_title: 'Pourquoi Nous Choisir',
    why_text: 'Nous augmentons vos revenus locatifs tout en assurant une expérience client irréprochable.',
    how_title: 'Comment Ça Marche',
    steps: ['Contact','Évaluation du bien','Optimisation','Gestion complète'],
    contact_title: 'Contact',
    contact_text: 'Contactez‑nous pour une gestion sans stress de votre bien.'
  },
  ar: {
    dir: 'rtl',
    title: 'أطلس للكونسيرج',
    subtitle: 'خدمات احترافية لإدارة Airbnb و Booking في جميع أنحاء المغرب',
    cta: 'استشارة مجانية',
    services_title: 'خدماتنا',
    services: [
      'إنشاء وتحسين الإعلانات',
      'التواصل مع الضيوف 24/7',
      'إدارة الأسعار بذكاء',
      'تنظيم التنظيف والصيانة',
      'إدارة تسجيل الدخول والخروج',
      'تقارير أداء شهرية'
    ],
    why_title: 'لماذا نحن',
    why_text: 'نزيد من أرباحك ونضمن تجربة ممتازة للضيوف بفضل خبرتنا المحلية.',
    how_title: 'كيف نعمل',
    steps: ['تواصل معنا','تقييم العقار','تحسين الإعلان','إدارة كاملة'],
    contact_title: 'تواصل معنا',
    contact_text: 'ابدأ الآن واستفد من إدارة احترافية لعقارك.'
  }
};

function setLang(lang){
  const c = content[lang];
  document.body.className = c.dir === 'rtl' ? 'rtl' : '';
  document.documentElement.dir = c.dir;
  title.innerText = c.title;
  subtitle.innerText = c.subtitle;
  cta.innerText = c.cta;
  services_title.innerText = c.services_title;
  services.innerHTML = c.services.map(s=>`<div class='card'>${s}</div>`).join('');
  why_title.innerText = c.why_title;
  why_text.innerText = c.why_text;
  how_title.innerText = c.how_title;
  steps.innerHTML = c.steps.map(s=>`<div class='card'>${s}</div>`).join('');
  contact_title.innerText = c.contact_title;
  contact_text.innerText = c.contact_text;
}

setLang('en');
</script>

</body>
</html>
