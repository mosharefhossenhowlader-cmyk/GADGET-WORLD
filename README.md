                        <div>
                            <p class="font-bold text-white" <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Digital Clock</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #1e1e2f, #2a2a40);
            color: #ffffff;
        }

        .clock-container {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px 60px;
            border-radius: 20px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
        }

        .time {
            font-size: 4rem;
            font-weight: 700;
            letter-spacing: 2px;
            color: #00ffcc;
            text-shadow: 0 0 10px rgba(0, 255, 204, 0.3);
        }

        .date {
            font-size: 1.2rem;
            margin-top: 10px;
            color: #b0b0c3;
            letter-spacing: 1px;
        }
    </style>
</head>
<body>

    <div class="clock-container">
        <div class="time" id="clock">00:00:00</div>
        <div class="date" id="date">Loading date...</div>
    </div>

    <script>
        function updateClock() {
            const now = new Date();
            
            // Format Time (HH:MM:SS)
            let hours = now.getHours();
            const minutes = String(now.getMinutes()).padStart(2, '0');
            const seconds = String(now.getSeconds()).padStart(2, '0');
            const ampm = hours >= 12 ? 'PM' : 'AM';
            
            hours = hours % 12;
            hours = hours ? hours.toString().padStart(2, '0') : '12'; // the hour '0' should be '12'
            
            const timeString = `${hours}:${minutes}:${seconds} ${ampm}`;
            document.getElementById('clock').textContent = timeString;

            // Format Date (Day, Month Date Year)
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            const dateString = now.toLocaleDateString(undefined, options);
            document.getElementById('date').textContent = dateString;
        }

        // Update clock every second
        setInterval(updateClock, 1000);
        updateClock(); // Initial call to avoid 1-second delay
    </script>

