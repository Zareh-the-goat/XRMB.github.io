
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XR Moon Engineering</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
            padding: 20px;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            overflow: hidden;
        }
        header {
            background: #333;
            color: white;
            padding: 40px 20px;
            text-align: center;
            position: relative;
        }
        .moon-drone {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .moon {
            width: 80px;
            height: 80px;
            background: radial-gradient(circle at 30% 30%, #fff, #f0f0f0 40%, #d3d3d3);
            border-radius: 50%;
            box-shadow: 0 0 20px rgba(255,255,255,0.3), inset -2px -2px 5px rgba(0,0,0,0.2);
        }
        .glasses {
            width: 80px;
            height: 40px;
            position: relative;
            border: 2px solid #fff;
            border-radius: 20px;
            background: transparent;
        }
        .glasses::before {
            content: '';
            position: absolute;
            top: 5px;
            left: 5px;
            width: 30px;
            height: 30px;
            border: 2px solid #fff;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
        }
        .glasses::after {
            content: '';
            position: absolute;
            top: 5px;
            right: 5px;
            width: 30px;
            height: 30px;
            border: 2px solid #fff;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
        }
        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        .content {
            padding: 40px;
        }
        .section {
            margin-bottom: 40px;
        }
        .section h2 {
            color: #667eea;
            margin-bottom: 20px;
            border-bottom: 2px solid #667eea;
            padding-bottom: 10px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #333;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: Arial, sans-serif;
        }
        textarea {
            resize: vertical;
            min-height: 100px;
        }
        button {
            background: #667eea;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            font-weight: bold;
            transition: background 0.3s;
        }
        button:hover {
            background: #764ba2;
        }
        .button-group {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }
        .donate-amount {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        .donate-btn {
            flex: 1;
            min-width: 100px;
            background: #27ae60;
            padding: 10px 20px;
        }
        .donate-btn:hover {
            background: #229954;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="moon-drone">
                <div class="moon"></div>
                <div class="glasses"></div>
            </div>
            <h1> XR Moon Engineering</h1>
            <p>Website made from Zareh.T</p>
        </header>
        
        <div class="content">
            <!-- Application Section -->
            <div class="section">
                <h2>Apply Now</h2>
                <form id="applicationForm">
                    <div class="form-group">
                        <label for="name">Full Name:</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email:</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone Number:</label>
                        <input type="tel" id="phone" name="phone" required>
                    </div>
                    <div class="form-group">
                        <label for="position">Position Applied For:</label>
                        <select id="position" name="position" required>
                            <option value="">Select a position</option>
                            <option value="Coder">Coder</option>
                            <option value="Builder">Builder</option>
                            <option value="Disigner">Designer</option>
                            <option value="Other">Other</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Tell us about yourself:</label>
                        <textarea id="message" name="message" required></textarea>
                        <p>Thank you, copy and paste the application then use the link below to submit it to zareh.tirinkian@pinecrest.edu.</p>
                        <p><a href="https://gmail.com" target="_blank" rel="noopener noreferrer">Submit Application</a></p>
                    </div>
                </form>
            </div>

            <!-- Donation Section -->
            <div class="section">
                <h2>Support our project pls</h2>
                <p style="margin-bottom: 20px;">pls donate</p>
                <form id="donationForm">
                    <div class="form-group">
                        <label for="donorName">Name:</label>
                        <input type="text" id="donorName" name="donorName" required>
                    </div>
                    <div class="form-group">
                        <label for="donorEmail">School gmail:</label>
                        <input type="email" id="donorEmail" name="donorEmail" required>
                    </div>
                    <div class="form-group">
                        <label>Donation Amount:</label>
                        <div class="donate-amount">
                            <button type="button" class="donate-btn" onclick="setDonation(25)">$25</button>
                            <button type="button" class="donate-btn" onclick="setDonation(50)">$50</button>
                            <button type="button" class="donate-btn" onclick="setDonation(100)">$100</button>
                            <button type="button" class="donate-btn" onclick="setDonation(500)">$500</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="customAmount">Custom Amount ($):</label>
                        <input type="number" id="customAmount" name="customAmount" min="1" placeholder="Enter custom amount">
                    </div>
                    <button type="submit">Donate</button>
                </form>
            </div>
        </div>
    </div>

    <script>
        // Application Form Handler
        document.getElementById('applicationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            const data = Object.fromEntries(formData);
            
            sendEmail('Application', data.name, data.email, data.phone, data.position, data.message);
            alert('Application submitted! Email sent to zareh.tirinkian@pinecrest.edu');
            this.reset();
        });

        // Donation Amount Setter
        function setDonation(amount) {
            document.getElementById('customAmount').value = amount;
        }

        // Donation Form Handler
        document.getElementById('donationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const amount = document.getElementById('customAmount').value || 0;
            const donorName = document.getElementById('donorName').value;
            
            alert(`Thank you for your donation of $${amount}! Here is the link to the zell,  zelle.com);
            this.reset();
        });

        // Email sending function (requires backend)
        function sendEmail(type, name, email, phone, position, message) {
            fetch('send-email.php', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    type: type,
                    name: name,
                    email: email,
                    phone: phone,
                    position: position,
                    message: message
                })
            });
        }
    </script>
</body>
</html>
