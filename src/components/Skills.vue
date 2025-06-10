<template>
    <div class="skills-container">
        <h1 class="skills-title">Skills</h1>
        <div class="skills-underline"></div>
        <div class="skills-sections-row" style="display: flex; gap: 2rem;">
            <div class="skills-section" style="flex: 1;">
                <div class="skills-header">
                    <span class="skills-icon">⚙️</span>
                    <span class="skills-dev-title">DEVELOPMENT</span>
                </div>
                <div class="skills-list">
                    <div v-for="skill in skills" :key="skill.name" class="skill-item">
                        {{ skill.name }}
                    </div>
                </div>
            </div>
            <div class="skills-section" style="flex: 0.5;">
                <div class="skills-header">
                    <span class="skills-icon">🛠️</span>
                    <span class="skills-dev-title">TOOLS</span>
                </div>
                <div class="skills-list">
                    <div v-for="tool in tools" :key="tool.name" class="tool-item">
                        <span class="tool-check">✔</span> {{ tool.name }}
                    </div>
                </div>
            </div>
            <div class="skills-section" style="flex: 0.5;">
                <div class="skills-header">
                    <span class="skills-icon">📚</span>
                    <span class="skills-dev-title">KNOWLEDGE</span>
                </div>
                <div class="skills-list">
                    <div v-for="item in knowledge" :key="item.name" class="tool-item">
                        <span class="tool-check">✔</span> {{ item.name }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillsPort',
    data() {
        return {
            skills: [
                { name: 'HTML' },
                { name: 'CSS' },
                { name: 'JavaScript' },
                { name: 'Vue.js' },
                { name: 'Laravel' },
                { name: 'Node.js' },
                { name: 'MySQL' },
            ],
            tools: [
                { name: 'Git + GitHub' },
                { name: 'Visual Studio Code' },
                { name: 'Postman' },
                { name: 'Figma' },
            ],
            knowledge: [
                { name: 'RESTful APIs' },
                { name: 'Responsive Design' },
                { name: 'Agile Methodologies' },
            ],
        };
    },
};
</script>

<style scoped>
.skills-container {
    background: #181818;
    color: #fff;
    padding: 32px 24px;
    min-height: 100vh;
    font-family: 'Segoe UI', Arial, sans-serif;
}

.skills-title {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
}

.skills-underline {
    width: 60px;
    height: 3px;
    background: #00bfff;
    margin-bottom: 2rem;
}

.skills-section {
    margin-top: 2rem;
}

.skills-header {
    display: flex;
    align-items: center;
    font-size: 1.3rem;
    font-weight: bold;
    margin-bottom: 2rem;
}

.skills-icon {
    font-size: 2rem;
    margin-right: 0.7rem;
}

.skills-dev-title {
    letter-spacing: 1px;
}

.skills-list {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: flex-start;
}

.skill-item {
    width: 55px;
    height: 55px;
    border: 1.5px solid #333;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.7rem;
    background: #222;
    margin-bottom: 1rem;
    text-align: center;
    padding: 5px;
}

.skill-item:hover {
    border: 1.5px solid #00bfff;
    background: #232b36;
}

/* Responsive styles */
@media (max-width: 900px) {
    .skills-sections-row {
        flex-direction: column !important;
        gap: 1.5rem !important;
    }
    .skills-section {
        margin-top: 1.5rem;
    }
}

@media (max-width: 600px) {
    .skills-container {
        padding: 16px 8px;
    }
    .skills-title {
        font-size: 2rem;
    }
    .skills-header {
        font-size: 1rem;
        margin-bottom: 1rem;
    }
    .skills-list {
        gap: 0.5rem;
    }
    .skill-item {
        width: 45px;
        height: 45px;
        font-size: 0.6rem;
        padding: 5px;
    }
}
</style>
