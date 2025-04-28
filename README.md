<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Services & Expertise</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" integrity="sha512-9usAa10IRO0HhonpyAIVpjrylPvoDwiPUiKdWk5t3PyolY1cOd4DSE0Ga+ri4AuTroPR5aQvXU9xC6qOPnzFeg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #e0f7fa, #b2ebf2); /* Subtle gradient background */
            margin: 0;
            padding: 60px 20px; /* Increased padding */
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            color: #333;
            line-height: 1.7; /* Increased line height */
            box-sizing: border-box;
        }

        .main-header {
            font-size: 3em; /* Slightly larger */
            color: #004d40; /* Dark teal */
            margin-bottom: 50px; /* Increased margin */
            text-align: center;
            font-weight: 700;
            letter-spacing: 1.5px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1); /* More prominent shadow */
        }

        .services-container {
            display: grid;
            /* Arrange in 5 columns on large screens, adjust dynamically */
            grid-template-columns: repeat(5, minmax(150px, 1fr));
            gap: 20px; /* Adjusted gap for more columns */
            width: 100%; /* Use full width up to max-width */
            max-width: 1400px; /* Increased max-width to accommodate more columns */
        }

        .service-item {
            background-color: #ffffff;
            border-radius: 15px; /* More rounded corners */
            box-shadow: 3px 3px 5px rgba(0, 0, 0, 0.2), /* Layered box shadow */
                        6px 6px 10px rgba(0, 0, 0, 0.15);
            padding: 20px; /* Adjusted padding for more columns */
            /* Smooth transitions for hover effects */
            transition: transform 0.4s ease-in-out, box-shadow 0.4s ease-in-out, background-color 0.3s ease, scale 0.3s ease-in-out;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            border: none; /* Remove default border */
        }

        .service-item:hover {
            transform: translateY(-10px); /* Slightly less lift */
            box-shadow: 0 10px 22px rgba(0, 0, 0, 0.12); /* Slightly adjusted hover shadow */
            background-color: #e8f5e9; /* Subtle green tint on hover */
            scale: 1.05; /* Added scale on hover for zoom effect */
        }

        .service-icon {
            font-size: 2.5em; /* Slightly smaller icons */
            color: #00796b; /* Medium teal */
            margin-bottom: 15px; /* Adjusted margin */
            display: flex;
            justify-content: center;
            align-items: center;
            width: 50px; /* Smaller circle */
            height: 50px; /* Smaller circle */
            border-radius: 50%;
            background-color: #b2dfdb; /* Lighter teal background for icon */
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1); /* Adjusted icon shadow */
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        .service-item:hover .service-icon {
            color: #ffffff; /* White icon on hover */
            background-color: #004d40; /* Dark teal background on hover */
        }


        .service-title {
            font-size: 1.2em; /* Smaller title */
            color: #263238; /* Very dark gray */
            margin-bottom: 10px; /* Adjusted margin */
            font-weight: 600;
        }

        .service-description {
            font-size: 0.9em; /* Slightly smaller description text */
            color: #546e7a; /* Medium gray */
            line-height: 1.6; /* Slightly less line height */
        }

        /* Unique color accents for variety */
        .services-container > div:nth-child(2) .service-icon { color: #388e3c; background-color: #c8e6c9; } /* Green */
        .services-container > div:nth-child(2):hover .service-icon { color: #ffffff; background-color: #1b5e20; }

        .services-container > div:nth-child(3) .service-icon { color: #d32f2f; background-color: #ffcdd2; } /* Red */
        .services-container > div:nth-child(3):hover .service-icon { color: #ffffff; background-color: #b71c1c; }

        .services-container > div:nth-child(4) .service-icon { color: #fbc02d; background-color: #fff9c4; } /* Yellow */
        .services-container > div:nth-child(4):hover .service-icon { color: #ffffff; background-color: #f57f17; }

        .services-container > div:nth-child(5) .service-icon { color: #673ab7; background-color: #d1c4e9; } /* Deep Purple */
        .services-container > div:nth-child(5):hover .service-icon { color: #ffffff; background-color: #4527a0; }

        .services-container > div:nth-child(6) .service-icon { color: #0097a7; background-color: #b2ebf2; } /* Cyan */
        .services-container > div:nth-child(6):hover .service-icon { color: #ffffff; background-color: #006064; }

        .services-container > div:nth-child(7) .service-icon { color: #f57c00; background-color: #ffe0b2; } /* Orange */
        .services-container > div:nth-child(7):hover .service-icon { color: #ffffff; background-color: #e65100; }

        .services-container > div:nth-child(8) .service-icon { color: #546e7a; background-color: #cfd8dc; } /* Blue Gray */
        .services-container > div:nth-child(8):hover .service-icon { color: #ffffff; background-color: #37474f; }

        .services-container > div:nth-child(9) .service-icon { color: #c2185b; background-color: #f8bbd0; } /* Pink */
        .services-container > div:nth-child(9):hover .service-icon { color: #ffffff; background-color: #880e4f; }

        .services-container > div:nth-child(10) .service-icon { color: #5d4037; background-color: #d7ccc8; } /* Brown */
        .services-container > div:nth-child(10):hover .service-icon { color: #ffffff; background-color: #3e2723; }

        .services-container > div:nth-child(11) .service-icon { color: #424242; background-color: #eeeeee; } /* Gray */
        .services-container > div:nth-child(11):hover .service-icon { color: #ffffff; background-color: #212121; }

         .services-container > div:nth-child(12) .service-icon { color: #1a237e; background-color: #c5cae9; } /* Indigo */
        .services-container > div:nth-child(12):hover .service-icon { color: #ffffff; background-color: #0d47a1; }

         .services-container > div:nth-child(13) .service-icon { color: #827717; background-color: #f0f4c3; } /* Lime */
        .services-container > div:nth-child(13):hover .service-icon { color: #ffffff; background-color: #33691e; }

         .services-container > div:nth-child(14) .service-icon { color: #e91e63; background-color: #f8bbd0; } /* Pink */
        .services-container > div:nth-child(14):hover .service-icon { color: #ffffff; background-color: #c2185b; }

        .services-container > div:nth-child(15) .service-icon { color: #006064; background-color: #b2ebf2; } /* Dark Cyan */
        .services-container > div:nth-child(15):hover .service-icon { color: #ffffff; background-color: #004d40; }


        /* Responsive adjustments */
        @media (max-width: 960px) {
            .services-container {
                /* Adjust for smaller screens, auto-fit columns with min width */
                grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            }
        }

        @media (max-width: 768px) {
            .main-header {
                font-size: 2.2em;
                margin-bottom: 40px;
            }

            .services-container {
                /* Further adjust for smaller screens */
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 15px;
            }

            .service-item {
                padding: 15px;
            }

            .service-icon {
                font-size: 2em;
                width: 40px;
                height: 40px;
                margin-bottom: 10px;
            }

            .service-title {
                font-size: 1em;
                margin-bottom: 8px;
            }

            .service-description {
                font-size: 0.8em;
                line-height: 1.4;
            }
        }

        @media (max-width: 480px) {
             .main-header {
                font-size: 1.8em;
                margin-bottom: 30px;
                letter-spacing: 1px;
            }

            .services-container {
                /* Adjust for very small screens */
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            }

            .service-item {
                padding: 10px;
            }

            .service-icon {
                font-size: 1.8em;
                width: 35px;
                height: 35px;
                margin-bottom: 5px;
            }

            .service-title {
                font-size: 0.9em;
                margin-bottom: 5px;
            }

            .service-description {
                font-size: 0.75em;
            }
        }
    </style>
</head>
<body>

    <h1 class="main-header">Our Services & Expertise</h1>

    <div class="services-container">
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-video"></i></div>
            <h3 class="service-title">CCTV Surveillance</h3>
            <p class="service-description">Professional installation and maintenance of CCTV security systems.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-network-wired"></i></div>
            <h3 class="service-title">Networking</h3>
            <p class="service-description">Design, implementation, and support for robust network infrastructure.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-wrench"></i></div>
            <h3 class="service-title">Hardware Repairing</h3>
            <p class="service-description">Expert repair services for computers, laptops, and other hardware.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-code"></i></div>
            <h3 class="service-title">Web Designing</h3>
            <p class="service-description">Creative and responsive website design and development solutions.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-microchip"></i></div>
            <h3 class="service-title">Chip Level Repairing</h3>
            <p class="service-description">Advanced diagnostic and repair services at the component level.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-database"></i></div>
            <h3 class="service-title">Data Recovery</h3>
            <p class="service-description">Reliable data recovery services for various storage media.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-shield-alt"></i></div>
            <h3 class="service-title">Antivirus & Malware</h3>
            <p class="service-description">Protection against viruses, malware, and other online threats.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-laptop-code"></i></div>
            <h3 class="service-title">IT Solutions & Support</h3>
            <p class="service-description">Comprehensive support for hardware, software, networking, and IT infrastructure.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-info-circle"></i></div>
            <h3 class="service-title">Local Information Center</h3>
            <p class="service-description">Providing essential local information, community news, and resources.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-graduation-cap"></i></div>
            <h3 class="service-title">Education & Training</h3>
            <p class="service-description">Computer courses, digital literacy programs, and educational support services.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-mountain"></i></div>
            <h3 class="service-title">Tourism & Local Promotion</h3>
            <p class="service-description">Promoting local attractions and assisting visitors with information.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-chart-bar"></i></div>
            <h3 class="service-title">Business & Online Services</h3>
            <p class="service-description">Support for online presence, digital tools, and small business needs.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-wifi"></i></div>
            <h3 class="service-title">Connectivity & Internet</h3>
            <p class="service-description">Reliable internet solutions and network connectivity services.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-file-alt"></i></div>
            <h3 class="service-title">Documentation & Reporting</h3>
            <p class="service-description">Assistance with digital documentation, forms, and basic reports.</p>
        </div>
        <div class="service-item">
            <div class="service-icon"><i class="fas fa-users"></i></div>
            <h3 class="service-title">Community Engagement</h3>
            <p class="service-description">Supporting local initiatives and fostering community connections.</p>
        </div>
    </div>

</body>
</html>
