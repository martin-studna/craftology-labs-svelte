<script>
    import emailjs from 'emailjs-com';

    emailjs.init("XkaO0JVBgvP3phBzS")

    let name = $state('');
    let company = $state('');
    let jobtitle = $state('');
    let email = $state('');
    let phone = $state('');
    let message = $state('');

    const sendEmail = () => {


        // validate inputs
        if (name === "" || email === "" || message === "") {
            alert('Please fill in all required fields.');
            return;
        }

        // validate email format
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (emailRegex.test(email) === false) {
            alert('Please enter a valid email address.');
            return;
        }

        // validate phone number format if provided
        if (phone.v) {
            const phoneRegex = /^\+?[\d\s-()]{8,}$/;
            if (phoneRegex.test(phone.v) === false) {
                alert('Please enter a valid phone number. (e.g. +420 123 456 789)');
                return;
            }
        }

        // validate message length
        if (message.length < 10) {
            alert('Please enter a message with at least 10 characters.');
            return;
        }

        const params = {
            name: name,
            company: company,
            jobtitle: jobtitle,
            email: email,
            phone: phone,
            message: message
        }

        emailjs.send('service_93qgher', 'template_3al002i', params)
        .then((response) => {
            console.log('SUCCESS!', response.status, response.text);
            name = '';
            company = '';
            jobtitle = '';
            email = '';
            phone = '';
            message = '';
            alert('E-mail sent successfully.');
        }, (err) => {
            alert('E-mail failed to send.');
        });

    }

    function autoResize(e) {
        e.target.style.height = "auto";
        e.target.style.height = e.target.scrollHeight + "px";
    }



</script>

<form onsubmit={sendEmail}  class="contact-form">
    <div class="content">
      <div class="input-wrapper">
        <input placeholder="" id="name" name="name" bind:value={name}  class="transparent-border" />
        <label for="name">Name</label>
      </div>
      <div class="input-wrapper">
        <input id="company" placeholder="" bind:value={company} name="company" class="transparent-border" />
        <label for="company" class=""><span>Company</span></label><span style="color: gray;">Optional</span>
      </div>
      <div class="input-wrapper">
        <input placeholder="" id="jobtitle" name="jobtitle" bind:value={jobtitle} class="transparent-border" />
        <label for="jobtitle" class=""><span>Job
            title</span></label><span style="color: gray;">Optional</span>
      </div>
      <div class="input-wrapper">
        <input placeholder="" id="email" name="email" bind:value={email} class="transparent-border" />
        <label for="email" class=""><span style="color: gray;">Business
            email</span></label>
      </div>
      <div>
        <div class="input-wrapper">
          <input placeholder="" id="phone" type="tel" bind:value={phone} class="transparent-border" />
          <label for="phone"><span>Phone</span></label>
          <span style="color: gray;">Optional</span>
        </div>
      </div>
      <div class="input-wrapper">
        <textarea bind:value={message} placeholder="" oninput={autoResize}
          id="message" name="message" class="transparent-border"></textarea>
        <label for="message" class=""><span>Message</span></label>
      </div>
    </div>
    <button class="submit-button" type="submit">Send message</button>
</form>

<style>
    .transparent-border {
        @apply border-transparent focus:border-transparent focus:ring-0;
    }


    .submit-button {
        margin-top: 20px;
        padding: 15px 30px;
        border-radius: 30px;
        background-color: #f5f5f5;
        color: #000;
        font-weight: 300;
        font-size: 1em;
        border: none;
        cursor: pointer;
        transition: all 0.1s linear;
    }

    .submit-button:hover {
        background-color: black;
        color: white;
        outline: 2px solid white;
    }

    .submit-button:active {
        background-color: #ffffff;
        color: black;
    }

    .input-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        position: relative;
        border-bottom: 1px solid gray;
        width: 500px;
    }

    .input-wrapper label {
        font-weight: 300;
        position: absolute;
        top: 1em;
        transform-origin: left;
        transition: all 0.3s ease;
        color: gray;
    }

    .input-wrapper input {
        width: 100%;
        padding: 10px;
        height: 100%;
        border-radius: 5px;
        border: none;
        background: transparent;
        color: white;
        font-size: 1.1rem;
        color: black;

    }

    .input-wrapper input:focus {
        outline: none;
        border: none;
    }

    .input-wrapper input:focus + label,
    .input-wrapper input:not(:placeholder-shown) + label {
        transform: translateY(-1.8em);
        font-size: 0.8rem !important;
    }

    .input-wrapper textarea {
        width: 100%;
        padding: 10px;
        height: auto;
        border-radius: 5px;
        border: none;
        background: transparent;
        color: black;
        font-size: 1.1rem;
        resize: none;
    }

    .input-wrapper textarea:focus {
        outline: none !important;
        border: none !important;
    }

    .input-wrapper textarea:focus + label,
    .input-wrapper textarea:not(:placeholder-shown) + label {
        transform: translateY(-1.8em);
        font-size: 0.8rem !important;
    }

    .contact-form {
        margin-top: 5rem;
        margin-bottom: 5rem;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    @media (max-width: 768px) {
        .input-wrapper {
            width: 100%;
        }
    }
</style>