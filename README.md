<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adolf Hitler - Historical Analysis</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lora:wght@400;700&family=Ysabeau+SC:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #a83249; /* Deep Burgundy - Rich and historical */
            --secondary-color: #fdd592; /* Pale Yellow - Warm and inviting */
            --accent-color: #3a7d40; /* Forest Green - Nature, growth, but also somber */
            --background-color: #f8f8ff; /* White Smoke - Soft and clean background */
            --text-color-dark: #333;
            --text-color-light: #fff;
        }

        body {
            font-family: 'Lora', serif; /* Elegant and readable serif */
            line-height: 1.8;
            margin: 0;
            padding: 0;
            background-color: var(--background-color);
            color: var(--text-color-dark);
            overflow-x: hidden; /* Prevent horizontal scrollbar */
            animation: fadeIn 1s ease-out forwards; /* Initial fade-in animation */
            opacity: 0;

            /* Background Image for the whole page */
            background-image: url('jGlzr.png'); /* Replace with your image URL */
            background-size: cover; /* Cover the entire viewport */
            background-repeat: no-repeat; /* Prevent image repetition */
            background-attachment: fixed; /* Fixed background, creates a subtle parallax effect */
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }

        header {
            background: var(--primary-color); /* Deep burgundy header */
            color: var(--text-color-light);
            padding: 25px 0;
            box-shadow: 0 3px 8px rgba(0,0,0,0.2);
            position: relative;
            z-index: 100; /* Ensure header is above content */
        }

        nav {
            position: relative; /* For wave effect */
        }

        nav::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 20px; /* Height of the wave */
            background: var(--primary-color);
            clip-path: path('M0 0 L100% 0 L100% 100% C50% 150%, 50% 50%, 0 100% Z'); /* Wave shape */
        }


        nav ul {
            list-style: none;
            padding: 0;
            text-align: center;
            margin: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 25px;
            position: relative;
        }

        nav ul li a {
            color: var(--text-color-light);
            text-decoration: none;
            font-weight: 700;
            font-size: 1.2em;
            transition: color 0.3s ease, transform 0.3s ease; /* Smooth transitions */
            display: inline-block; /* Required for transform */
            padding-bottom: 5px; /* Space for underline */
        }

        nav ul li a:hover {
            color: var(--secondary-color); /* Pale yellow on hover */
            transform: translateY(-3px); /* Slight lift on hover */
        }

        nav ul li::after {
            content: '';
            position: absolute;
            width: 0;
            height: 3px;
            bottom: 0;
            left: 50%;
            background-color: var(--secondary-color); /* Pale yellow underline */
            transition: width 0.4s ease-in-out, left 0.4s ease-in-out;
        }

        nav ul li:hover::after,
        nav ul li.active::after {
            width: 100%;
            left: 0;
        }


        .hero {
            position: relative;
            color: var(--text-color-light);
            text-align: center;
            height: 700px; /* Increased hero height */
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: linear-gradient(to bottom, rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.7)); /* Gradient overlay */
        }

        .background-video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            animation: zoomInOut 12s linear infinite alternate; /* Subtle zoom animation */
        }

        @keyframes zoomInOut {
            0% { transform: scale(1); }
            100% { transform: scale(1.1); }
        }


        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5); /* Slightly darker overlay */
        }

        .hero-content {
            position: relative;
            z-index: 1;
            padding: 30px;
            animation: fadeInUp 1s ease-out 0.5s forwards; /* Fade up and in animation */
            opacity: 0;
            transform: translateY(20px);
        }

        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }


        .hero-content h1 {
            font-family: 'Ysabeau SC', serif; /* Stronger, historical font for title */
            font-size: 4.5em;
            margin-bottom: 15px;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.7);
            letter-spacing: 2px;
            color: var(--secondary-color); /* Pale Yellow title */
        }

        .hero-content .tagline {
            font-size: 1.4em;
            font-weight: 400;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.7);
            color: var(--background-color); /* White smoke tagline */
        }

        .content-section {
            padding: 60px 30px;
            margin: 40px 0;
            background: rgba(255, 255, 255, 0.85); /* Slightly transparent white content background */
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12);
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 1.2s ease-out, transform 1.2s ease-out;
            backdrop-filter: blur(5px); /* Subtle blur for glass effect */
            position: relative; /* For background pattern */
            overflow: hidden; /* Clip background pattern */
        }

        .content-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('jGlzr.png'); /* Replace with a subtle texture image */
            opacity: 0.05; /* Very subtle texture */
            pointer-events: none; /* Make sure it doesn't interfere with clicks */
        }


        .content-section.active {
            opacity: 1;
            transform: translateY(0);
        }

        .transparent-container {
            padding: 40px;
        }

        .content-section h2 {
            font-family: 'Ysabeau SC', serif;
            font-size: 3em;
            color: var(--primary-color); /* Burgundy section titles */
            margin-bottom: 30px;
            border-bottom: 3px double var(--accent-color); /* Forest green double border */
            padding-bottom: 15px;
            letter-spacing: 1px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.05);
        }

        .content-div {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 40px;
        }

        .content-div p {
            margin-bottom: 25px;
            text-align: justify;
            color: var(--text-color-dark);
            font-size: 1.05em;
            animation: fadeInText 1.5s ease-out 0.7s forwards; /* Fade in text with delay */
            opacity: 0;
        }

        @keyframes fadeInText {
            to { opacity: 1; }
        }


        .section-image {
            max-width: 70%; /* Adjusted max-width for better responsiveness */
            height: auto; /* Let height adjust automatically */
            border-radius: 15px;
            box-shadow: 6px 6px 12px rgba(0,0,0,0.15);
            transition: transform 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275); /* Bouncy scale animation */
            cursor: pointer;
            display: block; /* Prevent extra space below image */
            margin: 0 auto 20px auto; /* Center images and add spacing */
        }

        .section-image:hover {
            transform: scale(1.08);
        }

        footer {
            text-align: center;
            padding: 25px 0;
            background: var(--primary-color);
            color: var(--text-color-light);
            position: relative;
            width: 100%;
            box-shadow: 0 -3px 8px rgba(0,0,0,0.2);
            margin-top: 60px; /* Added margin to separate from content */
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 20px; /* Height of the wave */
            background: var(--primary-color);
            clip-path: path('M0 100% L100% 100% L100% 0 C50% -50%, 50% 50%, 0 0 Z'); /* Wave shape, inverted */
        }


        /* Responsive adjustments */
        @media screen and (min-width: 768px) {
            .content-div {
                flex-direction: row;
                align-items: flex-start;
                gap: 60px;
            }
            .content-div p {
                flex: 2;
            }
            .section-image {
                flex: 1;
                max-width: 100%; /* Back to 100% for larger screens in row layout */
                margin: 0 0 0 0; /* Reset margins for larger screens */
            }
            .hero-content h1 {
                font-size: 5em;
            }
            .hero-content .tagline {
                font-size: 1.6em;
            }
        }

        @media screen and (max-width: 767px) {
            .hero {
                height: auto;
                padding: 100px 20px;
            }
            .hero-content h1 {
                font-size: 3.5em;
            }
            .hero-content .tagline {
                font-size: 1.2em;
            }
            nav ul li {
                margin: 0 15px;
            }
            .content-section {
                padding: 40px 20px;
                margin: 20px 0;
            }
            .transparent-container {
                padding: 25px;
            }
            .content-div {
                gap: 30px;
            }
            .section-image {
                max-width: 85%; /* Slightly wider images on smaller screens */
            }
        }

    </style>
