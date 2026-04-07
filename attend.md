---
layout: default
title: Attend
permalink: /attend/
hero-image: /assets/hero-attend.png
---

## Registration

All registrations are processed through [ConCat](https://www.concat.app/) and paid via Stripe.

Registration is only complete when:

- Payment is received
- Code of Conduct is accepted
- Liability waiver is signed

<div id="reg-button" class="my-3">
    <a href="#" class="btn btn-success btn-lg d-none" id="reg-open">Register on ConCat</a>
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
                <h4 class="card-title fw-bold" style="color: #234c41;">Camper</h4>
                <p class="text-muted">The standard weekend experience.</p>
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
                <h4 class="card-title fw-bold" style="color: #234c41;">Survivalist</h4>
                <p class="text-muted">For those who want to rough it.</p>
                <ul>
                    <li>Everything in Camper</li>
                    <li>Tent camping in designated areas</li>
                    <li>Bring your own camping equipment</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="col">
        <div class="card h-100 shadow-sm">
            <div class="card-body">
                <h4 class="card-title fw-bold" style="color: #234c41;">Trailblazer</h4>
                <p class="text-muted">Go above and beyond to support F.L.A.W.</p>
                <ul>
                    <li>Everything in Survivalist</li>
                    <li>Exclusive Trailblazer badge</li>
                    <li>Early cabin selection</li>
                    <li>Support the event and future growth</li>
                </ul>
            </div>
        </div>
    </div>
</div>

<div class="row row-cols-1 row-cols-md-2 g-4 my-2">
    <div class="col">
        <div class="card h-100 shadow-sm border-secondary">
            <div class="card-body">
                <h5 class="card-title fw-bold">Day Badge</h5>
                <p class="text-muted mb-0">Single-day admission. Access to activities and programming for the day. Meals not included.</p>
            </div>
        </div>
    </div>
    <div class="col">
        <div class="card h-100 shadow-sm border-secondary">
            <div class="card-body">
                <h5 class="card-title fw-bold">Minor Badge</h5>
                <p class="text-muted mb-1">For attendees under 18.</p>
                <ul class="small mb-0">
                    <li>Ages 0&ndash;14 must be accompanied by a parent or legal guardian at all times</li>
                    <li>Ages 15&ndash;17 can attend with notarized permission from a parent or legal guardian</li>
                    <li>Guardians assume full responsibility for minors</li>
                </ul>
            </div>
        </div>
    </div>
</div>

## Capacity

Attendance is capped at **100**.
