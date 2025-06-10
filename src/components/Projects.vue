<template>

    <div class="projects-port">
        <h1 class="title">Some of My Work</h1>
        <div class="header-underline">
        </div>
        <section class="project-section" v-for="(project, idx) in projects" :key="idx">
            <div class="project-images">
                <img v-for="(img, imgIdx) in project.images" :key="imgIdx" :src="img"
                    :alt="project.title + ' Image ' + (imgIdx + 1)" class="main-image" />
            </div>
            <h2 class="project-title">{{ project.title.toUpperCase() }}</h2>
            <p class="project-description">
                {{ project.description }}
            </p>
            <div class="project-buttons">
                <a :href="project.demoLink" class="btn demo" target="_blank" rel="noopener">DEMO</a>
                <a :href="project.codeLink" class="btn code" target="_blank" rel="noopener">CODE</a>
            </div>
            <div class="project-tags">
                <span class="tag" v-for="(tag, i) in project.tags" :key="i">{{ tag.toUpperCase() }}</span>
            </div>
        </section>
    </div>

</template>
<script>
import userImage from '@/assets/project1.png';
import portfoliPhp from '@/assets/portfilophp.png';
import petshop from '@/assets/petshop.png';
import lmsimage from '@/assets/lms.png';
import puspad from '@/assets/buspad.png';
import card from '@/assets/card.png';
import inventory from '@/assets/inventory.png';
export default {

    name: 'ProjectsPort',
    data() {
        return {
            projects: [
                {
                    images: [
                        portfoliPhp,
                    ],
                    title: 'My First Portfolio',
                    description: 'This was my first portfolio website I built in 2025. It\'s a simple one-pager like this one, but relied heavily on Bootstrap. Since then, I think my web development and design skills have expanded immensely.',
                    tags: ['PHP', 'Bootstrap', 'JavaScript'],
                    demoLink: 'http://yrrin.atwebpages.com/',
                    codeLink: '#'
                },
                {
                    images: [
                        lmsimage,
                    ],
                    title: 'LMS System',
                    description: 'A Leave Management System for managing employee leave requests. Employees can submit leave applications to their managers, who can approve or reject the requests. The system streamlines leave tracking, approval workflows, and helps organizations manage employee attendance efficiently. This project was developed as part of a school assignment, allowing me to apply concepts learned in class to a real-world scenario and collaborate with classmates on both frontend and backend development.',
                    tags: ['PHP', 'Boostrap', 'JavaScript', 'MySQL'],
                    demoLink: '#',
                    codeLink: 'https://github.com/So-panha/g7-lms.git'
                },
                {
                    images: [
                        userImage,
                    ],
                    title: 'Point of Sale System',
                    description: 'A Point of Sale system designed for retail businesses to manage sales, inventory, and customer transactions. It features real-time sales tracking, receipt generation, inventory alerts, and detailed analytics to help businesses optimize their operations. I created this project while completing a JavaScript course.',
                    tags: ['HTML', 'CSS', 'JavaScript'],
                    demoLink: '#',
                    codeLink: '#'
                },
                {
                    images: [
                        petshop,
                    ],
                    title: 'Pet Store Website',
                    description: 'A website for selling pets, pet supplies, and offering pet-related services. Customers can browse and purchase pets, buy pet materials, and book services such as grooming and veterinary appointments.',
                    tags: ['HTML', 'CSS', 'SASS'],
                    demoLink: '#',
                    codeLink: 'https://github.com/RinYouern/pet-shop-c5.git'
                },
                {
                    images: [
                        userImage,
                    ],
                    title: 'Easy Travel',
                    description: 'A website designed for travelers and visitors, allowing users to book hotels, rent cars, and discover famous places. The platform offers easy booking, travel recommendations, and helps users plan memorable trips.',
                    tags: ['LARAVEL', 'VUE.JS', 'Bootstrap','MySQL'],
                    demoLink: '#',
                    codeLink: '#'
                },
                {
                    images: [
                        puspad,
                    ],
                    title: 'BUSPAD',
                    description: 'Buspad is an app used on buses that allows customers to enjoy their ride by watching movies, listening to music, browsing the internet, and accessing YouTube, making travel more relaxing and entertaining.',
                    tags: ['JAVA', 'Kotlin', 'Android Studio'],
                    demoLink: '#',
                    codeLink: '#'
                },
                {
                    images: [
                        card,
                    ],
                    title: 'Card Management System',
                    description: 'A system for generating and managing digital employee cards. It allows organizations to create customizable employee ID cards, issue them securely, and validate them in real-time. Administrators can track card usage, manage employee records, and generate detailed reports.',
                    tags: ['PHP', 'Bootstrap', 'JavaScript'],
                    demoLink: 'http://vetem.onlinewebshop.net/',
                    codeLink: 'https://github.com/vetproject/employee_card'
                },
                {
                    images: [
                        inventory,
                    ],
                    title: 'Inventory Management System',
                    description: 'An inventory management system for businesses to track stock levels, manage suppliers, and process orders. The system provides automated alerts for low stock, detailed inventory analytics, and integration with sales channels.',
                    tags: ['PHP', 'Bootstrap', 'JavaScript', 'MySQL'],
                    demoLink: 'http://inventoryvet.onlinewebshop.net/products',
                    codeLink: 'https://github.com/vetproject/inventory'
                }


            ]
        };
    }
};
</script>

