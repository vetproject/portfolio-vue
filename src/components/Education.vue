<template>
    <div class="education">
        <h1>Education & Work</h1>
        <p>This section highlights my educational background and achievements.</p>
        <p>Below is a timeline of my academic journey and qualifications.</p>
    </div>
    <div class="timeline">

        <div v-for="(item, index) in timelineItems" :key="index" :class="['timeline-item', item.position]">
            <div v-if="item.position === 'left'" class="timeline-content">
                <h2>{{ item.title }}</h2>
                <h3 class="school">{{ item.school }}</h3>
                <p v-html="item.description"></p>
            </div>
            <div class="timeline-date">
                <!-- <span class="icon" v-html="item.icon"></span> -->
                <span>{{ item.date }}</span>
            </div>
            <div v-if="item.position === 'right'" class="timeline-content">
                <h2>{{ item.title }}</h2>
                <h3 class="school">{{ item.school }}</h3>
                <p v-html="item.description"></p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'EducationPort',
    data() {
        return {
            timelineItems: [
                {
                    position: 'left',
                    title: 'NORTHEASTERN UNIVERSITY CAMBODIA',
                    school: 'Bachelor of Information Technology',
                    description:
                        'Developed websites using HTML, CSS, JavaScript, PHP, and MySQL.<br></br>Created user-friendly web applications.<br></br>Managed databases with MySQL for efficient data access.<br></br>Developed the Buspad app using Java/Kotlin in Android Studio.<br></br>Designed simple screens and implemented real-time update features.<br></br>Tested the app to ensure reliability and performance.',
                    icon: '&#127891;',
                    date: 'DEC 2024 - PRESENT',
                },
                {
                    position: 'right',
                    title: 'Dai-ichi Life Insurance (Cambodia) Plc.',
                    school: 'Application Developer Intern',
                    description:
                        'Worked with the Application Developer team (Core and MIS).<br>Used SQL Server and Report Builder to develop business reports.<br>Supported and maintained MIS systems.',
                    icon: '&#127891;',
                    date: 'AUG - NOV 2024',
                },
                {
                    position: 'left',
                    title: 'PASSERELLES NUMÉRIQUES CAMBODIA',
                    school: 'Information Technology , Web Development',
                    description:
                        'Completed a comprehensive two-year program focused on information technology and web development. Gained hands-on experience in HTML, CSS, JavaScript, Vue.js, Laravel, Node.js, databases like MySQL, and participated in many project-based learning activities. <br><strong>Graduated in February 2025.</strong>',
                    icon: '&#127891;',
                    date: '2013 - PRESENT',
                },
                {
                    position: 'right',
                    title: 'BANTEAY CHHMAR HIGH SCHOOL',
                    school: 'High School Diploma',
                    description:
                        'Graduated from Banteay Chhmar High School with a focus on science. <br><strong>Graduated in 2022.</strong>',
                    icon: '&#128269;',
                    date: 'MAR - MAY 2015',
                },
                
            ],
        };
    },
};
</script>
<style scoped>
.education {
    width: 50%;
    margin: 0 auto;
}
.education h1 {
    font-size: 2rem;
    font-weight: 900;
    margin-bottom: 0.5rem;
    text-align: center;
    font-family: 'Montserrat', 'Arial Black', Arial, sans-serif;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #19d4d4;
    text-shadow: 1px 2px 8px rgba(25, 212, 212, 0.15);
}
.timeline {
    position: relative;
    max-width: 900px;
    margin: 40px auto;
    padding: 40px 0;
}

.timeline:before {
    content: '';
    position: absolute;
    left: 50%;
    top: 0;
    transform: translateX(-50%);
    width: 4px;
    height: 100%;
    background: #19d4d4;
    z-index: 0;
    border-radius: 2px;
}

.timeline-item {
    display: flex;
    justify-content: flex-end;
    align-items: flex-start;
    position: relative;
    width: 50%;
    padding: 30px 40px;
    box-sizing: border-box;
}

.timeline-item.left {
    left: 0;
    flex-direction: row;
    text-align: left;
}

.timeline-item.right {
    left: 50%;
    flex-direction: row-reverse;
    text-align: left;
}

.timeline-content {
    background: #181d23;
    color: #fff;
    padding: 24px 28px;
    border-radius: 8px;
    box-shadow: 0 2px 16px rgba(0, 0, 0, 0.25);
    min-width: 320px;
    max-width: 400px;
    position: relative;
    z-index: 2;
}

.timeline-content h2 {
    margin: 0 0 8px 0;
    font-size: 1.25rem;
    font-weight: bold;
    letter-spacing: 1px;
}

.timeline-content .school {
    color: #19d4d4;
    font-size: 1rem;
    margin-bottom: 12px;
    margin-top: 0;
}

.timeline-content p {
    margin: 0;
    font-size: 1rem;
    line-height: 1.6;
}

.timeline-content strong {
    color: #fff;
    font-weight: bold;
}

.timeline-date {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: #222b34;
    color: #fff;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    position: absolute;
    top: 40px;
    z-index: 3;
    font-size: 0.95rem;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    border: 4px solid #19d4d4;
}

.timeline-item.left .timeline-date {
    right: -35px;
}

.timeline-item.right .timeline-date {
    left: -35px;
}

.timeline-date .icon {
    font-size: 1.6rem;
    margin-bottom: 4px;
    color: #19d4d4;
}
span{
    font-size: 6px;
    color: #fff;
}

@media (max-width: 600px) {
    .timeline:before {
        left: 20px;
        transform: none;
    }

    .timeline-item,
    .timeline-item.left,
    .timeline-item.right {
        width: 100%;
        left: 0px;
        flex-direction: row;
        text-align: left;
        padding-left: 70px;
        padding-right: 20px;
    }
    .timeline-item.left .timeline-date {
        left: -15px;
    }
    .timeline-item.right .timeline-date {
        left: -15px;
    }

    .timeline{
        margin-left:18px ;
    }
    .education{
        width: 90%;
    }
}
</style>