---
layout: default
title: "PitchBlack Recovery Project"
---
{% assign devs = site.oem | sort: "title" %}
{% assign oem_groups = site.oem | group_by: "oem" | sort: "name" %}

<!-- HERO -->
<section id="home" class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center py-10 lg:py-24">
  <div class="lg:col-span-7">
    <p class="inline-flex items-center gap-2 text-[11px] font-mono uppercase tracking-wider text-muted border border-fg/20 rounded-full px-3 py-1 mb-6"><span class="h-1.5 w-1.5 rounded-full bg-fg"></span> Open source · TWRP 3.7.1 base</p>
    <h1 class="font-display font-black text-fg text-3xl sm:text-5xl lg:text-6xl leading-[1.1] break-words tracking-tight">The recovery built for people who flash.</h1>
    <p class="mt-6 text-lg text-muted max-w-xl leading-relaxed">PBRP is the most advanced open-source Android recovery. Back up, restore, flash and troubleshoot your device on the go.</p>
    <div class="mt-8 flex flex-wrap gap-3">
      <a href="#devices" class="btn btn-primary"><i class="fas fa-download"></i> Download</a>
      <a href="{{ '/docs/' | relative_url }}" class="btn btn-ghost"><i class="fas fa-book"></i> Docs</a>
    </div>
    <dl class="mt-12 grid grid-cols-2 sm:grid-cols-4 gap-px bg-fg/15 border border-fg/15 rounded-2xl overflow-hidden">
      {% assign stats = devs.size | append: "|Devices|" | append: oem_groups.size | append: "|Brands|10+|Tools|10+|Languages" | split: "|" %}
      {% for i in (0..3) %}{% assign n = i | times: 2 %}{% assign m = n | plus: 1 %}
      <div class="bg-bg p-4"><dt class="font-display font-bold text-2xl text-fg">{{ stats[n] }}</dt><dd class="text-xs text-muted uppercase tracking-wider mt-1">{{ stats[m] }}</dd></div>
      {% endfor %}
    </dl>
  </div>

  <div class="lg:col-span-5">
    <div class="border border-fg/20 rounded-2xl bg-surface overflow-hidden">
      <div class="flex items-center gap-2 px-4 py-3 border-b border-fg/15">
        <span class="h-3 w-3 rounded-full border border-fg/40"></span><span class="h-3 w-3 rounded-full border border-fg/40"></span><span class="h-3 w-3 rounded-full border border-fg/40"></span>
        <span class="ml-2 text-xs font-mono text-muted">~/pbrp</span>
      </div>
      <div class="codebox !border-0 !rounded-none !mb-0 !bg-transparent !p-5 !pr-12 leading-8">
<span class="text-muted">$</span> adb reboot bootloader<br><span class="text-muted">$</span> fastboot boot pbrp.img<br><span class="text-muted">$</span> fastboot reboot
      </div>
      <p class="px-5 pb-5 text-xs text-muted">Boot the image, then flash the PBRP zip from Install to make it permanent.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about" class="py-16 border-t border-fg/15">
  <div class="flex flex-col md:flex-row md:items-end md:justify-between gap-4 mb-10">
    <h2 class="font-display font-bold text-fg text-3xl">Why PBRP</h2>
    <p class="text-muted max-w-xl">Founded on 28 March 2018 by developers from many countries, to deliver the world’s most capable recovery with deep customization.</p>
  </div>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-px bg-fg/15 border border-fg/15 rounded-2xl overflow-hidden">
    {% assign feats = "fa-tools|Advanced Toolbox|10+ tools for your device, including Magisk Manager integration.|fa-mobile-alt|Wide Device Support|Treble, ARB support, force encryption and much more.|fa-paint-brush|Theme Engine|Customize PBRP with the PBRP Theme Engine™.|fa-layer-group|Material Design UI|A clean, modern interface for the latest Android.|fa-sync|Latest TWRP Base|Built on TWRP 3.7.1 for modern and legacy devices.|fa-language|Multi-Language|Official support for 10+ languages, updated regularly." | split: "|" %}
    {% for i in (0..5) %}{% assign n = i | times: 3 %}{% assign t = n | plus: 1 %}{% assign d = n | plus: 2 %}
    <div class="bg-bg p-7 group hover:bg-surface transition-colors">
      <div class="flex items-center justify-between mb-8"><i class="fas {{ feats[n] }} text-xl text-fg"></i><span class="font-mono text-xs text-muted">0{{ forloop.index }}</span></div>
      <h3 class="font-bold text-fg text-lg mb-2">{{ feats[t] }}</h3>
      <p class="text-sm text-muted leading-relaxed">{{ feats[d] }}</p>
    </div>
    {% endfor %}
  </div>
