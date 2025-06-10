<template>
    <footer class="footer">
        <div class="footer-icons">
            <a href="#" aria-label="Email">
                <i class="fas fa-envelope"></i>
            </a>
            <a href="#" target="_blank" aria-label="Twitter">
                <i class="fab fa-twitter"></i>
            </a>
            <a href="#" target="_blank" aria-label="Instagram">
                <i class="fab fa-instagram"></i>
            </a>
            <a href="#" target="_blank" aria-label="CodePen">
                <i class="fab fa-codepen"></i>
            </a>
            <a href="#" target="_blank" aria-label="GitHub">
                <i class="fab fa-github"></i>
            </a>
            <a href="#" target="_blank" aria-label="LinkedIn">
                <i class="fab fa-linkedin-in"></i>
            </a>
        </div>
        <p class="footer-copyright">
            &copy; 2025 YOUERN RIN. All rights reserved.
        </p>
    </footer>
</template>
<script>
import '@fortawesome/fontawesome-free/css/all.css';
export default {
    name: 'FooterPort'
}
</script>
<style scoped>
.footer {
    background: linear-gradient(120deg, #06beb6, #8f6ed5 100%);
    padding: 60px 0 40px 0;
    text-align: center;
    color: #fff;
    border-top: 2px solid #222;
}

.footer-icons {
    margin-bottom: 30px;
}

.footer-icons a {
    color: #fff;
    margin: 0 18px;
    font-size: 2.2rem;
    transition: color 0.2s;
    display: inline-block;
    vertical-align: middle;
}

.footer-icons a:hover {
    color: #ffd700;
}

.footer-copyright {
    font-size: 1.1rem;
    margin-top: 10px;
    letter-spacing: 0.5px;
}

@media screen and (max-width: 600px) {
    .footer-icons a {
        margin: 0 10px;
        font-size: 1.8rem;
    }
    .footer-copyright {
        font-size: 1rem;
    }
    
}
</style>