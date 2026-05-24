<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AIRDROP - About Us</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">

    <style>
        /* GLOBAL STYLES: Resets margins and applies the font family everywhere */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }
        
        /* BODY STYLES: Sets the dark background color for the entire page */
        body {
            background-color: #0b1020;
            color: #e6ecff;
        }

        /* SECTION PADDING: Controls the spacing on the left and right of the website */
        section {
            padding: 4% 10%;
        }

        /* HEADER STYLING: Controls the top welcome text area */
        .intro-header {
            text-align: center;
            padding: 40px 10%;
            background-color: #070c1a;
        }

        .intro-header h1 {
            font-size: 42px;
            color: #e6ecff;
            margin-bottom: 10px;
        }

        .intro-header p {
            color: #ce1446;
            font-weight: 500;
        }

        /* ABOUT US GRID Layout: Splits the image and text into a 2-column grid */
        .about-us {
            width: 100%;
            min-height: 100vh;
            background-color: #0b1020;
            display: grid;
            grid-template-columns: 1.4fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        /* TEAM IMAGE STYLING: Makes the full team image responsive with smooth corners */
        .main-img img {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 8px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.5);
        }

        /* TEXT STYLING: Colors, text sizing, and spacing for the headers */
        .text {
            padding: 6% 0;
            display: flex;
            flex-direction: column;
        }

        .text h4 {
            color: #ce1446;
            font-size: 16px;
            font-weight: 500;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .text h1 {
            color: #e6ecff;
            font-size: 36px;
            text-transform: capitalize;
            font-weight: 700;
            line-height: 46px;
            margin-bottom: 30px;
        }

        /* DECORATIVE LINE (The red line under the title) */
        hr {
            width: 30%;
            border: none;
            height: 2px;
            background-color: #ce1446;
            margin-bottom: 50px;
        }

        .text p {
            max-width: 600px;
            color: #e6ecff;
            font-size: 15px;
            font-weight: 400;
            line-height: 1.7;
            margin-bottom: 40px;
        }

        .text-row {
            display: grid;
            grid-template-columns: 2fr 1fr;
            align-items: center;
            gap: 40px;
        }

        /* STATISTICS BLOCK (20+ Hours, 2500+ Reached placement) */
        .last-text {
            display: flex;
            gap: 40px;
            flex-direction: column;
            align-items: flex-start;
        }

        .text1 {
            margin-right: 60px;
            flex-direction: column;
        }

        .last-text h3 {
            color: #ce1446;
            font-size: 60px;
            font-weight: 700;
            line-height: 1;
        }

        .last-text h5 {
            color: #e6ecff;
            font-size: 18px;
            font-weight: 500;
            margin-top: 6px;
        }

        /* GROUP PHOTO BUTTON: Custom crimson red styling to match your theme */
        .btn-container {
            margin-bottom: 40px;
        }

        .group-photo-btn {
            background-color: #ce1446;
            color: white;
            padding: 14px 28px;
            font-size: 16px;
            font-weight: 600;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.3s ease, transform 0.2s ease;
            text-decoration: none;
            display: inline-block;
        }

        /* BUTTON HOVER STATE: darkens the color and gives a subtle lift when mouse hovers */
        .group-photo-btn:hover {
            background-color: #a80f39;
            transform: translateY(-2px);
        }

        /* CONTACT SECTION LAYOUT */
        .contact {
            background: #070c1a;
            padding: 6% 10%;
            color: #e6ecff;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .contact-info h4 {
            color: #ce1446;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .contact-info h1 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        .contact-info p {
            line-height: 1.7;
            margin-bottom: 20px;
            max-width: 500px;
        }

        .contact-details p {
            margin-bottom: 10px;
        }

        /* CONTACT FORM INPUT FIELDS STYLING */
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-form input,
        .contact-form textarea {
            background: #0b1020;
            border: 1px solid #1c2545;
            padding: 14px;
            color: #fff;
            border-radius: 6px;
            font-family: 'Montserrat', sans-serif;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #ce1446;
        }

        /* SUBMIT MESSAGE BUTTON STYLING */
        .contact-form button {
            background: #ce1446;
            color: white;
            padding: 14px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: 0.3s;
        }

        .contact-form button:hover {
            background: #a80f39;
        }

        /* MOBILE RESPONSIVENESS: Stacks elements vertically on smaller screen resolutions */
        @media (max-width: 1024px) {
            .about-us {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .main-img {
                order: -1;
                max-width: 800px;
                margin: 0 auto;
            }

            .text-row {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .last-text {
                flex-direction: row;
                justify-content: center;
                width: 100%;
            }

            hr {
                margin: 0 auto 30px auto;
            }
        }

        @media (max-width: 900px) {
            .contact-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header class="intro-header">
        <h1>Welcome to AIRDROP</h1>
        <p>Made in the United Kingdom, by students.</p>
    </header>

    <section class="about-us"> 
        
        <div class="main-img">
            <img src="image_65ffe4.png" alt="AIRDROP CanSat Team">
        </div>

        <div class="text">
            <h4>About</h4>
            <h1>We Are A Team Of Students Developing An Autonomous, Can-Sized Satellite For Advanced Aerospace Research.</h1>
            <hr>

            <div class="text-row">
                <div>
                    <p>
                        We are a team of six students working together to design and build our own CanSat,
                        and from the beginning it’s been more than just a project, it’s something we’ve
                        grown into as we’ve learned new skills and taken on challenges we’d never faced before.
                        From planning and pitching ideas to developing our website, running outreach and
                        engineering the satellite itself, each stage has pushed us to think differently,
                        solve real problems and work like a proper technical team.
                    </p>
                    
                    <div class="btn-container">
                        <a href="image_65ffe4.png" target="_blank" class="group-photo-btn">View Full-Size Group Photo</a>
                    </div>
                </div>

                <div class="last-text">
                    <div class="text1">
                        <h3>20+</h3>
                        <h5>Hours Invested</h5>
                    </div>

                    <div class="text2">
                        <h3>2500+</h3>
                        <h5>People Reached</h5>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact">
        <div class="contact-container">
            
            <div class="contact-info">
                <h4>Contact</h4>
                <h1>Get In Touch</h1>
                <p>
                    Have questions about our CanSat project, collaboration opportunities,
                    or outreach events? We'd love to hear from you.
                </p>

                <div class="contact-details">
                    <p><strong>Email:</strong> utcairdrop@icloud.com</p>
                    <p><strong>Location:</strong> United Kingdom</p>
                </div>
            </div>

            <form class="contact-form">
                <input type="text" placeholder="Your Name" required>
                <input type="email" placeholder="Email Address" required>
                <textarea placeholder="Your Message" rows="5" required></textarea>
                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

</body>
</html>