<style scoped>
.projects-port {
    padding: 2rem;
    background: #121212;
    color: #eaeaea;
}

.project-section {
    color: #eaeaea;
    margin: 2rem auto;
    padding: 2.5rem 2rem;
    border-radius: 12px;
    max-width: 900px;
    box-sizing: border-box;
}

.project-images {
    display: flex;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
    align-items: flex-start;
    flex-wrap: wrap;
}

.main-image {
    width: 100%;
    max-width: 900px;
    border-radius: 8px;
    box-shadow: 0 2px 16px rgba(0, 0, 0, 0.18);
    height: auto;
    object-fit: cover;
}

.project-title {
    font-size: 2rem;
    font-weight: 700;
    margin: 2rem 0 1rem 0;
    letter-spacing: 1px;
    color: #fff;
    text-transform: uppercase;
}

.project-description {
    font-size: 1.1rem;
    color: #b0b0b0;
    margin-bottom: 2rem;
    line-height: 1.7;
}

.project-buttons {
    margin-bottom: 1.5rem;
}

.btn {
    display: inline-block;
    padding: 0.6rem 1.6rem;
    margin-right: 1rem;
    border: 2px solid #00fff7;
    color: #00fff7;
    background: transparent;
    border-radius: 6px;
    font-weight: 600;
    letter-spacing: 1px;
    text-decoration: none;
    transition: background 0.2s, color 0.2s;
    margin-bottom: 0.5rem;
}

.btn:hover {
    background: #00fff7;
    color: #18191a;
}

.project-tags {
    margin-top: 1.5rem;
}

.tag {
    display: inline-block;
    background: #232425;
    color: #b0b0b0;
    font-size: 0.85rem;
    font-weight: 600;
    border-radius: 4px;
    padding: 0.35em 1em;
    margin-right: 0.5em;
    margin-bottom: 0.5em;
    letter-spacing: 1px;
    text-transform: uppercase;
    opacity: 0.85;
}

.title {
    font-size: 3rem;
    font-weight: bold;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
    margin-bottom: 0.5rem;
}

.header-underline {
    width: 100px;
    height: 3px;
    background: #00bfff;
    margin-bottom: 2rem;
}

/* Responsive styles */
@media (max-width: 900px) {
    .project-section {
        padding: 2rem 1rem;
        max-width: 100%;
    }
    .main-image {
        max-width: 100%;
    }
}

@media (max-width: 600px) {
    .projects-port {
        padding: 1rem;
    }
    .title {
        font-size: 2rem;
    }
    .project-section {
        padding: 1.2rem 0.5rem;
        margin: 1rem 0;
    }
    .project-title {
        font-size: 1.3rem;
        margin: 1.2rem 0 0.7rem 0;
    }
    .project-description {
        font-size: 1rem;
    }
    .project-images {
        flex-direction: column;
        gap: 1rem;
        align-items: stretch;
    }
    .main-image {
        max-width: 100%;
        width: 100%;
    }
    .btn {
        padding: 0.5rem 1.2rem;
        font-size: 0.5rem;
    }
    .tag {
        font-size: 0.75rem;
        padding: 0.25em 0.8em;
    }
    .header-underline {
        width: 60px;
        height: 2px;
    }
}
</style>