<script>
    let firstName = ''
    let lastName = ''
    let email = ''
    let message = ''

function handleSubmit(){
    alert("Form Submitted")
}
</script>
<h1>Contact</h1>
<section class="flow">
<p>Please complete this form for more information. Thank you.</p>

<form on:submit|preventDefault={handleSubmit}>
    <div>
        <label for="first-name">First Name</label>
        <input type="text" id="first-name" name="first-name"
        bind:value="{firstName}"
        placeholder="Enter first name..." required/>
        </div>

    <div>
        <label for="last-name">Last Name</label>
        <input type="text" id="last-name" name="last-name"
        bind:value="{lastName}"
        placeholder="Enter last name..." required/>
        </div>

    <div>
        <label for="email">Email</label>
        <input type="text" id="email" name="email"
        bind:value="{email}"
        placeholder="Enter email address..." required/>
        </div>

    <div>
        <label for="message">Message</label>
        <textarea name="message" rows="10"
        bind:value="{message}"
        placeholder="Enter message..."required></textarea>
    </div>

    <button>Submit</button>
</form>
</section>

<style>
    form {
        max-width: 32rem;
        display:grid;
        gap: 1.5rem;
    }

    div{
        display: grid;
        gap: 0.5rem;
    }

    input, textarea {
        padding: 0.5rem;
        font-family: inherit;
    }
</style>