---
layout: default
title: "Documentation - PitchBlack Recovery Project"
permalink: /docs/
---

<div class="max-w-6xl mx-auto py-12 px-4">
  
  <!-- Header -->
  <div class="text-center mb-16">
    <h1 class="text-4xl md:text-5xl font-display font-bold text-fg mb-6 text-gradient">Documentation</h1>
    <p class="text-muted text-lg max-w-2xl mx-auto leading-relaxed">
      Welcome to the PBRP Documentation Center. Here you'll find comprehensive guides, build instructions, and technical documentation.
    </p>
  </div>

  <!-- Developer Cards Grid -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-12">
    
    <!-- Maintainer Card -->
    <div class="bg-surface border border-fg/15 rounded-2xl p-8 hover:border-fg/25 transition-all group relative overflow-hidden">
      <div class="absolute top-0 right-0 p-3 opacity-10 group-hover:opacity-20 transition-opacity">
        <i class="fas fa-crown text-8xl text-fg"></i>
      </div>
      <div class="relative z-10">
        <div class="w-14 h-14 rounded-xl bg-fg/5 flex items-center justify-center mb-6 text-fg group-hover:scale-110 transition-transform">
          <i class="fas fa-star text-2xl"></i>
        </div>
        <h3 class="text-2xl font-bold text-fg mb-3">Official Maintainer</h3>
        <p class="text-muted mb-8 min-h-[3rem]">Learn how to become an official PBRP device maintainer and join our team.</p>
        <a href="/official/" class="inline-flex items-center px-6 py-3 rounded-lg bg-fg text-bg font-bold hover:opacity-85 transition-colors shadow-lg ">
          <i class="fas fa-crown mr-2"></i> Apply Now
        </a>
      </div>
    </div>

    <!-- Build Flags Card -->
    <div class="bg-surface border border-fg/15 rounded-2xl p-8 hover:border-fg/25 transition-all group relative overflow-hidden">
      <div class="absolute top-0 right-0 p-3 opacity-10 group-hover:opacity-20 transition-opacity">
        <i class="fas fa-code text-8xl text-fg"></i>
      </div>
      <div class="relative z-10">
        <div class="w-14 h-14 rounded-xl bg-fg/5 flex items-center justify-center mb-6 text-fg group-hover:scale-110 transition-transform">
          <i class="fas fa-cogs text-2xl"></i>
        </div>
        <h3 class="text-2xl font-bold text-fg mb-3">Build Flags</h3>
        <p class="text-muted mb-8 min-h-[3rem]">Learn about custom PBRP build flags to use in your device tree's BoardConfig.mk.</p>
        <a href="/docs/build-flags/" class="inline-flex items-center px-6 py-3 rounded-lg bg-fg/5 border border-fg/15 text-fg font-bold hover:bg-fg/10 transition-colors">
          <i class="fas fa-book mr-2"></i> View Guide
        </a>
      </div>
    </div>

  </div>

  <!-- Bottom Section: Quick Links & Contributing -->
  <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
    
    <!-- Quick Links -->
    <div class="lg:col-span-2 bg-surface/60 border border-fg/15 rounded-2xl p-8">
      <h3 class="text-xl font-bold text-fg mb-6 border-b border-fg/15 pb-4">External Resources</h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
        <a href="https://github.com/PitchBlackRecoveryProject" target="_blank" class="flex items-center gap-4 p-4 rounded-xl bg-bg/40 hover:bg-fg/5 transition-colors border border-fg/10 hover:border-fg/15 group">
          <i class="fab fa-github text-2xl text-muted group-hover:text-fg transition-colors"></i>
          <div>
            <div class="text-fg font-medium">GitHub Organization</div>
            <div class="text-xs text-muted">Source code & Trees</div>
          </div>
        </a>
        <a href="https://t.me/pbrpcom" target="_blank" class="flex items-center gap-4 p-4 rounded-xl bg-bg/40 hover:bg-fg/5 transition-colors border border-fg/10 hover:border-fg/15 group">
          <i class="fab fa-telegram text-2xl text-fg group-hover:text-fg transition-colors"></i>
          <div>
            <div class="text-fg font-medium">Telegram Community</div>
            <div class="text-xs text-muted">Support & Chat</div>
          </div>
        </a>
        <a href="https://sourceforge.net/projects/pbrp/" target="_blank" class="flex items-center gap-4 p-4 rounded-xl bg-bg/40 hover:bg-fg/5 transition-colors border border-fg/10 hover:border-fg/15 group">
          <i class="fas fa-download text-2xl text-fg group-hover:text-fg transition-colors"></i>
          <div>
            <div class="text-fg font-medium">SourceForge</div>
            <div class="text-xs text-muted">File Repository</div>
          </div>
        </a>
      </div>
    </div>

    <!-- Contributing (Updated Links) -->
    <div class="bg-surface border border-fg/15 rounded-2xl p-8 flex flex-col justify-center text-center">
      <div class="w-16 h-16 bg-fg/5 rounded-full flex items-center justify-center mx-auto mb-4 text-fg/80">
        <i class="fas fa-code-branch text-2xl"></i>
      </div>
      <h3 class="text-lg font-bold text-fg mb-2">Contribute</h3>
      <p class="text-muted text-sm mb-6">Help us improve the project or report issues.</p>
      <div class="flex flex-col gap-3">
        <!-- Changed to Org Link -->
        <a href="https://github.com/PitchBlackRecoveryProject" target="_blank" class="px-4 py-2 rounded-lg bg-fg/5 hover:bg-fg/10 text-fg text-sm font-medium border border-fg/15 transition-colors">
          Visit GitHub Org
        </a>
        <!-- Kept specific Repo Link for Issues, or change to Org if preferred -->
        <a href="https://github.com/PitchBlackRecoveryProject/PitchBlackRecoveryProject.github.io/issues" target="_blank" class="px-4 py-2 rounded-lg bg-fg/5 hover:bg-fg/10 text-fg text-sm font-medium border border-fg/15 transition-colors">
          Report Website Issue
        </a>
      </div>
    </div>

  </div>
</div>
