
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.about-title {
    font-size: 7.5rem;
    font-weight: 900;
    letter-spacing: -0.02em;
    position: absolute;
    top: 45px;
    left: 50%;
    transform: translateX(-50%);
    pointer-events: none;
    white-space: nowrap;
    background: linear-gradient(
        to bottom,
        rgb(255, 255, 255) 30%,
        rgb(255 255 255 / 0%) 76%
    );
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}
.carousel-container {
    width: 100%;
    max-width: 1200px;
    height: 450px;
    position: relative;
    perspective: 1000px;
    margin-top: 80px;
}
.carousel-track {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.card {
    position: absolute;
    width: 280px;
    height: 380px;
    background: white;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
    transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    cursor: pointer;
}
.card img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.card.center {
    z-index: 10;
    transform: scale(1.1) translateZ(0);
}
.card.center img {
    filter: none;
}
.card.left-2 {
    z-index: 1;
    transform: translateX(-400px) scale(0.8) translateZ(-300px);
    opacity: 0.7;
}
.card.left-2 img {
    filter: grayscale(100%);
}
.card.left-1 {
    z-index: 5;
    transform: translateX(-200px) scale(0.9) translateZ(-100px);
    opacity: 0.9;
}
.card.left-1 img {
    filter: grayscale(100%);
}
.card.right-1 {
    z-index: 5;
    transform: translateX(200px) scale(0.9) translateZ(-100px);
    opacity: 0.9;
}
.card.right-1 img {
    filter: grayscale(100%);
}
.card.right-2 {
    z-index: 1;
    transform: translateX(400px) scale(0.8) translateZ(-300px);
    opacity: 0.7;
}
.card.right-2 img {
    filter: grayscale(100%);
}
.card.hidden {
    opacity: 0;
    pointer-events: none;
}
.member-info {
    text-align: center;
    margin-top: 40px;
    transition: all 0.5s ease-out;
}
.member-name {
    color: #fff;
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 10px;
    position: relative;
    display: inline-block;
}
.member-name::before,
.member-name::after {
    content: "";
    position: absolute;
    top: 100%;
    width: 100px;
    height: 2px;
    background: #b51836;
}
.member-name::before {
    left: -120px;
}
.member-name::after {
    right: -120px;
}
.member-role {
    color: #b51836;
    font-size: 1.5rem;
    font-weight: 500;
    opacity: 0.8;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    padding: 10px 0;
    margin-top: -15px;
    position: relative;
}
.dots {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-top: 60px;
}
.dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #fff;
    cursor: pointer;
    transition: all 0.3s ease;
}
.dot.active {
    background: #b51836;
    transform: scale(1.2);
}
.nav-arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: #b51836;
    color: #fff;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 20;
    transition: all 0.3s ease;
    font-size: 1.5rem;
    border: none;
    outline: none;
    padding-bottom: 4px;
}
.nav-arrow:hover {
    background: #93142c;
    transform: translateY(-50%) scale(1.1);
}
.nav-arrow.left {
    left: 20px;
    padding-right: 3px;
}
.nav-arrow.right {
    right: 20px;
    padding-left: 3px;
}
@media (max-width: 768px) {
    .about-title {
        font-size: 4.5rem;
    }
    .card {
        width: 200px;
        height: 280px;
    }
    .card.left-2 {
        transform: translateX(-250px) scale(0.8) translateZ(-300px);
    }
    .card.left-1 {
        transform: translateX(-120px) scale(0.9) translateZ(-100px);
    }
    .card.right-1 {
        transform: translateX(120px) scale(0.9) translateZ(-100px);
    }
    .card.right-2 {
        transform: translateX(250px) scale(0.8) translateZ(-300px);
    }
    .member-name {
        font-size: 2rem;
    }
    .member-role {
        font-size: 1.2rem;
    }
    .member-name::before,
    .member-name::after {
        width: 50px;
    }
    .member-name::before {
        left: -70px;
    }
    .member-name::after {
        right: -70px;
    }
</style>

<h1 class="about-title">Unser Team</h1>

<div class="carousel-container">
  <button class="nav-arrow left">‹</button>
  <div class="carousel-track">
    <div class="card" data-index="0">
      <img src="https://images.unsplash.com/photo-1600878459138-e1123b37cb30?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8OTJ8fHBlcnNvbnxlbnwwfDF8MHx8fDA%3D" alt="Team Member 1">
    </div>
    <div class="card" data-index="1">
      <img src="https://images.unsplash.com/photo-1614786269829-d24616faf56d?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mzl8fHBlcnNvbnxlbnwwfDF8MHx8fDA%3D" alt="Team Member 2">
    </div>
    <div class="card" data-index="2">
      <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NDh8fHBlcnNvbnxlbnwwfDF8MHx8fDA%3D" alt="Team Member 3">
    </div>
    <div class="card" data-index="3">
      <img src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8ODN8fHBlcnNvbnxlbnwwfDF8MHx8fDA%3D" alt="Team Member 4">
    </div>
    <div class="card" data-index="4">
      <img src="https://images.unsplash.com/photo-1581403341630-a6e0b9d2d257?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTUxfHxwZXJzb258ZW58MHwxfDB8fHww" alt="Team Member 5">
    </div>
    <div class="card" data-index="5">
      <img src="https://images.unsplash.com/photo-1589696485114-9e2f81d83484?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTE0fHxwZXJzb258ZW58MHwxfDB8fHww" alt="Team Member 6">
    </div>
  </div>
  <button class="nav-arrow right">›</button>
</div>

<div class="member-info">
  <h2 class="member-name">David Kim</h2>
  <p class="member-role">Founder</p>
</div>

<div class="dots">
  <div class="dot active" data-index="0"></div>
  <div class="dot" data-index="1"></div>
  <div class="dot" data-index="2"></div>
  <div class="dot" data-index="3"></div>
  <div class="dot" data-index="4"></div>
  <div class="dot" data-index="5"></div>
</div>

<script>
// Team-Mitglieder Namen und Rollen
const teamMembers = [
    { name: "John Q.", role: "CEO" },
    { name: "Susan E.", role: "Office" },
    { name: "Nuigel R.", role: "Developer" },
    { name: "Julia G.", role: "UX Designer" },
    { name: "Lisa A.", role: "Manager" },
    { name: "Anna W.", role: "Manager" }
];
const cards = document.querySelectorAll(".card");
const dots = document.querySelectorAll(".dot");
const memberName = document.querySelector(".member-name");
const memberRole = document.querySelector(".member-role");
const leftArrow = document.querySelector(".nav-arrow.left");
const rightArrow = document.querySelector(".nav-arrow.right");
let currentIndex = 0;
let isAnimating = false;
function updateCarousel(newIndex) {
    if (isAnimating) return;
    isAnimating = true;
    currentIndex = (newIndex + cards.length) % cards.length;
    cards.forEach((card, i) => {
        const offset = (i - currentIndex + cards.length) % cards.length;
        card.classList.remove(
            "center",
            "left-1",
            "left-2",
            "right-1",
            "right-2",
            "hidden"
        );
        if (offset === 0) {
            card.classList.add("center");
        } else if (offset === 1) {
            card.classList.add("right-1");
        } else if (offset === 2) {
            card.classList.add("right-2");
        } else if (offset === cards.length - 1) {
            card.classList.add("left-1");
        } else if (offset === cards.length - 2) {
            card.classList.add("left-2");
        } else {
            card.classList.add("hidden");
        }
    });
    dots.forEach((dot, i) => {
        dot.classList.toggle("active", i === currentIndex);
    });
    memberName.style.opacity = "0";
    memberRole.style.opacity = "0";
    setTimeout(() => {
        memberName.textContent = teamMembers[currentIndex].name;
        memberRole.textContent = teamMembers[currentIndex].role;
        memberName.style.opacity = "1";
        memberRole.style.opacity = "1";
    }, 300);
    setTimeout(() => {
        isAnimating = false;
    }, 800);
}
leftArrow.addEventListener("click", () => {
    updateCarousel(currentIndex - 1);
});
rightArrow.addEventListener("click", () => {
    updateCarousel(currentIndex + 1);
});
dots.forEach((dot, i) => {
    dot.addEventListener("click", () => {
        updateCarousel(i);
    });
});
cards.forEach((card, i) => {
    card.addEventListener("click", () => {
        updateCarousel(i);
    });
});
document.addEventListener("keydown", (e) => {
    if (e.key === "ArrowLeft") {
        updateCarousel(currentIndex - 1);
    } else if (e.key === "ArrowRight") {
        updateCarousel(currentIndex + 1);
    }
});
let touchStartX = 0;
let touchEndX = 0;
document.addEventListener("touchstart", (e) => {
    touchStartX = e.changedTouches[0].screenX;
});
document.addEventListener("touchend", (e) => {
    touchEndX = e.changedTouches[0].screenX;
    handleSwipe();
});
function handleSwipe() {
    const swipeThreshold = 50;
    const diff = touchStartX - touchEndX;
    if (Math.abs(diff) > swipeThreshold) {
        if (diff > 0) {
            updateCarousel(currentIndex + 1);
        } else {
            updateCarousel(currentIndex - 1);
        }
    }
}
updateCarousel(0);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
