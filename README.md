# Final-monte
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Equipment & Costs | Beekeeping for Beginners</title>
    <meta name="description" content="Detailed breakdown of essential beekeeping equipment, tools, and estimated starting costs.">
    
    <style>
        /* Accessibility & Global Resets */
        :root {
            --color-primary: #FFB703; /* Honey Gold */
            --color-secondary: #023047; /* Dark Blue */
            --color-text: #333;
            --font-stack: 'Helvetica Neue', Helvetica, Arial, sans-serif;
        }

        /* Base Typography for Readability */
        body {
            font-family: var(--font-stack);
            line-height: 1.6;
            color: var(--color-text);
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        h1, h2, h3 {
            color: var(--color-secondary);
            margin-top: 1.5em;
        }

        main {
            padding: 20px 5%;
        }

        /* --- FLEXBOX for Navigation --- */

        .main-header {
            background-color: #fff;
            border-bottom: 3px solid var(--color-primary);
            padding: 10px 5%;
            /* 1. Enable Flexbox */
            display: flex; 
            /* 2. Space elements between logo and nav */
            justify-content: space-between; 
            /* 3. Vertically align items */
            align-items: center; 
        }

        .main-nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            /* Enable Flexbox for horizontal list */
            display: flex; 
            gap: 20px; /* Space between links */
        }

        .main-nav a {
            text-decoration: none;
            color: var(--color-secondary);
            font-weight: bold;
            padding: 5px 10px;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--color-primary);
            color: var(--color-secondary);
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            margin-top: 20px;
        }

        /* --- COMPLEX TABLE STYLING --- */

        .equipment-list {
            padding: 20px 0;
        }

        .styled-table {
            width: 100%;
            margin: 20px auto;
            border-collapse: collapse; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            caption-side: bottom; /* Optional: Accessibility for table captions */
        }

        .styled-table th, .styled-table td {
            padding: 12px 15px;
            border: 1px solid #ddd;
            text-align: left;
        }

        /* Styling the header */
        .styled-table thead th {
            background-color: var(--color-secondary);
            color: white;
            font-weight: bold;
            letter-spacing: 0.5px;
        }

        /* Striping rows for readability */
        .styled-table tbody tr:nth-child(even) {
            background-color: #f2f2f2;
        }

        .category-header {
            font-weight: bold;
            background-color: #ffe8a8; /* Lighter honey tone */
            color: var(--color-secondary);
            vertical-align: top;
        }

        /* Styling the footer */
        .styled-table tfoot td {
            background-color: #e0e0e0;
            font-weight: bold;
        }

        /* --- IMAGE STYLING --- */
        .equipment-image {
            width: 100%;
            max-width: 300px;
            height: auto;
            display: block;
            border-radius: 8px;
            margin-bottom: 10px;
        }
        
        /* --- CSS GRID for Content Layout --- */
        .equipment-gallery {
            display: grid;
            /* Creates 3 equal columns for displaying equipment items */
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .equipment-item {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            text-align: center;
        }
        
        .equipment-item figcaption {
            font-style: italic;
            font-size: 0.9em;
            color: #666;
        }
        
    </style>
</head>
<body>

    <header class="main-header">
        <div class="logo">
            <h1>BeeBeginner</h1>
        </div>
        <nav class="main-nav">
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="getting_started.html">Getting Started</a></li>
                <li><a href="equipment.html">Equipment & Costs</a></li>
                <li><a href="calendar.html">Bee Calendar</a></li>
                <li><a href="resources.html">Resources</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <h2>Essential Beekeeping Equipment and Estimated Costs</h2>
        
        <section class="equipment-list">
            
            <table class="styled-table">
                <thead>
                    <tr>
                        <th scope="col">Category</th>
                        <th scope="col">Item</th>
                        <th scope="col">Purpose</th>
                        <th scope="col" colspan="2">Estimated Cost Range (USD)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td rowspan="3" class="category-header">Hive Components</td>
                        <td>Complete Hive Kit (Langstroth)</td>
                        <td>Housing the colony; includes boxes, frames, and foundation.</td>
                        <td>$150</td>
                        <td>$250</td>
                    </tr>
                    <tr>
                        <td>Bottom Board & Cover</td>
                        <td>Base and roof for protection.</td>
                        <td>$30</td>
                        <td>$60</td>
                    </tr>
                    <tr>
                        <td>Frames & Foundation (10-pack)</td>
                        <td>Where the bees build comb for honey and brood.</td>
                        <td>$25</td>
                        <td>$40</td>
                    </tr>
                    <tr>
                        <td rowspan="2" class="category-header">Safety & Tools</td>
                        <td>Full Bee Suit & Veil</td>
                        <td>Personal protection from stings.</td>
                        <td>$70</td>
                        <td>$150</td>
                    </tr>
                    <tr>
                        <td>Smoker & Fuel</td>
                        <td>Calms the bees for inspection.</td>
                        <td>$40</td>
                        <td>$80</td>
                    </tr>
                </tbody>
                <tfoot>
                    <tr>
                        <td colspan="3"><strong>Total Initial Investment (Estimate)</strong></td>
                        <td>$315</td>
                        <td>$580</td>
                    </tr>
                </tfoot>
                <caption>Detailed breakdown of first-year, minimum equipment costs.</caption>
            </table>
        </section>

        <section class="equipment-gallery">
            <h3>Visual Guide to Essential Gear (using CSS Grid)</h3>
            
            <div class="equipment-item">
                <figure>
                    <img src="images/bee_suit_placeholder.jpg" alt="A white full-body beekeeping suit with a zippered veil." class="equipment-image">
                    <figcaption>Protective Suit and Veil</figcaption>
                </figure>
                <a href="#" class="cta-button">View Suppliers</a>
            </div>
            
            <div class="equipment-item">
                <figure>
                    <img src="images/smoker_placeholder.jpg" alt="A stainless steel cylindrical bee smoker with leather bellows." class="equipment-image">
                    <figcaption>Smoker and Smoker Fuel</figcaption>
                </figure>
                <a href="#" class="cta-button">View Suppliers</a>
            </div>
            
            <div class="equipment-item">
                <figure>
                    <img src="images/hive_tool_placeholder.jpg" alt="A metal, multi-purpose J-hook hive tool used to pry frames apart." class="equipment-image">
                    <figcaption>Hive Tool (The Beekeeper's Hand)</figcaption>
                </figure>
                <a href="#" class="cta-button">View Suppliers</a>
            </div>
            
            </section>
        
    </main>

    <footer class="site-footer">
        <p>&copy; 2025 BeeBeginner. All rights reserved.</p>
        <p>
            <a href="https://www.beekeeping.com" target="_blank">External Beekeeping Resources</a>
        </p>
    </footer>

</body>
</html>