</body>
</html>
 Turbo Fan</p>
                            <p class="text-xs text-zinc-400 mt-0.5">Color: <span id="summary-color" class="text-white font-semibold">Black</span> | Qty: <span id="summary-qty" class="text-white font-semibold">1</span></p>
                        </div>
                        <div class="text-right">
                            <span class="text-xs text-zinc-500 block">Total Payable</span>
                            <span id="summary-total" class="text-base font-extrabold text-meyon-orange">৳620</span>
                        </div>
                    </div>

                    <!-- Full Name -->
                    <div class="space-y-2">
                        <label class="block text-sm font-medium text-zinc-300" for="full-name">Full Name <span class="text-meyon-orange">*</span></label>
                        <input type="text" id="full-name" placeholder="Enter your full name" class="w-full bg-meyon-dark border border-meyon-border rounded-xl px-4 py-3 text-sm text-white placeholder-zinc-600 focus:outline-none focus:border-meyon-orange transition-colors">
                        <p id="error-full-name" class="text-xs text-red-500 hidden"></p>
                    </div>

                    <!-- Mobile Number -->
                    <div class="space-y-2">
                        <label class="block text-sm font-medium text-zinc-300" for="mobile-number">Mobile Number <span class="text-meyon-orange">*</span></label>
                        <input type="tel" id="mobile-number" placeholder="e.g. 01700000000" class="w-full bg-meyon-dark border border-meyon-border rounded-xl px-4 py-3 text-sm text-white placeholder-zinc-600 focus:outline-none focus:border-meyon-orange transition-colors">
                        <p id="error-mobile-number" class="text-xs text-red-500 hidden"></p>
                    </div>

                    <!-- Full Delivery Address -->
                    <div class="space-y-2">
                        <label class="block text-sm font-medium text-zinc-300" for="delivery-address">Full Delivery Address <span class="text-meyon-orange">*</span></label>
                        <textarea id="delivery-address" rows="3" placeholder="House/Road, Area, Thana, District" class="w-full bg-meyon-dark border border-meyon-border rounded-xl px-4 py-3 text-sm text-white placeholder-zinc-600 focus:outline-none focus:border-meyon-orange transition-colors resize-none"></textarea>
                        <p id="error-delivery-address" class="text-xs text-red-500 hidden"></p>
                    </div>

                    <!-- Color & Quantity Hidden / Display confirmation -->
                    <div class="grid grid-cols-2 gap-4">
                        <div class="space-y-1">
                            <span class="text-xs text-zinc-400 block">Selected Color</span>
                            <div class="bg-meyon-dark border border-meyon-border px-4 py-2.5 rounded-xl text-sm font-semibold text-white capitalize" id="form-display-color">Black</div>
                        </div>
                        <div class="space-y-1">
                            <span class="text-xs text-zinc-400 block">Quantity</span>
                            <div class="bg-meyon-dark border border-meyon-border px-4 py-2.5 rounded-xl text-sm font-semibold text-white" id="form-display-qty">1</div>
                        </div>
                    </div>

                    <!-- Payment Verification Area -->
                    <div class="space-y-4 pt-4 border-t border-meyon-border">
                        <div class="flex items-center justify-between">
                            <label class="block text-sm font-medium text-zinc-300">Payment Method <span class="text-meyon-orange">*</span></label>
                            <span class="text-xs bg-purple-500/10 text-purple-400 px-2.5 py-1 rounded border border-purple-500/20 font-semibold">Rocket Secure</span>
                        </div>
                        
                        <!-- Rocket Option Card -->
                        <div class="bg-meyon-dark border-2 border-purple-500/50 p-4 rounded-xl flex items-center justify-between">
                            <div class="flex items-center gap-3">
                                <div class="w-8 h-8 rounded-full bg-purple-600 text-white font-bold flex items-center justify-center text-xs">R</div>
                                <div>
                                    <p class="text-sm font-bold text-white">Rocket Mobile Banking</p>
                                    <p class="text-xs text-zinc-400">Manual verification required after payment</p>
                                </div>
                            </div>
                            <span class="text-xs text-emerald-400 font-semibold"><i class="fa-solid fa-check"></i> Selected</span>
                        </div>

                        <!-- TRX ID Input -->
                        <div class="space-y-2">
                            <label class="block text-sm font-medium text-zinc-300" for="trx-id">Rocket Transaction ID (TRX ID) <span class="text-meyon-orange">*</span></label>
                            <input type="text" id="trx-id" placeholder="Enter your Rocket TRX ID (e.g. 9N74K...)" class="w-full bg-meyon-dark border border-meyon-border rounded-xl px-4 py-3 text-sm text-white placeholder-zinc-600 focus:outline-none focus:border-meyon-orange transition-colors uppercase font-mono">
                            <p class="text-[11px] text-zinc-500">Please send money to our merchant/personal Rocket number and enter the exact TRX ID here.</p>
                            <p id="error-trx-id" class="text-xs text-red-500 hidden"></p>
                        </div>
                    </div>

                    <!-- Submit Button -->
                    <button type="submit" class="w-full bg-meyon-orange hover:bg-meyon-orangeHover text-white font-bold py-4 px-6 rounded-xl transition-all shadow-lg shadow-meyon-orange/25 text-base tracking-wide flex items-center justify-center gap-2">
                        <i class="fa-solid fa-shield-check"></i>
                        <span>SUBMIT ORDER</span>
                    </button>

                    <p class="text-center text-xs text-zinc-500">By clicking submit, your order status will be set to <span class="text-zinc-300 font-semibold">Payment Verification Pending</span> until reviewed by our support team.</p>

                </form>
            </div>

        </div>
    </section>

    <!-- FAQ SECTION -->
    <section id="faq" class="py-16 max-w-4xl mx-auto px-4 sm:px-6">
        <div class="text-center mb-12">
            <span class="text-meyon-orange text-xs font-bold uppercase tracking-widest bg-meyon-orange/10 px-3 py-1 rounded-full border border-meyon-orange/20">Help Center</span>
            <h2 class="text-2xl sm:text-3xl font-extrabold mt-3 mb-2">Frequently Asked Questions</h2>
            <p class="text-sm text-zinc-400">Got questions? We have clear answers.</p>
        </div>

        <div class="space-y-4">
            <!-- FAQ 1 -->
            <div class="bg-meyon-card border border-meyon-border rounded-xl p-5 sm:p-6">
                <h3 class="text-base font-bold text-white mb-2 flex items-center justify-between">
                    <span>What is the price?</span>
                    <i class="fa-solid fa-plus text-xs text-zinc-500"></i>
                </h3>
                <p class="text-sm text-zinc-400 leading-relaxed">The special offer price is ৳620, which includes delivery charges nationwide across Bangladesh.</p>
            </div>

            <!-- FAQ 2 -->
            <div class="bg-meyon-card border border-meyon-border rounded-xl p-5 sm:p-6">
                <h3 class="text-base font-bold text-white mb-2 flex items-center justify-between">
                    <span>What colors are available?</span>
                    <i class="fa-solid fa-plus text-xs text-zinc-500"></i>
                </h3>
                <p class="text-sm text-zinc-400 leading-relaxed">The MEYON Mini Turbo Fan is available in two attractive color options: Black and White/Silver.</p>
            </div>

            <!-- FAQ 3 -->
            <div class="bg-meyon-card border border-meyon-border rounded-xl p-5 sm:p-6">
                <h3 class="text-base font-bold text-white mb-2 flex items-center justify-between">
                    <span>How many speed levels does it have?</span>
                    <i class="fa-solid fa-plus text-xs text-zinc-500"></i>
                </h3>
                <p class="text-sm text-zinc-400 leading-relaxed">It features 5-level speed control, allowing you to easily customize your personal airflow.</p>
            </div>

            <!-- FAQ 4 -->
            <div class="bg-meyon-card border border-meyon-border rounded-xl p-5 sm:p-6">
                <h3 class="text-base font-bold text-white mb-2 flex items-center justify-between">
                    <span>How do I place an order?</span>
                    <i class="fa-solid fa-plus text-xs text-zinc-500"></i>
                </h3>
                <p class="text-sm text-zinc-400 leading-relaxed">Select your preferred color and quantity, enter your delivery details, provide your Rocket TRX ID in the order form, and submit your order.</p>
            </div>

            <!-- FAQ 5 -->
            <div class="bg-meyon-card border border-meyon-border rounded-xl p-5 sm:p-6">
                <h3 class="text-base font-bold text-white mb-2 flex items-center justify-between">
                    <span>Can I order through WhatsApp?</span>
                    <i class="fa-solid fa-plus text-xs text-zinc-500"></i>
                </h3>
                <p class="text-sm text-zinc-400 leading-relaxed">Yes! You can order directly through WhatsApp by clicking the "Order on WhatsApp" button on the page.</p>
            </div>
        </div>
    </section>

    <!-- PREMIUM FOOTER -->
    <footer class="bg-meyon-dark border-t border-meyon-border pt-16 pb-24 sm:pb-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10 pb-12 border-b border-meyon-border">
                
                <!-- Col 1: Brand Info -->
                <div class="space-y-4">
                    <div class="bg-white text-meyon-black font-extrabold text-xl px-3 py-1 rounded tracking-tighter inline-block">
                        MEYON
                    </div>
                    <p class="text-sm text-zinc-400 leading-relaxed">
                        Smart products. Better everyday living.
                    </p>
                    <div class="space-y-2 text-sm text-zinc-400">
                        <p class="flex items-center gap-2"><i class="fa-solid fa-phone text-meyon-orange"></i> 01336486494</p>
                        <p class="flex items-center gap-2"><i class="fa-brands fa-whatsapp text-meyon-orange"></i> 01336486494</p>
                    </div>
                </div>

                <!-- Col 2: Support -->
                <div class="space-y-3">
                    <h4 class="text-sm font-bold uppercase tracking-wider text-white">Support</h4>
                    <ul class="space-y-2 text-sm text-zinc-400">
                        <li><a href="#order-section" class="hover:text-meyon-orange transition-colors">Contact Us</a></li>
                        <li><a href="#delivery-section" class="hover:text-meyon-orange transition-colors">Delivery Information</a></li>
                        <li><a href="#order-section" class="hover:text-meyon-orange transition-colors">Payment Verification</a></li>
                        <li><a href="#faq" class="hover:text-meyon-orange transition-colors">FAQ</a></li>
                    </ul>
                </div>

                <!-- Col 3: Shop -->
                <div class="space-y-3">
                    <h4 class="text-sm font-bold uppercase tracking-wider text-white">Shop</h4>
                    <ul class="space-y-2 text-sm text-zinc-400">
                        <li><a href="#" class="hover:text-meyon-orange transition-colors">Mini Turbo Fan</a></li>
                        <li><a href="#" class="hover:text-meyon-orange transition-colors">All Products</a></li>
                    </ul>
                </div>

                <!-- Col 4: Bangladesh Nationwide Service -->
                <div class="space-y-3">
                    <h4 class="text-sm font-bold uppercase tracking-wider text-white">Nationwide Service</h4>
                    <p class="text-sm text-zinc-400 leading-relaxed">Proudly serving customers across all districts and divisions in Bangladesh with secure delivery.</p>
                    <div class="pt-2">
                        <span class="inline-block bg-meyon-card border border-meyon-border text-xs text-zinc-300 px-3 py-1.5 rounded-lg font-mono">
                            <i class="fa-solid fa-shield text-meyon-orange mr-1"></i> Secure E-Commerce
                        </span>
                    </div>
                </div>

            </div>

            <!-- Copyright -->
            <div class="pt-8 flex flex-col sm:flex-row items-center justify-between text-xs text-zinc-500 gap-4">
                <p>&copy; 2026 MEYON. All rights reserved.</p>
                <div class="flex items-center gap-6">
                    <a href="#" class="hover:text-zinc-400">Privacy Policy</a>
                    <a href="#" class="hover:text-zinc-400">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- STICKY MOBILE CTA BAR -->
    <div class="fixed bottom-0 left-0 right-0 z-50 bg-meyon-dark/95 backdrop-blur-md border-t border-meyon-border p-3 sm:hidden flex items-center gap-3">
        <a href="https://wa.me/8801336486494?text=Hello%20MEYON,%20I%20want%20to%20order%20the%20Mini%20Turbo%20Fan." target="_blank" class="bg-emerald-600 hover:bg-emerald-700 text-white font-semibold py-3 px-4 rounded-xl text-xs flex items-center justify-center gap-2 flex-shrink-0">
            <i class="fa-brands fa-whatsapp text-base"></i>
            <span>WhatsApp</span>
        </a>
        <a href="#order-section" class="flex-1 bg-meyon-orange hover:bg-meyon-orangeHover text-white font-bold py-3 px-4 rounded-xl text-xs text-center tracking-wide uppercase shadow-lg shadow-meyon-orange/20">
            ORDER NOW (৳620)
        </a>
    </div>

    <!-- ORDER SUCCESS MODAL -->
    <div id="success-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-meyon-card border border-meyon-border rounded-2xl max-w-md w-full p-6 sm:p-8 text-center space-y-4 animate-in fade-in zoom-in duration-200">
            <div class="w-16 h-16 rounded-full bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-2xl flex items-center justify-center mx-auto">
                <i class="fa-solid fa-check"></i>
            </div>
            <h3 class="text-xl font-extrabold text-white">Order Received Successfully!</h3>
            <p class="text-sm text-zinc-400 leading-relaxed">
                Thank you, <span id="modal-customer-name" class="font-semibold text-white">Customer</span>. Your order for the <span class="font-semibold text-white">Mini Turbo Fan</span> has been placed.
            </p>
            <div class="bg-meyon-dark border border-meyon-border p-3 rounded-xl text-left text-xs space-y-1.5">
                <p class="flex justify-between"><span class="text-zinc-500">Status:</span> <span class="text-amber-400 font-semibold">Payment Verification Pending</span></p>
                <p class="flex justify-between"><span class="text-zinc-500">Payment Method:</span> <span class="text-white font-semibold">Rocket</span></p>
                <p class="flex justify-between"><span class="text-zinc-500">TRX ID:</span> <span class="text-white font-mono font-semibold" id="modal-trx-id">---</span></p>
            </div>
            <p class="text-xs text-zinc-500">Our support team will manually verify your Rocket TRX ID and confirm your order shortly via phone.</p>
            <button onclick="closeSuccessModal()" class="w-full bg-meyon-orange hover:bg-meyon-orangeHover text-white font-bold py-3 rounded-xl transition-all text-sm">
                Close & Continue
            </button>
        </div>
    </div>

    <!-- INTERACTIVE FRONTEND LOGIC -->
    <script>
        // State Management
        let state = {
            selectedColor: 'Black',
            quantity: 1,
            unitPrice: CONFIG.UNIT_PRICE,
            images: CONFIG.PRODUCT_IMAGES
        };

        // Switch Main Product Image
        function switchImage(index, buttonElement) {
            const mainImg = document.getElementById('main-product-image');
            mainImg.src = state.images[index].url;
            mainImg.alt = state.images[index].alt;

            // Update active thumbnail styles
            document.querySelectorAll('.thumb-btn').forEach(btn => {
                btn.classList.remove('border-meyon-orange');
                btn.classList.add('border-transparent');
            });
            buttonElement.classList.remove('border-transparent');
            buttonElement.classList.add('border-meyon-orange');
        }

        // Color Selection
        function selectColor(colorId, colorName, buttonElement) {
            state.selectedColor = colorName;
            document.getElementById('selected-color-name').textContent = colorName;
            document.getElementById('form-display-color').textContent = colorName;
            document.getElementById('summary-color').textContent = colorName;

            // Update button styles
            document.querySelectorAll('.color-btn').forEach(btn => {
                btn.classList.remove('border-meyon-orange', 'active-color');
                btn.classList.add('border-meyon-border');
            });
            buttonElement.classList.remove('border-meyon-border');
            buttonElement.classList.add('border-meyon-orange', 'active-color');
        }

        // Quantity Update
        function updateQuantity(change) {
            let newQty = state.quantity + change;
            if (newQty < 1) newQty = 1;
            if (newQty > 10) newQty = 10; // reasonable limit
            state.quantity = newQty;

            // Update UI elements
            document.getElementById('quantity-display').textContent = newQty;
            document.getElementById('form-display-qty').textContent = newQty;
            document.getElementById('summary-qty').textContent = newQty;

            // Calculate total price
            const total = newQty * state.unitPrice;
            const formattedTotal = '৳' + total.toLocaleString();
            document.getElementById('total-price-display').textContent = formattedTotal;
            document.getElementById('summary-total').textContent = formattedTotal;
        }

        // WhatsApp Direct Order Trigger
        function openWhatsApp() {
            const message = `Hello MEYON, I want to order the Mini Turbo Fan. Color: ${state.selectedColor}, Quantity: ${state.quantity}, Total: ৳${state.quantity * state.unitPrice}.`;
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://wa.me/880${CONFIG.WHATSAPP_NUMBER.replace(/^0/, '')}?text=${encodedMessage}`;
            window.open(whatsappUrl, '_blank');
        }

        // Form Validation & Submission Handler
        function handleOrderSubmission(event) {
            event.preventDefault();

            // Clear previous errors
            document.querySelectorAll('[id^="error-"]').forEach(el => {
                el.textContent = '';
                el.classList.add('hidden');
            });

            // Get form field values
            const fullName = document.getElementById('full-name').value.trim();
            const mobileNumber = document.getElementById('mobile-number').value.trim();
            const deliveryAddress = document.getElementById('delivery-address').value.trim();
            const trxId = document.getElementById('trx-id').value.trim();

            let isValid = true;

            // Validation checks
            if (!fullName) {
                showError('error-full-name', 'Please enter your full name.');
                isValid = false;
            }

            if (!mobileNumber || !/^01[3-9]\d{8}$/.test(mobileNumber)) {
                showError('error-mobile-number', 'Please enter a valid mobile number (e.g. 01700000000).');
                isValid = false;
            }

            if (!deliveryAddress) {
                showError('error-delivery-address', 'Please enter your full delivery address.');
                isValid = false;
            }

            if (!trxId) {
                showError('error-trx-id', 'Please enter your Rocket TRX ID.');
                isValid = false;
            }

            if (!isValid) return;

            // Prepare order data object
            const orderData = {
                product: CONFIG.PRODUCT_NAME,
                color: state.selectedColor,
                quantity: state.quantity,
                unitPrice: state.unitPrice,
                total: state.quantity * state.unitPrice,
                customerName: fullName,
                phone: mobileNumber,
                address: deliveryAddress,
                paymentMethod: "Rocket",
                trxId: trxId,
                orderTime: new Date().toLocaleString(),
                status: "Payment Verification Pending"
            };

            // Send to Telegram Bot securely via backend/webhook structure
            sendToTelegram(orderData);

            // Show Success Modal
            document.getElementById('modal-customer-name').textContent = fullName;
            document.getElementById('modal-trx-id').textContent = trxId;
            document.getElementById('success-modal').classList.remove('hidden');
            document.getElementById('success-modal').classList.add('flex');

            // Reset form
            document.getElementById('checkout-form').reset();
            updateQuantity(1 - state.quantity); // reset qty to 1
        }

        function showError(elementId, message) {
            const el = document.getElementById(elementId);
            el.textContent = message;
            el.classList.remove('hidden');
        }

        function closeSuccessModal() {
            document.getElementById('success-modal').classList.remove('flex');
            document.getElementById('success-modal').classList.add('hidden');
        }

        // Telegram Bot Notification Integration
        function sendToTelegram(data) {
            const telegramMessage = `━━━━━━━━━━━━━━ 🛒 NEW MEYON ORDER ━━━━━━━━━━━━━━\n` +
                `Product: ${data.product}\n` +
                `Color: ${data.color}\n` +
                `Quantity: ${data.quantity}\n` +
                `Unit Price: ৳${data.unitPrice}\n` +
                `Total: ৳${data.total}\n` +
                `Customer Name: ${data.customerName}\n` +
                `Phone: ${data.phone}\n` +
                `Address: ${data.address}\n` +
                `Payment Method: ${data.paymentMethod}\n` +
                `TRX ID: ${data.trxId}\n` +
                `Order Time: ${data.orderTime}\n` +
                `Status: ${data.status}\n` +
                `━━━━━━━━━━━━━━`;

            // Note: In production, configure TELEGRAM_CONFIG.ENDPOINT to point to your secure backend serverless function (e.g. Vercel/Netlify function) to keep Bot Tokens private.
            // Example fetch request payload:
            /*
            fetch(CONFIG.TELEGRAM_CONFIG.ENDPOINT, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    chat_id: CONFIG.TELEGRAM_CONFIG.CHAT_ID,
                    text: telegramMessage
                })
            }).catch(err => console.error('Telegram notification error:', err));
            */
            console.log("Telegram Notification Payload Prepared:", telegramMessage);
        }
    </script>
</body>
</html>
