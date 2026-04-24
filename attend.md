---
layout: default
title: Attend
permalink: /attend/
hero-image: 
  webp: /assets/hero-attend.webp
  fallback: /assets/hero-attend.png
---

<div class="alert alert-info">
<strong>Welcome to the great outdoors, furry style! Whether you're new to the woods or a seasoned camper, F.L.A.W. offers a fun, safe, and unforgettable weekend surrounded by nature and great company. Come make memories under the stars!</strong>
</div>

## Registration

<picture>
<source type="image/webp" srcset="/assets/regdog.webp">
<img src="/assets/regdog.png" alt="F.L.A.W. Registration Mascot" class="float-end ms-3 mb-3" style="max-height: 220px;">
</picture>

All registrations are processed through [ConCat](https://www.concat.app/) and paid via Stripe.

<div id="reg-button" class="my-3">
    <a href="https://reg.campflaw.org/" class="btn btn-success btn-lg d-none" id="reg-open" style="color: #fff !important;">Register</a>
    <button class="btn btn-secondary btn-lg" id="reg-countdown" disabled>
        Registration opens <span id="countdown-text"></span>
    </button>
</div>

<script>
(function() {
    var regDate = new Date('2026-04-08T18:00:00-04:00');
    var openBtn = document.getElementById('reg-open');
    var countdownBtn = document.getElementById('reg-countdown');
    var countdownText = document.getElementById('countdown-text');

    function update() {
        var now = new Date();
        var diff = regDate - now;

        if (diff <= 0) {
            openBtn.classList.remove('d-none');
            countdownBtn.classList.add('d-none');
            return;
        }

        var days = Math.floor(diff / 86400000);
        var hours = Math.floor((diff % 86400000) / 3600000);
        var minutes = Math.floor((diff % 3600000) / 60000);
        var seconds = Math.floor((diff % 60000) / 1000);

        var parts = [];
        if (days > 0) parts.push(days + 'd');
        if (hours > 0) parts.push(hours + 'h');
        parts.push(minutes + 'm');
        parts.push(seconds + 's');

        countdownText.textContent = 'in ' + parts.join(' ');
        setTimeout(update, 1000);
    }

    update();
})();
</script>

## Registration Types

<div class="row row-cols-1 row-cols-md-3 g-4 my-3">
    <div class="col">
        <div class="card h-100 shadow-sm">
            <div class="card-body">
                <h4 class="card-title fw-bold" style="color: #234c41;">Camper <span class="badge bg-secondary">$175</span></h4>
                <p class="text-muted">The original experience!</p>
                <ul>
                    <li>Full weekend admission</li>
                    <li>Cabin bunk assignment</li>
                    <li>6 meals included</li>
                    <li>Access to all activities and programming</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="col">
        <div class="card h-100 shadow-sm">
            <div class="card-body">
                <h4 class="card-title fw-bold" style="color: #234c41;">Survivalist <span class="badge bg-secondary">$250</span></h4>
                <p class="text-muted">Go above and beyond to support F.L.A.W.</p>
                <ul>
                    <li>Everything in Camper</li>
                    <li>Included t-shirt</li>
                    <li>Special token of our appreciation</li>
                    <li>Support the event and future growth</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="col">
        <div class="card h-100 shadow-sm">
            <div class="card-body">
                <h4 class="card-title fw-bold" style="color: #234c41;">Trailblazer <span class="badge bg-secondary">$325</span></h4>
                <p class="text-muted">The elevated glamping experience.</p>
                <ul>
                    <li>All items from previous tiers</li>
                    <li>Placement in exclusive premium cabin with full furnishing, bedding, water, and electricity</li>
                    <li>F.L.A.W. flask and mug</li>
                    <li>2 special gifts disclosed onsite</li>
                    <li>Custom badge of your sona drawn by our art department</li>
                </ul>
            </div>
        </div>
    </div>
</div>

<div class="row row-cols-1 row-cols-md-2 g-4 my-2">
    <div class="col">
        <div class="card h-100 shadow-sm border-secondary">
            <div class="card-body">
                <h5 class="card-title fw-bold">Day Badge <span class="badge bg-secondary">At-Con Only</span></h5>
                <p class="text-muted mb-0">Purchased on-site only. Single-day admission with access to activities and programming. Meals not included.</p>
            </div>
        </div>
    </div>
    <div class="col">
        <div class="card h-100 shadow-sm border-secondary">
            <div class="card-body">
                <h5 class="card-title fw-bold">Minor Policy <span class="badge bg-warning"><i class="bi bi-exclamation-triangle-fill px-2"></i></span></h5>
                <p class="text-muted mb-1">Finger Lakes Anthro Weekend is an all-ages event! For attendees under the age of 18, a few restrictions apply:</p>
                <ul class="small mb-0">
                    <li>Ages 0&ndash;14 must be accompanied by a parent or legal guardian at all times. The parent/legal guardian must register for the event under <strong>their own account,</strong> using their information not the child's.</li>
                    <li>Ages 15&ndash;17 can attend with notarized permission from a parent or legal guardian</li>
                    <li>Guardians assume full responsibility for minors</li>
                </ul>
            </div>
        </div>
    </div>
</div>

## Capacity

Attendance is capped at **100**.
