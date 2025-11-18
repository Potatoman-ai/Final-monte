# Final-monte
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Hive Guardian: A Beekeeping Guide</title>
    <meta name="description" content="A comprehensive guide for beginner and intermediate beekeepers focused on sustainable hive health, harvesting, and community resources.">
    <!-- Load Tailwind CSS for modern, responsive styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom CSS for Beekeeping Theme and Specific Layouts */
        :root {
            --color-primary: #ffc300; /* Honey Gold */
            --color-secondary: #795548; /* Beehive Brown */
            --color-text: #333333;
            --color-light: #f4f4e8; /* Wax/Cream */
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--color-text);
            background-color: var(--color-light);
            scroll-behavior: smooth; /* Smooth scrolling for internal links */
        }

        /* Accessibility: Highly visible focus state for keyboard navigation */
        a:focus, button:focus, input:focus, select:focus, textarea:focus {
            outline: 3px solid var(--color-primary);
            outline-offset: 2px;
            border-radius: 4px;
        }

        /* --- Custom Grid and Flexbox for Content Sections --- */

        /* CSS Grid: Used for the Hive Health Table Section */
        .health-grid {
            display: grid;
            grid-template-columns: 3fr 1fr;
            gap: 2rem;
        }

        /* Complex List Styling */
        .nested-list-item {
            list-style: disc;
            margin-left: 1.5rem;
            color: var(--color-secondary);
        }
        .nested-list-sub {
            list-style: circle;
            margin-left: 3rem;
        }
        .nested-list-item > span {
            font-weight: 600;
            color: var(--color-text);
        }

        /* Complex Table Styling */
        .styled-table {
            border-collapse: collapse;
            width: 100%;
            margin-top: 1.5rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
        .styled-table thead th {
            background-color: var(--color-secondary);
            color: white;
            padding: 12px 15px;
            text-align: left;
        }
        .styled-table tbody tr:nth-child(even) {
            background-color: #f3f3f3; /* Zebra striping */
        }
        .styled-table tbody tr:hover {
            background-color: #ffe08a;
            cursor: pointer;
        }
        .styled-table tbody td {
            padding: 10px 15px;
            border: 1px solid #ddd;
            vertical-align: top;
        }
        .severity-high {
            background-color: #fee2e2;
            font-weight: 700;
        }
        .table-caption {
            font-weight: bold;
            text-align: left;
            margin-bottom: 0.5rem;
            font-size: 1.125rem;
        }

        /* Responsive Breakpoint for Grid */
        @media (max-width: 1024px) {
            .health-grid {
                grid-template-columns: 1fr; /* Stack on smaller screens */
            }
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header & Main Navigation (Flexbox) -->
    <header class="bg-yellow-500 shadow-lg sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4">
                <h1 class="text-3xl font-extrabold text-amber-900 tracking-tight">
                    The Hive Guardian 🐝
                </h1>
                <!-- Navigation (Internal Links) -->
                <nav class="hidden md:flex space-x-4 font-medium" role="navigation">
                    <a href="#home" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">Home</a>
                    <a href="#getting-started" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">Getting Started</a>
                    <a href="#health-care" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">Hive Health & Care</a>
                    <a href="#harvesting" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">Honey & Harvest</a>
                    <a href="#resources" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">Resources</a>
                    <a href="#about" class="text-amber-900 hover:text-white hover:bg-amber-800 rounded-lg px-3 py-2 transition duration-150">About Us</a>
                </nav>
            </div>
        </div>
    </header>

    <main class="max-w-7xl mx-auto p-4 sm:p-6 lg:p-8">

        <!-- ========================================================================= -->
        <!-- 1. INDEX PAGE (Home) -->
        <!-- ========================================================================= -->
        <section id="home" class="bg-white p-8 rounded-xl shadow-2xl mb-12">
            <h2 class="text-4xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">Welcome to The Hive Guardian</h2>
            
            <div class="md:flex md:space-x-8 items-center">
                <div class="md:w-1/2">
                    <p class="text-lg mb-4 leading-relaxed">
                        We are dedicated to promoting **sustainable and responsible beekeeping**. Whether you're considering setting up your first hive or you're an experienced apiarist looking for advanced tips, this site is your guide. Our mission is to safeguard honey bee populations by empowering beekeepers with knowledge and community support.
                    </p>
                    <p class="text-lg mb-6 leading-relaxed">
                        Explore our comprehensive sections below to dive into everything from initial setup and seasonal care to harvesting your first batch of liquid gold.
                    </p>
                    <a href="#getting-started" class="inline-block bg-yellow-500 text-amber-900 font-bold py-3 px-6 rounded-lg shadow-lg hover:bg-yellow-600 transition duration-300">Start Your Beekeeping Journey</a>
                </div>
                
                <figure class="md:w-1/2 mt-6 md:mt-0">
                    <!-- Image, optimized and with alt text -->
                    <img src="https://toppng.com/uploads/preview/beehive-clipart-transparent-honey-bee-hive-clip-art-11562900111vlwvhtdayf.png" 
                         alt="A robust, natural-colored wooden beehive situated in a green meadow." 
                         width="200px" height="200px"
                         class="rounded-lg shadow-xl w-full h-auto object-cover border-4 border-amber-900"
                         onerror="this.src='https://placehold.co/600x400/795548/FFF?text=Beehive+Image';"
                    >
                    <figcaption class="text-sm text-center italic mt-2 text-gray-600">
                        A thriving apiary is the ultimate goal of every hive guardian.
                    </figcaption>
                </figure>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- 2. GETTING STARTED PAGE (Complex List & Simple List) -->
        <!-- ========================================================================= -->
        <section id="getting-started" class="bg-white p-8 rounded-xl shadow-lg mb-12">
            <h2 class="text-3xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">1. Getting Started: Your First Season</h2>
            
            <!-- Simple List -->
            <h3 class="text-2xl font-semibold text-amber-700 mt-6 mb-3">Essential Safety Equipment (Simple List)</h3>
            <ul class="list-disc list-inside space-y-2 mb-8 p-4 bg-yellow-50 border-l-4 border-yellow-500 rounded-r-lg">
                <li>**Bee Suit or Jacket:** Full body coverage for maximum protection.</li>
                <li>**Veil:** Mandatory protection for your face and neck.</li>
                <li>**Gloves:** Leather or heavy-duty nitrile gloves for handling frames.</li>
                <li>**Smoker:** Essential tool for calming the colony during inspections.</li>
                <li>**Hive Tool:** The beekeeper's multi-purpose lever for separating frames.</li>
            </ul>

            <!-- Complex List with Nesting -->
            <h3 class="text-2xl font-semibold text-amber-700 mt-6 mb-3">The Beekeeping Season: Year-Round Checklist (Complex List)</h3>
            <ol class="list-decimal list-inside space-y-3">
                <li class="nested-list-item"><span>Spring: Building and Expansion</span>
                    <ul class="nested-list-sub space-y-1 mt-1">
                        <li>Install your package or nuc of bees.</li>
                        <li>Feed sugar syrup until the nectar flow begins.</li>
                        <li>Regularly inspect for swarm preparations (queen cells).</li>
                    </ul>
                </li>
                <li class="nested-list-item"><span>Summer: Nectar Flow and Production</span>
                    <ul class="nested-list-sub space-y-1 mt-1">
                        <li>Add honey supers to maximize storage space.</li>
                        <li>Conduct weekly mite counts.</li>
                        <li>Avoid disturbing the hive during the peak nectar flow period.</li>
                    </ul>
                </li>
                <li class="nested-list-item"><span>Fall: Preparation for Winter</span>
                    <ul class="nested-list-sub space-y-1 mt-1">
                        <li>Remove all honey supers for harvesting.</li>
                        <li>Conduct final Varroa mite treatment.</li>
                        <li>Ensure adequate winter food stores (at least 60 lbs).</li>
                    </ul>
                </li>
                <li class="nested-list-item"><span>Winter: Survival and Planning</span>
                    <ul class="nested-list-sub space-y-1 mt-1">
                        <li>Protect the hive from wind and moisture.</li>
                        <li>Order new equipment and packages for the next spring.</li>
                        <li>Monitor for signs of starvation (use emergency feeding if necessary).</li>
                    </ul>
                </li>
            </ol>
            
            <figure class="mt-8 text-center">
                <img src="https://static.vecteezy.com/system/resources/previews/036/151/797/non_2x/beekeeper-in-suit-hat-at-beehive-with-smoker-vector.jpg" 
                     alt="A gloved hand using a stainless steel bee smoker near a hive entrance." 
                     width="200px" height="200px"
                     class="mx-auto rounded-lg shadow-md border-2 border-yellow-500"
                     onerror="this.src='https://placehold.co/400x250/ffc300/333?text=Smoker+Image+Placeholder';"
                >
                <figcaption class="text-sm italic mt-2 text-gray-600">
                    The smoker helps mask alarm pheromones, making hive inspections safer.
                </figcaption>
            </figure>
        </section>

        <!-- ========================================================================= -->
        <!-- 3. HIVE HEALTH & CARE PAGE (Complex Table & CSS Grid) -->
        <!-- ========================================================================= -->
        <section id="health-care" class="bg-white p-8 rounded-xl shadow-lg mb-12">
            <h2 class="text-3xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">2. Hive Health & Care: Pest Management</h2>

            <div class="health-grid">
                <!-- Main Content Area: Table -->
                <div class="col-span-3 lg:col-span-1">
                    <p class="mb-4">
                        Pest and disease monitoring is continuous. The **Varroa Mite ($Varroa$ $destructor$)** is the greatest threat to honeybees globally. Use this complex table to understand common issues and management techniques.
                    </p>
                    
                    <div class="table-responsive overflow-x-auto">
                        <!-- COMPLEX TABLE -->
                        <table class="styled-table text-sm">
                            <caption class="table-caption">Common Honeybee Pests and Diseases</caption>
                            <thead>
                                <tr>
                                    <th scope="col" class="w-1/5">Threat Name</th>
                                    <th scope="col" class="w-2/5">Symptoms and Life Cycle</th>
                                    <th scope="col" class="w-1/12 text-center">Severity</th>
                                    <th scope="col" class="w-1/4">Treatment and Prevention</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <th scope="row">Varroa Mites ($V.$ $destructor$)</th>
                                    <td>External parasite feeding on fat bodies. Causes **Deformed Wing Virus (DWV)**. Symptoms: Brood loss, dead/chewed pupae.</td>
                                    <td class="text-center severity-high">High</td>
                                    <td>Integrated Pest Management (IPM), Oxalic Acid Vaporization, Formic Acid Strips.</td>
                                </tr>
                                <tr>
                                    <th scope="row">Small Hive Beetle (SHB)</th>
                                    <td>Adult beetles lay eggs in the hive. Larvae tunnel through comb, causing honey to ferment and "sliming" the hive.</td>
                                    <td class="text-center">Medium</td>
                                    <td>Beetle traps, maintaining strong populations, removing damaged comb.</td>
                                </tr>
                                <tr>
                                    <th scope="row">American Foulbrood (AFB)</th>
                                    <td>Highly virulent bacteria ($Paenibacillus$ $larvae$). Larvae die in cells, forming a dark, gluey scale (ropiness test).</td>
                                    <td class="text-center severity-high">EXTREME</td>
                                    <td>**Reportable disease.** Mandatory burning of hive, bees, and equipment in many regions.</td>
                                </tr>
                                <tr>
                                    <th scope="row" rowspan="2">Fungal Diseases</th>
                                    <td colspan="3" class="font-semibold bg-gray-100">Comparing Two Fungal Issues:</td>
                                </tr>
                                <tr>
                                    <td>**Chalkbrood:** Mummified, white/gray larvae in open cells.</td>
                                    <td class="text-center">Low</td>
                                    <td>Improve ventilation; requeen with hygienic stock.</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <!-- Sidebar (Aside) -->
                <aside class="col-span-3 lg:col-span-1 p-6 bg-yellow-50 rounded-lg shadow-inner">
                    <h3 class="text-2xl font-semibold text-amber-700 mb-4">External Resources</h3>
                    <p class="mb-4">
                        Consulting experts is vital for proper diagnosis. Always check your local regulations, especially concerning AFB.
                    </p>
                    <ul class="space-y-3 list-disc list-inside">
                        <li>
                            <!-- External Link with Descriptive Text -->
                            <a href="https://www.ars.usda.gov/research/bee-research/" target="_blank" class="text-blue-600 hover:text-blue-800 font-medium underline">
                                USDA Bee Research Lab: Latest Pest Findings
                            </a>
                        </li>
                        <li>
                            <a href="https://www.epa.gov/pollinator-protection" target="_blank" class="text-blue-600 hover:text-blue-800 font-medium underline">
                                EPA Guidelines on Pesticide Use near Apiaries
                            </a>
                        </li>
                        <li>
                            <a href="#resources" class="text-blue-600 hover:text-blue-800 font-medium underline">
                                Find Your Local Beekeeping Association (Internal Link)
                            </a>
                        </li>
                    </ul>
                    <figure class="mt-6">
                        <img src="https://static.vecteezy.com/system/resources/previews/036/151/797/non_2x/beekeeper-in-suit-hat-at-beehive-with-smoker-vector.jpg" 
                             alt="A beekeeper using a small microscope to count Varroa mites." 
                             width="200px" height="200px"
                             class="rounded-lg shadow w-full h-auto"
                             onerror="this.src='https://placehold.co/300x200/a0522d/FFF?text=Mite+Count+Placeholder';"
                        >
                        <figcaption class="text-xs italic mt-1 text-gray-500">
                            Regular sampling (e.g., sugar shake) is required for Varroa management.
                        </figcaption>
                    </figure>
                </aside>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- 4. HONEY & HARVEST PAGE (Video/Animation) -->
        <!-- ========================================================================= -->
        <section id="harvesting" class="bg-white p-8 rounded-xl shadow-lg mb-12">
            <h2 class="text-3xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">3. Honey & Harvest: From Hive to Jar</h2>
            
            <p class="text-lg mb-6">
                Harvesting honey is one of the most rewarding aspects of beekeeping. It typically happens in late summer or early fall after the main nectar flow ends. Always ensure the bees have enough stores for themselves before taking the excess.
            </p>
            
            <h3 class="text-2xl font-semibold text-amber-700 mb-4">Video Guide: Honey Extraction</h3>
            
            <!-- Video/Multimedia Element -->
            <div class="relative overflow-hidden w-full" style="padding-top: 56.25%">
                <!-- Embedded YouTube Player (Placeholder for a relevant beekeeping video) -->
               <iframe width="560" height="315" src="https://www.youtube.com/embed/4O1IQkhVPAI?si=wf1BCmhAJaD09mCw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
            
            <figure class="mt-4 text-center">
                <figcaption class="text-sm italic text-gray-600">
                    Watch this short demonstration on how to safely uncap and spin honey frames using a centrifugal extractor.
                </figcaption>
            </figure>
            
            <!-- Accessibility: Transcript or description for visual/hearing impaired -->
            <div role="contentinfo" class="mt-6 p-4 bg-gray-100 rounded-lg border-l-4 border-amber-500">
                <h4 class="font-bold text-lg mb-2">Video Accessibility Transcript Summary:</h4>
                <p class="text-sm">
                    The video details three steps: 1) **Preparation:** Ensure frames are 80% capped. Remove frames gently. 2) **Uncapping:** Use a hot knife or fork to remove the wax cappings, revealing the honey. 3) **Extraction:** Place frames in the centrifugal extractor and spin. The force pulls the honey out of the comb, ready for filtering and bottling. (Full transcript available upon request.)
                </p>
            </div>

            <figure class="mt-8 text-center">
                <img src="https://openclipart.org/image/2400px/svg_to_png/162139/Honey-Jar-1.png" 
                     alt="A clear glass jar filled with golden, freshly harvested honey." 
                     width="300px" height="300px"
                     class="mx-auto rounded-lg shadow-md border-2 border-yellow-500"
                     onerror="this.src='https://placehold.co/400x250/ffc300/333?text=Honey+Jar+Placeholder';"
                >
                <figcaption class="text-sm italic mt-2 text-gray-600">
                    Different floral sources yield different colors and flavors of honey.
                </figcaption>
            </figure>
        </section>
        
        <!-- ========================================================================= -->
        <!-- 5. COMMUNITY & RESOURCES PAGE (Form) -->
        <!-- ========================================================================= -->
        <section id="resources" class="bg-white p-8 rounded-xl shadow-lg mb-12">
            <h2 class="text-3xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">4. Community & Resources</h2>
            
            <!-- Form with at least 3 elements -->
            <div class="max-w-xl mx-auto p-6 bg-yellow-50 rounded-lg shadow-inner">
                <h3 class="text-2xl font-semibold text-amber-700 mb-4 text-center">Join Our Hive Community Newsletter</h3>
                <form id="newsletter-form" class="space-y-4">
                    
                    <!-- Form Element 1: Text Input (Name) -->
                    <div>
                        <label for="full-name" class="block text-sm font-medium text-gray-700">Full Name</label>
                        <input type="text" id="full-name" name="full-name" required 
                               aria-required="true" 
                               placeholder="John Doe"
                               class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 focus:border-yellow-500 focus:ring focus:ring-yellow-200 focus:ring-opacity-50">
                    </div>
                    
                    <!-- Form Element 2: Email Input -->
                    <div>
                        <label for="email-address" class="block text-sm font-medium text-gray-700">Email Address</label>
                        <input type="email" id="email-address" name="email-address" required 
                               aria-required="true"
                               placeholder="your.email@example.com"
                               class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 focus:border-yellow-500 focus:ring focus:ring-yellow-200 focus:ring-opacity-50">
                    </div>

                    <!-- Form Element 3: Select Dropdown -->
                    <div>
                        <label for="interest-level" class="block text-sm font-medium text-gray-700">Your Current Beekeeping Level</label>
                        <select id="interest-level" name="interest-level" required 
                                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 bg-white focus:border-yellow-500 focus:ring focus:ring-yellow-200 focus:ring-opacity-50">
                            <option value="">-- Select an option --</option>
                            <option value="beginner">Beginner (Planning to start)</option>
                            <option value="novice">Novice (1-2 years experience)</option>
                            <option value="expert">Expert (3+ years experience)</option>
                            <option value="curious">Just Curious About Bees</option>
                        </select>
                    </div>

                    <!-- Submit Button -->
                    <button type="submit" class="w-full bg-amber-800 text-white font-bold py-3 px-4 rounded-lg hover:bg-amber-900 transition duration-300 shadow-lg">
                        Subscribe & Get the Free Starter Guide
                    </button>
                    <p id="form-message" class="text-center mt-2 text-green-700 font-semibold hidden">Thank you for subscribing!</p>
                </form>
            </div>
            
            <script>
                // Simple form submission handler
                document.getElementById('newsletter-form').addEventListener('submit', function(event) {
                    event.preventDefault();
                    // In a real application, you would send this data to a server.
                    console.log('Form Submitted:', {
                        name: document.getElementById('full-name').value,
                        email: document.getElementById('email-address').value,
                        level: document.getElementById('interest-level').value,
                    });
                    
                    // Show confirmation message
                    const message = document.getElementById('form-message');
                    message.classList.remove('hidden');
                    // Reset form after a small delay
                    setTimeout(() => {
                        this.reset();
                        message.classList.add('hidden');
                    }, 3000);
                });
            </script>
            
            <figure class="mt-8 text-center">
                <img src="https://static.vecteezy.com/system/resources/previews/036/151/797/non_2x/beekeeper-in-suit-hat-at-beehive-with-smoker-vector.jpg" 
                     alt="A small group of beekeepers talking around an active hive in a community garden." 
                     width="200px" height="200px"
                     class="mx-auto rounded-lg shadow-md border-2 border-amber-800"
                     onerror="this.src='https://placehold.co/400x250/795548/FFF?text=Community+Placeholder';"
                >
                <figcaption class="text-sm italic mt-2 text-gray-600">
                    Connecting with other beekeepers is the best way to learn and grow.
                </figcaption>
            </figure>
        </section>

        <!-- ========================================================================= -->
        <!-- 6. ABOUT US PAGE -->
        <!-- ========================================================================= -->
        <section id="about" class="bg-white p-8 rounded-xl shadow-lg">
            <h2 class="text-3xl font-bold text-amber-800 mb-6 border-b-2 border-yellow-500 pb-2">5. About Us: Our Mission</h2>
            
            <div class="space-y-4 text-lg">
                <p>
                    **The Hive Guardian** was founded on the principle that healthy bees create a healthy planet. We believe that proper education and adherence to **best practices** are non-negotiable for anyone who takes on the responsibility of stewardship over a colony of honey bees.
                </p>
                <p>
                    Our core values are **Sustainability**, **Education**, and **Conservation**. Every piece of advice provided on this site emphasizes long-term hive survival over short-term honey yields.
                </p>
            </div>

            <h3 class="text-2xl font-semibold text-amber-700 mt-6 mb-3">Contact Information</h3>
            <address class="space-y-1 not-italic text-lg">
                <p><strong>Email:</strong> <a href="mailto:info@hiveguardian.org" class="text-blue-600 hover:underline">info@hiveguardian.org</a></p>
                <p><strong>Address:</strong> 456 Pollinator Path, Bee County, CA 90210</p>
                <p><strong>Phone:</strong> (555) BEE-HIVE</p>
            </address>

            <figure class="mt-8 text-center">
                <img src="https://img.clipart-library.com/24/3172cb07-d375-41b1-9d1f-7c18568adc5a.png" 
                     alt="A single honey bee collecting pollen from a yellow flower in a garden." 
                     width="200px" height="200px"
                     class="mx-auto rounded-lg shadow-md border-2 border-amber-800"
                     onerror="this.src='https://placehold.co/400x250/a0522d/FFF?text=Bee+Placeholder';"
                >
                <figcaption class="text-sm italic mt-2 text-gray-600">
                    Every bee plays a vital role in our ecosystem.
                </figcaption>
            </figure>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-amber-900 text-white p-6 mt-12">
        <div class="max-w-7xl mx-auto text-center text-sm">
            <p>&copy; 2025 The Hive Guardian | All Rights Reserved.</p>
            <p class="mt-2">
                <a href="#home" class="hover:underline mx-2">Back to Top</a> | 
                <a href="https://example.com/privacy" target="_blank" class="hover:underline mx-2">Privacy Policy (External Link)</a>
            </p>
        </div>
    </footer>

</body>
</html>
