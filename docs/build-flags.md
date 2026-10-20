---
layout: default
title: "Build Flags - PitchBlack Recovery Project"
permalink: /docs/build-flags/
---

<div class="max-w-4xl mx-auto py-12 px-4">
  
  <div class="mb-10">
    <a href="{{ '/docs/' | relative_url }}" class="text-sm text-muted hover:text-fg mb-4 inline-block transition-colors"><i class="fas fa-arrow-left mr-2"></i> Back to Docs</a>
    <h1 class="text-4xl font-display font-bold text-fg mb-4 border-l-4 border-fg pl-4">Build Flags</h1>
    <p class="text-muted text-lg">Custom flags to configure PBRP for your specific device tree in <code class="text-fg bg-fg/10 px-2 py-0.5 rounded text-base">BoardConfig.mk</code>.</p>
  </div>

  <div class="space-y-6">

    <!-- Flag Item -->
    <div class="bg-surface border border-fg/15 rounded-xl p-6 hover:border-fg/30 transition-colors">
      <div class="flex justify-between items-start mb-4">
        <h3 class="text-xl font-bold text-fg">Official Build</h3>
        <span class="px-2 py-1 rounded text-xs font-bold bg-fg text-bg border border-fg">RECOMMENDED</span>
      </div>
      <p class="text-muted mb-4">Marks the build as an Official release. This affects versioning string and branding.</p>
      <div class="bg-bg rounded-lg border border-fg/15 p-4 font-mono text-sm text-fg/80 overflow-x-auto">
        PB_OFFICIAL := true
      </div>
    </div>

    <!-- Flag Item -->
    <div class="bg-surface border border-fg/15 rounded-xl p-6 hover:border-fg/30 transition-colors">
      <div class="flex justify-between items-start mb-4">
        <h3 class="text-xl font-bold text-fg">Disable Default DM-Verity</h3>
        <span class="px-2 py-1 rounded text-xs font-bold bg-fg/5 text-fg border border-fg/25">OPTIONAL</span>
      </div>
      <p class="text-muted mb-4">Disables dm-verity checks by default. useful for devices that fail to boot after modification.</p>
      <div class="bg-bg rounded-lg border border-fg/15 p-4 font-mono text-sm text-fg/80 overflow-x-auto">
        PB_DISABLE_DEFAULT_DM_VERITY := true
      </div>
    </div>

    <!-- Flag Item -->
    <div class="bg-surface border border-fg/15 rounded-xl p-6 hover:border-fg/30 transition-colors">
      <div class="flex justify-between items-start mb-4">
        <h3 class="text-xl font-bold text-fg">Custom Torch Path</h3>
        <span class="px-2 py-1 rounded text-xs font-bold bg-fg/5 text-fg border border-fg/25">DEVICE SPECIFIC</span>
      </div>
      <p class="text-muted mb-4">If the flashlight toggle doesn't work, you may need to specify the correct sysfs path.</p>
      <div class="bg-bg rounded-lg border border-fg/15 p-4 font-mono text-sm text-fg/80 overflow-x-auto">
        PB_TORCH_PATH := /sys/class/leds/flashlight
      </div>
    </div>

    <!-- Flag Item (Deprecated) -->
    <div class="bg-surface/60 border border-fg/10 rounded-xl p-6 opacity-75">
      <div class="flex justify-between items-start mb-4">
        <h3 class="text-lg font-bold text-muted line-through">PBRP GO Support</h3>
        <span class="px-2 py-1 rounded text-xs font-bold bg-fg/5 text-fg border border-fg/25">DEPRECATED</span>
      </div>
      <p class="text-muted mb-4">Was used for low-memory devices. Removed in PBRP 3.0.0+.</p>
      <div class="bg-bg/50 rounded-lg border border-fg/10 p-4 font-mono text-sm text-muted/70 overflow-x-auto select-none">
        PB_GO := TRUE
      </div>
    </div>

  </div>
</div>