</section>

<!-- REQUIREMENTS -->
<section id="requirements" class="py-16 border-t border-fg/15 grid grid-cols-1 lg:grid-cols-12 gap-10">
  <div class="lg:col-span-4"><h2 class="font-display font-bold text-fg text-3xl mb-3">Before you start</h2><p class="text-muted">Everything you need ready on your computer and device.</p></div>
  <div class="lg:col-span-8">
    <ul class="divide-y divide-fg/15 border border-fg/15 rounded-2xl">
      {% assign reqs = "Unlocked bootloader (device-specific process)|USB debugging enabled|ADB and Fastboot installed on your computer|Proper USB drivers for your device|A complete backup of your important data" | split: "|" %}
      {% for r in reqs %}<li class="flex items-center gap-4 p-4 text-fg/85"><i class="far fa-circle-check text-fg"></i>{{ r }}</li>{% endfor %}
    </ul>
    <p class="mt-4 flex gap-3 text-sm text-muted border border-dashed border-fg/30 rounded-xl p-4"><i class="fas fa-triangle-exclamation mt-0.5 text-fg"></i><span><strong class="text-fg">Warning:</strong> installing a custom recovery may void your warranty. Always follow the device-specific guide.</span></p>
  </div>
</section>

<!-- DEVICES -->
<section id="devices" class="py-16 border-t border-fg/15">
  <div class="flex items-end justify-between gap-4 mb-6">
    <h2 class="font-display font-bold text-fg text-2xl sm:text-3xl">Supported devices</h2>
    <p class="text-sm text-muted font-mono whitespace-nowrap shrink-0"><span id="dev-count">{{ devs.size }}</span> shown</p>
  </div>
  <div class="sticky top-16 z-30 -mx-4 px-4 py-3 bg-bg/90 backdrop-blur border-b border-fg/10">
    <div class="relative max-w-2xl">
      <i class="fas fa-search absolute left-4 top-1/2 -translate-y-1/2 text-muted"></i>
      <input type="search" id="device-search" aria-label="Search devices" autocomplete="off" placeholder="Search device or codename…  ( / )" class="w-full bg-surface text-fg pl-11 pr-4 py-3 rounded-xl border border-fg/20 focus:border-fg outline-none placeholder:text-muted">
    </div>
    <div id="chips" class="flex gap-2 mt-3 overflow-x-auto pb-1">
      <button class="chip" data-oem="" aria-pressed="true">All</button>
      {% for g in oem_groups %}<button class="chip capitalize" data-oem="{{ g.name }}" aria-pressed="false">{{ g.name }} <span class="opacity-60">{{ g.items.size }}</span></button>{% endfor %}
    </div>
  </div>
  <div id="device-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3 mt-6">
    {% for d in devs %}
    <a href="{{ d.url | relative_url }}" class="device-item group flex items-center justify-between gap-3 p-4 rounded-xl border border-fg/15 hover:border-fg hover:bg-surface transition-colors" data-oem="{{ d.oem }}" data-q="{{ d.title | downcase }} {{ d.codename | downcase }} {{ d.oem | downcase }}">
      <div class="min-w-0"><p class="text-[11px] uppercase tracking-widest text-muted capitalize">{{ d.oem }}</p><p class="font-semibold text-fg truncate">{{ d.title }}</p><p class="text-xs font-mono text-muted">{{ d.codename }}</p></div>
      <i class="fas fa-arrow-right -rotate-45 text-muted group-hover:text-fg group-hover:rotate-0 transition-transform"></i>
    </a>
    {% endfor %}
  </div>
  <p id="no-results" class="hidden text-center py-12 text-muted">No devices found. Try another name or codename.</p>