</head>
<body>

    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#early-life">Early Life</a></li>
                <li><a href="#rise-to-power">Rise to Power</a></li>
                <li><a href="#world-war-ii">World War II</a></li>
                <li><a href="#legacy">Legacy & Analysis</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <video autoplay muted loop class="background-video">
            <source src="hitler.mp4.mp4" type="video/mp4"> <!-- Replace with a relevant video -->
            Your browser does not support the video tag.
        </video>
        <div class="overlay"></div>
        <div class="hero-content">
            <h1>I,Adolf Hitler: An Ultimate-Killing Machine</h1>
            <p class="tagline"> He alone, who owns the youth, gains the future.</p>
            <p class="tagline" style="color:red" font-style="bold"> I Killed 6 million Jews and I am proud of it.</p>
        </div>
    </section>

    <section id="early-life" class="content-section">
        <div class="transparent-container">
            <h2>Early Life and Influences</h2>
            <div class="content-div">
                <img src="https://media.gettyimages.com/id/517391954/photo/german-dictator-adolf-hitler-in-military-uniform.jpg?s=612x612&w=0&k=20&c=Ftfn0cb1QUM1QveYEPrD7UTmFeChoIybkMWlwcrIXco=" alt="Adolf Hitler Early Life" class="section-image">
<p>
    <ul>
        <li><strong>Born:</strong> April 20, 1889, in <strong>Braunau am Inn, Austria-Hungary</strong>.</li>
        <li><strong>Father:</strong> <strong>Alois Hitler</strong> – a strict customs official.</li>
        <li><strong>Mother:</strong> <strong>Klara Hitler</strong> – loving but overprotective.</li>
        <li><strong>Childhood Interest:</strong> <strong>Art and architecture</strong>, but his father wanted him to pursue civil service.</li>
        <li><strong>Father’s Death (1903):</strong> Led to him dropping out of school.</li>
        <li><strong>Move to Vienna (1907):</strong> Hoped to become a painter.</li>
        <li><strong>Art Academy Rejections:</strong> <strong>Twice rejected by the Academy of Fine Arts Vienna</strong>.</li>
        <li><strong>Struggled with Poverty:</strong> Lived in shelters and developed his political ideology.</li>
        <li><strong>Influence of Vienna:</strong> Exposure to nationalist and anti-Semitic ideas.</li>
        <li><strong>Military Aspirations:</strong> Applied to join the Austrian Army but was deemed unfit for service.</li>
        <li><strong>Impact of Early Life:</strong> Shaped his <strong>extreme nationalist and anti-Semitic views</strong>, influencing his rise in <strong>German politics</strong>.</li>
    </ul>
    
    

