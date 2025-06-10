<template>
    <div class="about-container">
        <div class="about-left">
            <h1>Hey, I'm Brittany.</h1>
            <h2>
                I'm a web developer passionate about combining beautiful code with beautiful design.
            </h2>
            <div class="about-right1">
                <div class="about-img-wrapper">
                    <img :src="userImage" alt="Profile" />
                </div>

            </div>
            <div class="about-underline"></div>
            <p class="about-bold">
                I'm a two years at PASSERELLES NUMÉRIQUES CAMBODIA
            </p>
            <p>
                As a web developer with a strong background in information technologies, I specialize in building responsive and efficient web applications. My experience includes working with modern frameworks, databases, and cloud services to deliver scalable solutions. I am passionate about leveraging technology to solve real-world problems and continuously improving my skills in the ever-evolving IT landscape.
            </p>
            <p>
                I love learning new and better ways to create seamless user experiences with clean, efficient, and
                scalable code. I consider work an ongoing education, and I'm always looking for opportunities to work
                with those who are willing to share their knowledge and expertise.
            </p>
        </div>
        <div class="about-right">
            <div class="about-img-wrapper">
                <img :src="userImage" alt="Profile" />
            </div>

        </div>
    </div>
</template>

<script>
import userImage from '@/assets/user.png';

export default {
    name: 'AboutPor',
    data() {
        return {
            userImage,
        };
    },
};
</script>

<style scoped>
.about-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-height: 100vh;
    background: #111;
    color: #fff;
    padding: 0 5vw;
}

.about-left {
    flex: 1.2;
    max-width: 600px;
}

.about-left h1 {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 1rem;
    font-family: 'Georgia', serif;
}

.about-left h2 {
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 1.5rem;
    color: #fff;
}

.about-underline {
    width: 110px;
    height: 3px;
    background: #19e6ff;
    margin-bottom: 1.5rem;
}

.about-bold {
    font-weight: bold;
    margin-bottom: 0.5rem;
    color: #fff;
}

.about-left p {
    color: #d3d3d3;
    margin-bottom: 1rem;
    line-height: 1.7;
}

.about-right {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.about-right1 {
    display: none;
}
.about-img-wrapper {
    width: 320px;
    height: 320px;
    background: #fff;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 2rem;
    overflow: hidden;
}

.about-img-wrapper img {
    width: 90%;
    height: auto;
    border-radius: 50%;
    object-fit: cover;
}

.about-nav {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 18px;
}

.about-nav li {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #444;
    transition: background 0.2s;
}

.about-nav li.active {
    background: #19e6ff;
}

@media (max-width: 900px) {
    .about-container {
        flex-direction: column;
        align-items: flex-start;
        padding: 2vw;
    }

    .about-right {
        display: none;
    }
    .about-right1 {
        display: block;
    }
}
</style>