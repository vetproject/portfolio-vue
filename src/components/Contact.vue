<template>
    <div class="contact-container">
        <div class="contact-header">
            <h2>Have a sweet project in mind or just want to say hi?</h2>
            <p>Feel free to send me a message!</p>
        </div>
        <form class="contact-form">
            <div>
                <label for="name">NAME</label>
                <input type="text" id="name" name="name" autocomplete="off" />
            </div>
            <div>
                <label for="email">EMAIL</label>
                <input type="email" id="email" name="email" autocomplete="off" />
            </div>
            <div>
                <label for="subject">SUBJECT</label>
                <input type="text" id="subject" name="subject" autocomplete="off" />
            </div>
            <div>
                <label for="message">MESSAGE</label>
                <textarea id="message" name="message" rows="3"></textarea>
            </div>
            <button type="submit">SEND MESSAGE</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'ContactPort',
};
</script>

<style scoped>
.contact-container {
    padding: 40px 30px;
    background: linear-gradient(135deg, #1e90ff 0%, #6a11cb 100%);
    color: #fff;
}

.contact-header {

    text-align: center;
    margin-bottom: 32px;
}

.contact-header h2 {
    font-size: 1.7rem;
    font-weight: 600;
    margin-bottom: 10px;
    color: #fff;
}

.contact-header p {
    font-size: 1.1rem;
    color: #e0e0e0;
}

.contact-form {
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
}

.contact-form label {
    display: block;
    font-weight: 700;
    margin-bottom: 6px;
    letter-spacing: 1px;
    color: #fff;
}

.contact-form input,
.contact-form textarea {
    width: 100%;
    padding: 10px 0;
    background: transparent;
    border: none;
    border-bottom: 2px solid #ccc;
    color: #fff;
    font-size: 1rem;
    margin-bottom: 24px;
    outline: none;
    transition: border-color 0.3s;
    resize: none;
}

.contact-form input:focus,
.contact-form textarea:focus {
    border-bottom: 2px solid #00bcd4;
}

.contact-form input[type="email"] {
    border-bottom: 2px solid #00bcd4;
}

.contact-form button {
    display: block;
    width: 180px;
    margin: 30px auto 0 auto;
    padding: 12px 0;
    background: transparent;
    border: 2px solid #00bcd4;
    color: #00bcd4;
    font-size: 1rem;
    font-weight: 700;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.3s, color 0.3s;
}

.contact-form button:hover {
    background: #00bcd4;
    color: #fff;
}
</style>