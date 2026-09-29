index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ola-Ola Food Canteen | Mushin, Lagos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #113689;
            --primary-dark: #0a235c;
            --accent: #f8c21a;
            --accent-hover: #e0ac07;
            --secondary: #28a745;
            --danger: #dc3545;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --card-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            padding-bottom: 60px;
        }

        /* Top Announcement Header */
        .top-bar {
            background-color: var(--accent);
            color: #000;
            text-align: center;
            padding: 8px 15px;
            font-weight: 700;
            font-size: 14px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        /* Navigation Header */
        header {
            background-color: var(--primary);
            color: white;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .brand-logo {
            width: 45px;
            height: 45px;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 22px;
        }

        .brand-text h1 {
            font-size: 22px;
            color: var(--accent);
            line-height: 1.1;
            letter-spacing: 0.5px;
        }

        .brand-text p {
            font-size: 11px;
            color: #cbd5e1;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-actions {
            display: flex;
            gap: 12px;
            align-items: center;
        }

        .btn {
            padding: 9px 18px;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: none;
            font-size: 14px;
            transition: all 0.2s ease;
        }

        .btn-accent {
            background-color: var(--accent);
            color: #000;
        }

        .btn-accent:hover {
            background-color: var(--accent-hover);
        }

        .btn-outline {
            background: transparent;
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .btn-outline:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        /* Mode Switcher Banner */
        .mode-bar {
            background-color: var(--primary-dark);
            padding: 10px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: white;
            font-size: 13px;
        }

        .mode-toggle-btn {
            background: rgba(255, 255, 255, 0.15);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            cursor: pointer;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        /* Hero Banner Section */
        .hero {
            background: linear-gradient(rgba(17, 54, 137, 0.88), rgba(10, 35, 92, 0.92)), 
                        url('https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
            color: white;
            text-align: center;
            padding: 60px 20px;
        }

        .hero h2 {
            font-size: 38px;
            color: var(--accent);
            margin-bottom: 12px;
            font-weight: 800;
        }

        .hero p {
            font-size: 17px;
            max-width: 650px;
            margin: 0 auto 25px;
            color: #e2e8f0;
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: -30px auto 0;
            padding: 0 20px;
        }

        /* Quick Info Cards */
        .info-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .info-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: var(--card-shadow);
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .info-icon {
            width: 50px;
            height: 50px;
            background: #eef2ff;
            color: var(--primary);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 22px;
            flex-shrink: 0;
        }

        .info-text h4 {
            font-size: 16px;
            color: var(--dark);
        }

        .info-text p {
            font-size: 13px;
            color: var(--gray);
        }

        /* Section Title */
        .section-header {
            text-align: center;
            margin: 40px 0 25px;
        }

        .section-header h3 {
            font-size: 28px;
            color: var(--primary);
        }

        .section-header p {
            color: var(--gray);
            font-size: 14px;
        }

        /* Menu Grid */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 25px;
        }

        .food-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: transform 0.2s ease;
            display: flex;
            flex-direction: column;
            border: 1px solid #e2e8f0;
        }

        .food-card:hover {
            transform: translateY(-5px);
        }

        .food-img-holder {
            height: 180px;
            background-color: #cbd5e1;
            position: relative;
            background-size: cover;
            background-position: center;
        }

        .food-tag {
            position: absolute;
            top: 10px;
            right: 10px;
            background: var(--primary);
            color: white;
            font-size: 11px;
            font-weight: 700;
            padding: 4px 10px;
            border-radius: 20px;
        }

        .food-details {
            padding: 18px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .food-title {
            font-size: 18px;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 6px;
        }

        .food-desc {
            font-size: 13px;
            color: var(--gray);
            margin-bottom: 15px;
            flex-grow: 1;
        }

        .food-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
        }

        .food-price {
            font-size: 18px;
            font-weight: 800;
            color: var(--primary);
        }

        /* Cashier POS Mode Panel */
        .pos-panel {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: var(--card-shadow);
            display: none;
            margin-bottom: 40px;
        }

        .pos-grid {
            display: grid;
            grid-template-columns: 1fr 380px;
            gap: 25px;
        }

        @media (max-width: 900px) {
            .pos-grid {
                grid-template-columns: 1fr;
            }
        }

        .pos-table-container {
            max-height: 450px;
            overflow-y: auto;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #e2e8f0;
            font-size: 14px;
        }

        th {
            background: var(--primary);
            color: white;
            position: sticky;
            top: 0;
        }

        .order-summary-card {
            background: #f8fafc;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            padding: 20px;
        }

        .summary-line {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-size: 15px;
        }

        .summary-total {
            font-size: 22px;
            font-weight: 800;
            color: var(--primary);
            border-top: 2px dashed #cbd5e1;
            padding-top: 10px;
            margin-top: 10px;
        }

        input, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            margin-top: 5px;
            margin-bottom: 15px;
            font-size: 14px;
        }

        /* Catering Section */
        .catering-box {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            border-radius: 16px;
            padding: 40px;
            margin: 50px 0;
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 30px;
            align-items: center;
        }

        @media (max-width: 768px) {
            .catering-box {
                grid-template-columns: 1fr;
                text-align: center;
            }
        }

        .catering-text h3 {
            font-size: 28px;
            color: var(--accent);
            margin-bottom: 10px;
        }

        /* Printable Receipt */
        @media print {
            body * {
                visibility: hidden;
            }
            #printableArea, #printableArea * {
                visibility: visible;
            }
            #printableArea {
                position: absolute;
                left: 0;
                top: 0;
                width: 100%;
            }
            .no-print {
                display: none !important;
            }
        }

        /* Floating Cart Badge */
        .cart-badge {
            background: var(--danger);
            color: white;
            border-radius: 50%;
            padding: 2px 7px;
            font-size: 11px;
            font-weight: bold;
        }

        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 30px 20px;
            margin-top: 60px;
        }

        footer p {
            color: #94a3b8;
            font-size: 14px;
            margin-bottom: 8px;
        }
    </style>