</p>
            </div>
            </div>
    </section>

    <section id="rise-to-power" class="content-section">
        <div class="transparent-container">
            <h2>The Rise to Power</h2>
            <div class="content-div">
                <p>
                    <ul>
                        <li><strong>Joined German Workers' Party (1919):</strong> Became a member of the small nationalist group, later renamed the Nazi Party.</li>
                       
                        <li><strong>Beer Hall Putsch (1923):</strong> Failed coup attempt to overthrow the Weimar government; resulted in his arrest.</li>
                        <li><strong>Wrote Mein Kampf (1924):</strong> Outlined his ideology and future plans while in prison.</li>
                        
                      
                        <li><strong>Hitler Becomes Führer (August 1934):</strong> After Hindenburg’s death, Hitler merged the roles of Chancellor and President, becoming Germany’s absolute ruler.</li>
                    </ul>
                    
                    
                </p>
                <img src="https://media.gettyimages.com/id/119505258/photo/adolf-hitler-in-munich-in-the-spring-of-1932.jpg?s=612x612&w=0&k=20&c=SPyMava8n_tHW4Dm5ygM1GNYZwjC-gv4tEejHV_1GrQ=" alt="Hitler Rise to Power" class="section-image">
            </div>
        </div>
    </section>

    <section id="world-war-ii" class="content-section">
        <div class="transparent-container">
            <h2>World War II and the Holocaust</h2>
            <div class="content-div">
                <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxMSEhUTExMWFhUXGB0YGBgYGB0XHxgfGBgXFhoXGBsaHSggGBolHRcXITEhJSkrLi4uFx8zODMtNygtLisBCgoKBQUFDgUFDisZExkrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrKysrK//AABEIAMsA+AMBIgACEQEDEQH/xAAbAAABBQEBAAAAAAAAAAAAAAAFAAIDBAYBB//EAEUQAAECAwUEBgcFBgUFAQAAAAECEQADIQQFEjFBBlFhcRMigZGxwSMyQqGy0fAHFGJygiQzUnPC4RVDY5LxFjRTg6Il/8QAFAEBAAAAAAAAAAAAAAAAAAAAAP/EABQRAQAAAAAAAAAAAAAAAAAAAAD/2gAMAwEAAhEDEQA/APH5hDBic8j8/wC0bv7OC8icP9UfAP7R5+Y3/wBmpeXNGgmD3oHygA+3qD95B/00/EuMyRGq+0EAWlLgv0QqD+Jehz90ZvPcrx7tex4CuRHHiQpHLgYapMBwQ4GGR2AkCoI2O9piKPiTuJ8DpAt46DAbKTeqJzVZTNhOeppvqTHLVZkrDKAP1odIx+KCNjvdaKK6ydxzHIwHbXdCk1RUbjmPnFZNnGp7BB+z2xEz1TXcaH+8R2qzg5iu/WAFS7KVKSkJoogOx11f3wcs9gly5qgC6UtUnz3fOK8oqokmiU00qGHg8S3ZaEhC8RBqTWtX46VgDG0lmlqkKW7KQlx/Y8fOMGGEFNorblJQt0J0DEBqZ58WfdAQQFjp90MM4xFEsuWDUqA957oDnOOph7pGQJ5/IfOHiarSg7oBCQrWnP5Zw7CkZl+VP7xHnq/KJEp4DtgIpqxoIjeHz884heAkeLN3qaYnnFSJJVCDxEBrVLcAvlqI90udjZpZGqE+DeMeBWad1T4Ru7g2qUiQElLjNLH1WYBoAZ9otpKbwJHsol+5zCgRt9a8d4FWWOTKU3NDwoDDKTSN59mymlTj/qD4BGGmikbj7Of3U7+YPgEBQ+0lD2lH8lPxrjJKSRGu21kCZa0V/wApI7lLih/hKQOqrs39kAB6XQ1517jmOyECNC3Oo/t74uWu7ykYmo7FtCzjPQ17jFXofrLxz7IBpTw7R9UhrROJLVeHdCQQohgWYtnAdTd0whwl4rFJFCI110qVuOFhWtA7YsmZ+MUNobOnpuqRxIyOXzgADRx4v/cxr4wvuyAaj3wFDHF+y3wpNF9Ye8duvbDgJIzbxhqp8oD1A/IUgCtntCJnqns17o7PlHCQk4X4a7+Bijd8hKz6oDh6BiORGURyr1KFFKhiSCQ+tC3bAUjZFAsr/mLH3NPHvgslaJgdBcajUcxEEyS0AHtFmUkgMesHTxERFLUILxsLHZHT0imKyABpkKJG4MIGbShCsJT+8TRTJIy1PaIANLJfLuDtDisf8wQu+VhKikuBqaPR4ZtBNClpZLEDczh6HxgKRtG4QxU0w0Q7BAIqDZV3kw2ERCEB0Q9AhkPQpqwGms8glmGbHdn4RcQlSE4Hy3HthtmHVT+UeAhLWACS7QA3aq04pyFe0mVLTzwpYGFFbaMem/Qj4RCgB9ps6kYQr2khY5Kdu2hja/Z5SRN4zP6Exy8tkjNUFJmgYUJQAQ9EBg5GsW9nLCuyylomFJJmYgzkNhSndwgAO2az95Th/wDGPiXENhKiQCQN5iHblT2lPGWPiVFb7rgm9GF9IEgElOTkO2en0IDU3rYJIsqkCa5WoKK8wMOVNz0/VGOsViXMWEAjJycwkDM8cwANSRBO02gqSwoAWYanR98EbmT0WFZzUpajx6JBwDliUVc2gCFiuaSAhKkAhRUCTUjCFMX3kjSmUAdo7IqVhlmqQeorgfZVxFGzjXWaQ8qUh+sEpL7lNiHvYxU2hl9LLQSBhWgFmyUAXAOjVDcOEADsM8GVgbreq/8ADxO+KF9FSUIIB6pKVHNj1W5P5NEMlRlTCMQIG/PgC0GlykqkpChmgin4i5PMlu6AyKrQo6/XZE932UzVhJdjmeEaS27LygglAU4SSOtmw4xXuWzgzzLVTCEoBFfVAr2ivbAT27YeYEdJKOIZ4SQCO/OMlNllJKSGILEco9NNumdCyCCkKUBicqZyAAQ2TR51auutan9o8dcxAF7jzH5fIQEto9Iv86viMHblR1wPwt7hDb4uoYFTUmoJxDtr28IAAhZBcEg7xBOz3rpMH6h5j5QLAjuGA0yZgwgoUM8weeYyiIqoQzPn5wClTSkukt9axekXiD61Dv0gEimJSaoo4y1HfFWcorViOfypFyah0kJLO3bA7AXYwD2SNY6Zg0EOnWVSPWSQ+VM+UMTKJ0gGKLxwQ4ph8qQpXqgnWlYBgiRAEXpdxWhUtU0SlFCcy2XGKKIDaSEjAn8qfCOhOf1vjsgejR+VPgI4g1+jAZzaE+m/Sj4RChX6PTF9yfhEKA9ETM0hnRrORjzyz7T2pJ9cL/MkH3hjGsue+rTMRj6CWpL+yogumuRp74AouS4wrQlQrRQ+YgdMuWz1wy+jJoSinuy90TS9ppCqTcUpWbLBp2s0SC3S5lUzEqfcRACZuz49hb1eo7Mx8oitlhnNKCUvhUSWI1SQM6mrQbIhpX2wEX+NIlJ6wUVqWwSBlhIYl97UHLnEtokrtEtMuUCVM9SE1WVKwk1avbDemBoRTdnDpC0IVjSwVkcwCBkCAwI4QAqZdKpMxS5iOjUliKg+qK8yS7hi7iKovGWZoWmWpctPsg4SCwLpSfWALhiQY01631MnAhWFyDUDfrnGPs92TJbgYVj/AGmA1RnJKApBcZVDEPRiDUHSMeT0U4kAqSSAQk9YH1eqNcosrmNmFJL+0KcQ4pF2xCVLSZq0cVH1h2QDL0lTJlnmGWopwdYo9opDhVQc+qeeE8Iy92CpG8RrLjtLrXgSVJUo4QTXCUgFLHOoi8di12SzLmzkCUVraXjwzMKNMVPXICywI0fdAZ+6B1y/8JEOvOcF9WoAzDsCQTU747ZlDpVFPqkEjgHYPuNIBWyarpF0frHfv5wF0ypQ0HfDcMncDyDwOxrHDkBDzLWzqUWOrkwFtXRfwDw8YjmrktRIfmfIxHLsSdVHsA8zFlNhlgEst9HI8hAQK6iCRvAzpXhHZM4K5/WUNtB9H+ryMU4Aza5pUE7ub8OyKxBitLtRFDURZQoHL6+nMBBMRWNX9n94CRNJMsryLJqTnlvjNLl7vCC1wXqZExJUHThw6ZYirxUawHrl4XwqYhKJMkqCxUlk4XdLFJzLgvHj+0N0qs8xOIg9IkroMuspBSeLp98bmTf02TJUXlEF+p7ScSiQAR63rajIR53bbUuaslZJagfQOS3eTAaKx2hK0AJIJShIU2hZm9xiaXK+ucDdmk/vOSf6oNSE0Vwb3v8AKAzF/I9OrkPhEKHX+fTHkn4RCgAINd3LjSN9sGkfd1mj9IfhRGAl6xvthv8AtlfzFfCiAz+2Sz95O4JDdrvAQKgxtkprSR+BPnAPFAW5VumJ9WYociYuSr/nj28XMA/3gTijmKA0MvaVXtIB4hx84to2hkkVC0niAR7i8ZN4WKA2sq8pKspie2njFhKnyII4VjBY4SZjZU5QG9MQzZKVZgGMjLvOanKYrtL+LxZRf00Z4TzDeEBqbrWLOoKlgBtDUe+NXeG3cydLCVIZhvcHjUR5pL2hHtIPYX8Wiyi+pR1I5g+UBacu5FSVE9qnhirtKUqmM6TUqAyepB+tIai1oVktJ7fKHdKpJdKiniNeBGRHAwAhElGN1CmEsBodPc8FUSxgqHSQ5O4DWIZKEpPqOCXYFmfMJ0T3MIkvEoUhXRlaHNEMCADpjdz3CAEC1y05FRAypD/8UBBABqGrxppFYXconQczEyLomZunqjFrkKnSARScIYOXy7IrrnkUKW4QUu1sQcs1XOVGz4RDfHpFA9UFIqR7XHlTWAGdL+ERYlAEEsBQ5corLRucxesKApSUaqIT3lvOA1Oz+w1qtMoTVYJaSHTicqU+uECnaYtL2EmJBKpiaFsITxbN+MeoLtqZCJaHGIgJSOyLlnszh/aNXgMVsxsamUoKmlSyKpCqJH4m31jlt+zCQtRVLmTEPUgEKSCdzh/fG7wgKc5s3KLCcoDzj/oA2aWtcubjoCUqSE5OaEE74Ay2KSDkSAakZvqC47DHp942pEyzzVJLjCoE8UuCO8ER5jY8ldndUeYgMxtD+/UPwp+EQoftIj9oVyT8IMKAzcqN9sMf2ZX80/CmMDLEb7YlP7Ko/wCqfhS8BnNtv+6/Qn+qAMHtth+0/wDrT4qgDAKFChQChQoUAoUKFAKFChQCiSWsA1Ti4O3hEcKAP3ehKmVgSl05AP7yT3wKtE4pmKwlg5oMu6C90nqJ/KYCW394v8xgJ5d5rGbH64ROi8xqkjlWBcPlyn4c+bQBYWpJdleUSptKgCHoQRvzoYVkuJNemUUgD1hl4E6wKUlIWUpUpnYEDPTeIC8Ejc/a3hDgupKqk0Pz49sVpyihLuSXasRJtm8d0BNa1goSAC6SatmPpom2dkldpkpGZmJ8XJ7gYq9Mk/3G+NJ9n9j6S2II9kE+XgTAeg7YWnDOsiR62JSuLABNP9xjYXXaHQkkMd0ea7Q2zpL1SnMSpQDcXxK7WI7o9HuebiSDwo9DXfAPK/SEvSO220kS10IZ69mcKQQVq4+UBtt7d0dlnEZ4CAeJoG74CrdysV1BSdZajzckxj7vmJBL7qccqfW6NPcE/wD/ACUAaST5xlLFMAfLJ/flABNqpY+8q/Kj4EwoZtCf2g8kj/4TCgAl42RErClL4jUuXppGr2MX+zKAd+lPwojH3jaMc1RGQ6o5Cni8azYxXoFfzD8KYARtfKBtNSfUTpxVFWx3agjrEngKQS2qllU+gfqDLmqKljkK3F4Cb/BpRYMoE5V+YiK1bMqYlCgeBo/DODaJCgAohsVATwZ27xFtSwBQkNugPPplkWkOUkdz9ozEQxpb6s+E48eFJILs+oJDb8205QMtiZSy8pCkhzVSqq4lIonsgBsKJ+hBoD35Ram3FaEljKPYpJ8FQA6FE06yLQWUkpPHXlvgpdezU6ckTKJQcRfNRwZ4U6ntEAFhR6QjYiQFSZcqYJhmUUtZSGoSoplkPQDR33iB22WyEuwpQpMwrxH1SACAPacNTTLWAEXX6ieR84oWuxKxKXQh3oXI5iLlkWPZyYt3RtdmEScBC0pqHJZzAYm5LJLXMSJhwo1oS7aUyj0K+NhrNOspmWbqTUpxAhSiFMHwqSolnGtDlnGStcqXLnzUuGSoBGVAQKcnPui3ab+nSULSCwWgoGb1DOa+sK148YDPot8xSCEF3A9bRqdXvihNu6ahlKTQn1sxvzi3ZcyOEX7ynqEpKcYIJIyYlmyajQAa2nqjn5RRi9aUOkNvinMlkFjAceN99kCgLRM3lAHcTGBKY1f2d2sSrWmtFDwI/vAW76xC95orVQy/lpr3iPULntSiCDmB30gLPudJts6eRVeEJPAJDt2+EGJQIHVLFSgOx6+4QBEzClLjPOPPPtKvVasEjVZxEZ5Hqjv8I9NYNGD2zuETLXZZicyrCocEusK73HaIAgtP3a7gn8ASB2M/iYxUldfd5xodu7wBUiQk+qMR8B590ZiWeNX784ChfyvTHkn4QYUU78memP5U/CIUBUvqzdHNyYKSCOwMfD3xotjlehX+f+lMCL7taZktOEuyvIwU2NPopn5/6RANv2xTpk0qlpUUpQCogFhVWZi5stKUDiUjEBmDruEK+L5XZqCSCFBkzCT1SxCktkXB18oqXbekwBJC2HN/+IA5t1aHlypicKVg4EywR1Qr2gAanqudKjtH2ecCEuioGEH+I7vEmOKR06xiq1cRzpQARFMW1oD+qlLDhicP7oANtYg9IknLDTm5flp7oEpLikFb7scyZMKiAnESwOg3khwavEFnuSYT6yQN9T7mgKSU5Zvr2RuLlscqZKRjScRA61c2pzcQDsWzWJQT0hU7hkgAmhpVXCNQm9CE9HMlmgw4sPVLBusw6pcQAy9rrVgeUzlTAEUo7liCUl6RSuO+plmWELb0anrxzbx7Y0ibwGGbMbqnD1D7SmAKhR8mG4t34y9Fy507IBWE0DsWyCqgvXRucBvrzviXMmybShQISxAoMOFnamoBDfiMAtu77+8FABolJpxJr4CDOzV0JtKMH3RCnf1SUsC2RJJGtXesQbT7BJkoVMV0spA/EiZh3skspW9sW+uQgMHd5Zu3zjSpt6Ey0hPVm4QAoFiTQKFaOw98ZmwaNUVY786tpBOzXgEOAApXEsffAV7NYp6lErBAUXUokV3lyfGJFXcCFEzgV6aimhIpDLdalzGKqjRIISB4uYM7K3lIlTgZ8tSperFyKaUZVeVIDPWbFuIPdFlVkChiWogpBICRmwdy4Yd+kF9pL/k2qYjo5BlYXBJbrB9WUXMFbTfN3pkdGiWlSlS2UooJIUxyLPAYNc1k86RVWp+srNqQRsigl3OjAs/bWB6kkk1o5zgHrtTJIIzFOFXeLFzTsE+WrIAse0N5wrstnQqxBKSXBqkFmOj0iGVKxKJFPWV4lvKA9hTeINmxLJ6rVrXQimWleEPu7aGSqmJq6iAF2TlJTgUGSSxfj1fFh+ob4CWVeBajUJBIFQCwLZb+EB6uq80YCQoU1eM9eF69fpD6oSwJocqq4RmrFakrLBXF2bFSjk1ArXIbhDr4UqZLMs0KuqFabzTtrz3wAD7+Z9pnTHoaJ5Asn3V7YsSZjO4y13wKu2UpEyYhQYgMe8fOCQyrkGgA99reaTvSn4RCht+H0p5J8IUBLfNgly0pKEqBJq5cZGn0BBbY1XUmD8QPuhv+GpXRRUz5OPlBC7LKiS4SCys3O7dSAgvWcszkoDYSAa6ly1dI1ux0hExYEysAJxSv1kpJDB2r7oZiCcg3KkB7ii4bNhfokEb2BjzLb67JCJzowsQxA8xGcNsWQ2NX+4/OIFl+cBXtVm9UJJYb6twD9ndB255siSqUshBCSTMSuX0hWKMElSmRroc4DqVDCYD0O+tvJC0ITKlTpZSoF0iUlwmpRUlknlGCt9r6WYVpKpQJqHxd9IqqVDFLbNhzgJ1TVgOF4g+oT7qcIrT7QpbFRcDRh4s/dEU63ywGxpzfNzruiou85e8nkD5wGkuzau0WdWOVgB3FLjuceMdvfbi3WgYZgs+E6hCwez0hjKG9hoknuEV1XsTkkd7wF4hsqQlgipxB8iQQ/I6xdui71TwlSDjUE4lJAoCT1UNqQkOa+1wjd3XapEyT0U9ISsgjAWc4faQd3yO6A80UqK8yYneO+Ir7solT5iEnEkGh4GsUYC8bQnfDPvI4xVAiQySGJ+qwFiZMIDtrvir0pixa8u2KrQHcZgncBBmEK1SR3kQLaL9yFpo5eYgNYmasOFDFUa0UMIQtJ/hxAJU+9HGIShiVYmSosSdCwAJ3OPfzi3MWK7gPeqn1zgBe1rWEIQC2NirjQOOFWgCPRgBJqxO/ia+EX7xkFASsKDjCGNAQpgANEkE9r1gdPPopJb+DygteuGdI6pDgAsTqkE+NYARbE4pnSMxbAsbik0PEEeEcH19dsQptuNRRSgckCqjQV3tFiWHfl5iAA3z+8/SIUK+/3n6RCgGi+52ih/tEGbltJmIUZilE4iAxwt1QfZ7Yy2KNFsspxMSQ4oe8EeUAYTNASCogUDknhEE685IzmJ7C/hAXaiQlKpeFIDgmgbdAWA1Ey/ZIyxHkPm0VZm0I9lB7SB4PBDZPZFFpPpJuH8I8z8o2Cfszlj/NSw/DU86wHm0y/phySkd5iCZe04+03IDzgze+zP7UuXJIEsEdZWQLVA+tYz4kdYpxJoSxNAW8H4wBm7LtmTqrWs8ASO8xavLZunUFe0vwrnHdlL2MosSWPMxuk3tJKOlp/DQEl/ytnxgPG1BixzFIIXZc06eCpKDgGazRI7dTwFY1dm2clmZ002uNRWxoEg1Y8YN2q1krQlIwy0GgFAk4XBbfWA5s7shY5aQuaenVmxHVH6de3uihtzZZEyUFiWETADhwgJZIBPWbRoPSZqUKSfZUluRAyPOBl9WQzEgBQGhficj7oDI7M20oSoBWDF1XbFmP/k8Y0FrvGRNlJcgTEpdS/VShqZPlQMMycs4H3dsLNUrrzUy0E0brqUOQ6o7Vdkc222WNlMoJJMhQodcdXCiMy2XMwGROKYompJOZ84u2axgVNfCIvuI3mHiyNlMI+ucBc6FOgA7GhlpkpZs2DjhESbKv/wAneH84fOkLYnGDStICsJeIZ5V3xFa7OZZD6xYs6yMs+bQ22B1EqIcaCvygKJMWrqWRNS31SIAiJrKAFp5wGvWCqVTMpftzHhGctkwlaAcgEmvfGnkE4ByjL35KwzQRuB95+QgDS1PKTwb3M3hAM21aVqwqZlq0GpLjiKmnGClhnAygOTBoB2ikxdT6x8TAXbnV1zvI8xBsKasArnbGeXmIMEwAO/D6T9I84UK/E+kH5B5woAbB7ZY9aYOA8TAGDezB66/y+cA7anOWeCh4RAq72kSJo/zCuu4pVhw8KV7Y9M2UskiZJnifLRMDoYLAIBIWnEH1rHlZs+BakgkpSosXzYs/MgCA3GzV0T1IQuVNwu5d2CWB6tBVyAHfWNfaptsmIklCgkKS6zQv3pPDdnGC2WvYolzZRU3VOGhIBO9qtGjva/jKu4YVDpEpCeriKf4aKUA5cjlAAdprWbOpSAXUpAWrRivEH5U8IwxG6JZ1sXMWpcxZUtWaiXJ07mo0dQl4C5ckwYsKgCN6g+XONFZZiFpIATSYXoKAAVIIpqab4zVikOoZduXgfCDSrWiShqYiWOFLDllAbq9ZyFyErCWFA3CAoCj1gKhtcxQfKLUidjkAHIo8hX3xVsZxOkKDsAQOthqWdqCogLmEECu7i2sT45YBUvCKMrEzKHF9YHzkiiFrHWDOksaEetXjnAa+AZZxHCpIyL4j4dXsgLVqvsIwqlHqD1XBA/TvgpPv/wC+SUhaAEpNHripm26ucYO3TjNUkEkAZAQZue9ZSR0cySV4QziYUeA9zwCnoTKUDTWm58s89R2xOhUtSkhVUNicka8BnVoFXtMllboBSP4cRUPGvbFG0TypRIGEbhlzgJbRaBjWEAFIUQC7U7ojNqJDYQO1/KIGAfSIkzqgJDnuEBOhDOIqLmVpWLyUhlBRBJHdyiEAJoICvgUdIdZ5RCkniPGLUm0gUJMcVO7eMBp5B6sA79S8z9I8zBmxzOrAK/Fel5pHiRAFNnbrmKlmYstLALBw54jUNn2RmgI3N2zsFjO4AxgkiAI3aOt2eYgmdKwGsB63ZSCaFu3PyMAOvMdfs8zCjt5nr9nmYUAOaC+zR9Ir8vmIEwU2ePpD+Q+KYDf7OSBMROBy6tOPWYnlGDt8ro5i0HQtGtuW2pl9IFEgKAYs+T5tGetxC50whTgknEzBtTXKAs7P3YVkrfC1AC/WJyTQgjUu9Gh+39rw4LNqGXMYk1qEJcl6Ak13iLexS+ltIH+XLT1eJOazxp3RPf1yItwM6QR0taHJYegJ0VuPZAeeRLLmtHJ0haCQpKkkFiCGY7jG/wBiLjsM0SyVKmTlIJKWIw78NWYEs9XMACui7p00gIlrGJJUkkEBQH8NOs/CnGJ78uabJXLl4C+JJUlwsh2r1eejjjHr1ktEsLB6BKWS6VBIyYBgdKUaAe1llnz1yuhShKMZJVULCmI31DFVOEAItt2kqkS5c3o1ElwCQSMLqCSxY0fTI1Edv25FWZAEpeMqUcRDgJZi61YiS51PJo1V2XYpMseoC+JVSt3ZxiIDhnEKfaZCJS0LQlAYhmCSQ1VADIQHj162e0SVBS5mIGjihBNag1A4jdFKRIExVVtmSVO1NzZncIs22fjNVFbPhJ3Pm2QJziB4DiEhJd3z7qt7oUwgl2AhnSB2FTHLXKXiCU7nLadvZAcmTAMzEQnKUWQmJJdhA9Yud0TaNQDcICsLIfaLncKxLgSKMI4tbawwr3QEoCRoIjnq1174jKoa+6AaqbHUzKUiKYmGpzpAaaxzgQztT6ygffTFYY6MfHziS5lKqkhiN+ee6Kt6oImMKklh2hPzgNHOmNYX/iDd9IyKqRqdo3RZpMsZBn9/yjLLFICzdzFXZ8oJpDQHu09fsPlBVBgKV5+sOXmYURXgXUOXmYUBTEErh/e/pPiIGpgncP739J8oAzaZJUKFu1og/wCm7RNHUIbUVA7TGt2RkpK5hKQSlIZwCzk5PBy0rLGsAD2b2bnSpExinpFyyhJcsCQQ7tlAaxXNeFhPWlFcvfLUFNyHre6NzcloUUoc6HxMEZs4qRU6tAeXX/Pk2iXiJZYo+ruzEe5orbJWqbZrTZ1snClfWYM6V4UqJYOWAB3ukQd2UsaFWi2TVJBWiVjSTVlKSp1MaPxaM7JV1YD0G2bV2VE50dLgCVJUQkHECSoAJJBdyWJIYEwBtm3FoxqMppaSQzgKIAdvwjNywz1oIzZiJfnAW5l/2vpAv7xMKgaB2FXDYUsGqcmh14X7OnIKVlCQT1sAKcX5ipRJ790C1mBK5hVmXgLsy2gZB/dEKUrmECrHcD7gKmLl2SElOIgExZWqAqS7PgUGORqCCDxEWZoJY1H9s6w8GscmqIAgIujAiKYgDfDsROsVTML5wD1qeIiYkmiIwYBNCKCIlMdI8YCBUH9nbnS4mqIO5Iqz6ni0BFmsT2a0rSMKVKABcAEip5QDr8nAz14XIcAniAxb63xTKapOuIeMPmHWFip9aZQGr2ksS1WdCsyACRwHy+cBLotslCCidI6R1hQUMOIM3VqAVJOeHGBnqXBOx2lShJxF3lqd+BBHLM98Z6VoYA3ZbTYQpGOROScK3MspBBM0KljrKZQEvEkqIeooWiaXbrIer92IV0CgpRmFXpWVgWhsLB8BL/iATvFy0gioiOWgOaQFi8RJVLCZctQmdI7moCMLYMTuo4mPqpArnnCiFKQATrCgP//Z" alt="World War II" class="section-image">
                <p>This section would cover World War II and the Holocaust.  **It is crucial to present this information with sensitivity, accuracy, and a focus on the victims and the historical facts of the atrocities.** This is perhaps the most critical and somber part of our examination. We will detail Hitler's role in initiating World War II and the horrific atrocities committed under his regime, most notably the Holocaust. It is imperative to approach this topic with the utmost respect for the victims, ensuring historical accuracy and providing context to the unimaginable scale of human suffering.</p>
            </div>
        </div>
    </section>

    <section id="legacy" class="content-section">
        <div class="transparent-container">
            <h2>Legacy and Historical Analysis</h2>
            <div class="content-div">
                <p>An analysis of Hitler's legacy, the long-term impacts of his actions, and historical perspectives.  Encourage critical thinking and learning from history.  In this concluding section, we reflect on the enduring legacy of Adolf Hitler and his impact on the 20th century and beyond. We will analyze the historical interpretations of his actions, the lessons learned from this dark period, and the ongoing relevance of understanding the dangers of extremism, nationalism, and hate. This section aims to foster critical thinking and encourage a deeper engagement with history to prevent similar tragedies in the future.</p>
                <img src="data:image/jpeg;base64,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" alt="Historical Legacy" class="section-image">
            </div>
        </div>
    </section>

    <footer>
        <p>©  Copyright By Adolf Hitler </p>
        <p>Don't Copy Otherwise Your Will be in Gas Chamber</p>
    </footer>

    <script>
        // Fade in content sections on scroll
        const sections = document.querySelectorAll('.content-section');

        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                    observer.unobserve(entry.target); // Stop observing after animating once
                }
            });
        }, {
            threshold: 0.15
        });

        sections.forEach(section => {
            observer.observe(section);
        });
    </script>

</body>
</html>