</section>

<!-- COMMUNITY + DONATE -->
<section id="donate" class="my-8 rounded-3xl bg-fg text-bg p-8 md:p-14 grid grid-cols-1 md:grid-cols-2 gap-10">
  <div id="community">
    <h2 class="font-display font-bold text-3xl mb-3">Join the community</h2>
    <p class="opacity-70 mb-6">Get support, updates and contribute to development.</p>
    <div class="flex flex-wrap gap-3">
      <a href="https://t.me/pbrpcom" target="_blank" rel="noopener" class="btn border border-bg/40 !text-bg hover:bg-bg/10"><i class="fab fa-telegram"></i> Telegram</a>
      <a href="https://github.com/PitchBlackRecoveryProject" target="_blank" rel="noopener" class="btn border border-bg/40 !text-bg hover:bg-bg/10"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>
  <div>
    <h2 class="font-display font-bold text-3xl mb-3">Support PBRP</h2>
    <p class="opacity-70 mb-6">A small team gives its time for free. Your donation keeps PBRP alive.</p>
    <div class="flex flex-wrap gap-3">
      <a href="https://www.patreon.com/pitchblackrecovery" target="_blank" rel="noopener" class="btn bg-bg !text-fg hover:opacity-85"><i class="fab fa-patreon"></i> Patreon</a>
      <a href="https://opencollective.com/pitchblackrecovery" target="_blank" rel="noopener" class="btn border border-bg/40 !text-bg hover:bg-bg/10"><i class="fas fa-hand-holding-heart"></i> Open Collective</a>
    </div>
  </div>
</section>

<!-- FAQ -->
<section id="faq" class="py-16 grid grid-cols-1 lg:grid-cols-12 gap-10">
  <h2 class="lg:col-span-4 font-display font-bold text-fg text-3xl">FAQ</h2>
  <div class="lg:col-span-8 divide-y divide-fg/15 border-y border-fg/15">
    {% assign faq = "What is PBRP?|PitchBlack Recovery Project is a feature-rich custom recovery based on TWRP 3.7.1, with a unique black interface and improved functionality for backup, restore and system modification.|How do I install PBRP?|Methods vary by device: fastboot, Odin (Samsung) or SP Flash Tool (MediaTek). Always follow the guide on your device’s page.|Is PBRP safe?|Yes, when used correctly. Always back up first, follow the instructions carefully and verify that your device is supported.|What makes PBRP different from TWRP?|PBRP is based on TWRP 3.7.1 but adds a distinctive theme, enhanced UI and extra features, with regular updates and device-specific optimizations.|Can I contribute to PBRP?|Yes! Maintain devices, report bugs or improve the code. Visit our GitHub to get started." | split: "|" %}
    {% for i in (0..4) %}{% assign q = i | times: 2 %}{% assign a = q | plus: 1 %}
    <details class="group py-5">
      <summary class="flex items-center justify-between gap-4 cursor-pointer list-none font-semibold text-fg">{{ faq[q] }}<i class="fas fa-plus text-sm text-muted transition-transform group-open:rotate-45"></i></summary>
      <p class="mt-3 text-muted leading-relaxed max-w-2xl">{{ faq[a] }}</p>
    </details>
    {% endfor %}
  </div>
</section>

<script>
  (() => {
    const items = [...document.querySelectorAll('.device-item')], chips = [...document.querySelectorAll('.chip')];
    const input = document.getElementById('device-search'), count = document.getElementById('dev-count'), empty = document.getElementById('no-results');
    let oem = '';
    function apply() {
      const q = input.value.trim().toLowerCase(); let n = 0;
      items.forEach(el => { const ok = (!oem || el.dataset.oem === oem) && (!q || el.dataset.q.includes(q)); el.classList.toggle('hidden', !ok); if (ok) n++; });
      count.textContent = n; empty.classList.toggle('hidden', n > 0);
    }
    input.addEventListener('input', apply);
    chips.forEach(c => c.addEventListener('click', () => { oem = c.dataset.oem; chips.forEach(x => x.setAttribute('aria-pressed', x === c)); apply(); }));
  })();
</script>