</head>
<body>

    <!-- Top Announcement -->
    <div class="top-bar no-print">
        <i class="fa-solid fa-utensils"></i> OLA-OLA FOOD CANTEEN — FRESH HOT MEALS DAILY IN MUSHIN, LAGOS
    </div>

    <!-- Main Navigation Header -->
    <header class="no-print">
        <div class="brand">
            <div class="brand-logo"><i class="fa-solid fa-bowl-food"></i></div>
            <div class="brand-text">
                <h1>OLA-OLA</h1>
                <p>Food Canteen</p>
            </div>
        </div>
        <div class="nav-actions">
            <button class="btn btn-outline" onclick="scrollToSection('menu')">Menu</button>
            <a href="tel:+2348039222123" class="btn btn-accent"><i class="fa-solid fa-phone"></i> Call Order</a>
        </div>
    </header>

    <!-- Mode Switcher Bar -->
    <div class="mode-bar no-print">
        <span><i class="fa-solid fa-store"></i> Operating Mode: <strong id="currentModeLabel">Customer Storefront</strong></span>
        <button class="mode-toggle-btn" onclick="togglePOSMode()"><i class="fa-solid fa-cash-register"></i> Switch to Cashier POS</button>
    </div>

    <!-- Hero Section -->
    <section class="hero no-print">
        <h2>Indoor & Outdoor Catering Services</h2>
        <p>Authentic Nigerian dishes prepared with fresh ingredients daily. Amala, Pounded Yam, Eba, Semo, Ogunfe Goat Meat, Assorted Soups, and Hot Rice.</p>
        <div>
            <a href="https://wa.me/2348039222123?text=Hello%20Ola-Ola%20Food%20Canteen,%20I%20want%20to%20place%20an%20order" class="btn btn-accent"><i class="fa-brands fa-whatsapp"></i> Order on WhatsApp</a>
        </div>
    </section>

    <!-- Container Area -->
    <div class="container">

        <!-- Info Cards -->
        <div class="info-cards no-print">
            <div class="info-card">
                <div class="info-icon"><i class="fa-solid fa-location-dot"></i></div>
                <div class="info-text">
                    <h4>Location</h4>
                    <p>2, Oluaina Street, Off Isolo Road, Mushin, Lagos</p>
                </div>
            </div>
            <div class="info-card">
                <div class="info-icon"><i class="fa-solid fa-phone-volume"></i></div>
                <div class="info-text">
                    <h4>Phone Contacts</h4>
                    <p>+234 803 9222 123<br>+234 908 0335 696</p>
                </div>
            </div>
            <div class="info-card">
                <div class="info-icon"><i class="fa-solid fa-clock"></i></div>
                <div class="info-text">
                    <h4>Opening Hours</h4>
                    <p>Mon - Sat: 8:00 AM - 9:00 PM</p>
                </div>
            </div>
        </div>

        <!-- CASHIER POS PANEL (TOGGLEABLE) -->
        <div class="pos-panel" id="posPanel">
            <h3 style="color: var(--primary); margin-bottom: 20px;"><i class="fa-solid fa-cash-register"></i> Cashier Counter POS Management System</h3>
            <div class="pos-grid">
                <div>
                    <h4>Select Items to Add</h4>
                    <div class="pos-table-container">
                        <table>
                            <thead>
                                <tr>
                                    <th>Food Item</th>
                                    <th>Price</th>
                                    <th>Qty</th>
                                    <th>Action</th>
                                </tr>
                            </thead>
                            <tbody id="posMenuTable">
                                <!-- Populated by JS -->
                            </tbody>
                        </table>
                    </div>
                </div>

                <div class="order-summary-card" id="printableArea">
                    <h4 style="text-align: center; color: var(--primary);">OLA-OLA CANTEEN RECEIPT</h4>
                    <p style="text-align: center; font-size: 11px; color: var(--gray);">2, Oluaina Street, Off Isolo Rd, Mushin</p>
                    <hr style="margin: 10px 0;">

                    <label for="customerName">Customer Name:</label>
                    <input type="text" id="customerName" placeholder="Enter Customer Name">

                    <table>
                        <thead>
                            <tr>
                                <th>Item</th>
                                <th>Qty</th>
                                <th>Subtotal</th>
                                <th class="no-print"></th>
                            </tr>
                        </thead>
                        <tbody id="cartTable">
                            <!-- Cart Items -->
                        </tbody>
                    </table>

                    <div class="summary-line summary-total">
                        <span>Total:</span>
                        <span>₦<span id="posTotal">0</span></span>
                    </div>

                    <div class="no-print">
                        <label for="amountPaid">Amount Paid (₦):</label>
                        <input type="number" id="amountPaid" placeholder="0" oninput="calculateChange()">

                        <div class="summary-line" style="font-weight: bold; color: var(--secondary);">
                            <span>Change:</span>
                            <span>₦<span id="posChange">0</span></span>
                        </div>

                        <button class="btn btn-accent" style="width: 100%; margin-top: 10px;" onclick="printReceipt()"><i class="fa-solid fa-print"></i> Print Receipt</button>
                        <button class="btn btn-outline" style="width: 100%; margin-top: 8px; color: var(--dark); border-color: #cbd5e1;" onclick="clearCart()">Clear Order</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- CUSTOMER STOREFRONT MENU -->
        <div id="menu" class="no-print">
            <div class="section-header">
                <h3>Our Canteen Specialties</h3>
                <p>Freshly prepared soups, swallows, meats, and drinks</p>
            </div>

            <div class="menu-grid" id="customerMenuGrid">
                <!-- Dynamic Food Cards -->
            </div>
        </div>

        <!-- Outdoor Catering Banner -->
        <div class="catering-box no-print">
            <div class="catering-text">
                <h3>Planning a Party or Event?</h3>
                <p>We provide full outdoor catering services for weddings, birthdays, corporate events, and family gatherings across Lagos. Get rich authentic flavors served hot to your guests.</p>
            </div>
            <div>
                <a href="https://wa.me/2348039222123?text=Hello%20Ola-Ola%20Canteen,%20I%20want%20to%20book%20Outdoor%20Catering" class="btn btn-accent" style="width: 100%; justify-content: center;"><i class="fa-brands fa-whatsapp"></i> Book Catering</a>
            </div>
        </div>

    </div>

    <!-- Footer -->
    <footer class="no-print">
        <p><strong>OLA-OLA FOOD CANTEEN</strong></p>
        <p>2, Oluaina Street, Off Isolo Road, Mushin, Lagos, Nigeria</p>
        <p>Tel: +234 (0) 803 9222 123 | +234 (0) 908 0335 696</p>
        <p style="font-size: 12px; margin-top: 15px; color: #64748b;">&copy; 2026 Ola-Ola Food Canteen. All Rights Reserved.</p>
    </footer>

    <script>
        const menuData = [
            { id: 1, name: "Amala", price: 200, category: "Swallow", tag: "Hot", img: "https://images.unsplash.com/photo-1626777552726-4a6b54c97e46?auto=format&fit=crop&w=500&q=80" },
            { id: 2, name: "Pounded Yam", price: 300, category: "Swallow", tag: "Fresh", img: "https://images.unsplash.com/photo-1541544741938-0af808871cc0?auto=format&fit=crop&w=500&q=80" },
            { id: 3, name: "Eba (Garri)", price: 200, category: "Swallow", tag: "Popular", img: "https://images.unsplash.com/photo-1512621776951-a57141f2eefd?auto=format&fit=crop&w=500&q=80" },
            { id: 4, name: "Semo", price: 200, category: "Swallow", tag: "Ready", img: "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?auto=format&fit=crop&w=500&q=80" },
            { id: 5, name: "White Rice & Stew", price: 300, category: "Rice", tag: "Hot", img: "https://images.unsplash.com/photo-1512058564366-18510be2db19?auto=format&fit=crop&w=500&q=80" },
            { id: 6, name: "Smoky Jollof Rice", price: 400, category: "Rice", tag: "Top Choice", img: "https://images.unsplash.com/photo-1604329760661-e71dc83f8f26?auto=format&fit=crop&w=500&q=80" },
            { id: 7, name: "Fried Rice", price: 400, category: "Rice", tag: "Special", img: "https://images.unsplash.com/photo-1603133872878-684f208fb84b?auto=format&fit=crop&w=500&q=80" },
            { id: 8, name: "Ogunfe (Goat Meat)", price: 800, category: "Meat", tag: "Signature", img: "https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=500&q=80" },
            { id: 9, name: "Assorted Meat", price: 500, category: "Meat", tag: "Rich", img: "https://images.unsplash.com/photo-1529193591184-b1d58069ecdd?auto=format&fit=crop&w=500&q=80" },
            { id: 10, name: "Fried / Peppered Fish", price: 600, category: "Fish", tag: "Fresh", img: "https://images.unsplash.com/photo-1519708227418-c8fd9a32b7a2?auto=format&fit=crop&w=500&q=80" },
            { id: 11, name: "Fried Plantain (Dodo)", price: 200, category: "Side", tag: "Sweet", img: "https://images.unsplash.com/photo-1528751014936-863e6e7a319c?auto=format&fit=crop&w=500&q=80" },
            { id: 12, name: "Chilled Soft Drinks", price: 300, category: "Drink", tag: "Cold", img: "https://images.unsplash.com/photo-1622483767028-3f66f32aef97?auto=format&fit=crop&w=500&q=80" }
        ];

        let cart = [];
        let isPOSMode = false;

        function renderCustomerMenu() {
            const grid = document.getElementById("customerMenuGrid");
            grid.innerHTML = "";

            menuData.forEach(item => {
                const card = document.createElement("div");
                card.className = "food-card";
                card.innerHTML = `
                    <div class="food-img-holder" style="background-image: url('${item.img}')">
                        <span class="food-tag">${item.tag}</span>
                    </div>
                    <div class="food-details">
                        <div class="food-title">${item.name}</div>
                        <div class="food-desc">Freshly cooked ${item.name} served hot at Ola-Ola Canteen.</div>
                        <div class="food-footer">
                            <span class="food-price">₦${item.price}</span>
                            <button class="btn btn-accent" onclick="addToCart(${item.id})"><i class="fa-solid fa-plus"></i> Add</button>
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        function renderPOSMenu() {
            const posTable = document.getElementById("posMenuTable");
            posTable.innerHTML = "";

            menuData.forEach(item => {
                const row = document.createElement("tr");
                row.innerHTML = `
                    <td><strong>${item.name}</strong></td>
                    <td>₦${item.price}</td>
                    <td><input type="number" id="posQty-${item.id}" value="1" min="1" style="width: 50px; padding: 4px; margin: 0;"></td>
                    <td><button class="btn btn-accent" style="padding: 4px 10px; font-size: 12px;" onclick="addPosItem(${item.id})">Add</button></td>
                `;
                posTable.appendChild(row);
            });
        }

        function addToCart(id) {
            const item = menuData.find(m => m.id === id);
            const existing = cart.find(c => c.id === id);

            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...item, qty: 1 });
            }
            updateCartUI();
        }

        function addPosItem(id) {
            const qtyInput = document.getElementById(`posQty-${id}`);
            const qty = parseInt(qtyInput.value) || 1;
            const item = menuData.find(m => m.id === id);
            const existing = cart.find(c => c.id === id);

            if (existing) {
                existing.qty += qty;
            } else {
                cart.push({ ...item, qty: qty });
            }
            qtyInput.value = 1;
            updateCartUI();
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCartUI();
        }

        function updateCartUI() {
            const cartTable = document.getElementById("cartTable");
            cartTable.innerHTML = "";
            let grandTotal = 0;

            cart.forEach((item, index) => {
                const subtotal = item.price * item.qty;
                grandTotal += subtotal;

                const row = document.createElement("tr");
                row.innerHTML = `
                    <td>${item.name}</td>
                    <td>${item.qty}</td>
                    <td>₦${subtotal}</td>
                    <td class="no-print"><button onclick="removeFromCart(${index})" style="background:none; border:none; color: red; cursor:pointer;"><i class="fa-solid fa-trash"></i></button></td>
                `;
                cartTable.appendChild(row);
            });

            document.getElementById("posTotal").innerText = grandTotal.toLocaleString();
            calculateChange();
        }

        function calculateChange() {
            const total = parseInt(document.getElementById("posTotal").innerText.replace(/,/g, '')) || 0;
            const paid = parseFloat(document.getElementById("amountPaid").value) || 0;
            const changeDisplay = document.getElementById("posChange");

            if (paid >= total && total > 0) {
                changeDisplay.innerText = (paid - total).toLocaleString();
            } else {
                changeDisplay.innerText = "0";
            }
        }

        function clearCart() {
            cart = [];
            document.getElementById("customerName").value = "";
            document.getElementById("amountPaid").value = "";
            updateCartUI();
        }

        function togglePOSMode() {
            isPOSMode = !isPOSMode;
            const posPanel = document.getElementById("posPanel");
            const label = document.getElementById("currentModeLabel");

            if (isPOSMode) {
                posPanel.style.display = "block";
                label.innerText = "Cashier POS Mode";
                scrollToSection("posPanel");
            } else {
                posPanel.style.display = "none";
                label.innerText = "Customer Storefront";
            }
        }

        function printReceipt() {
            if (cart.length === 0) {
                alert("Please add at least one item to the receipt order.");
                return;
            }
            window.print();
        }

        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }

        // Initialize on Load
        window.onload = function() {
            renderCustomerMenu();
            renderPOSMenu();
        };
    </script>
</body>
</html>

