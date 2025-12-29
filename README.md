<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brandi Russell - Cost Inquiry Form</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #00a5e9;
            --dark-color: #222222;
            --light-bg: #f8f9fa;
            --white: #ffffff;
            --border-color: #e0e0e0;
            --text-gray: #666666;
            --success-color: #27ae60;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--light-bg);
            color: var(--dark-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        header {
            text-align: center;
            margin-bottom: 50px;
            border-bottom: 3px solid var(--primary-color);
            padding-bottom: 30px;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3em;
            color: var(--dark-color);
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 1.1em;
            color: var(--primary-color);
            font-weight: 600;
        }

        .form-wrapper {
            background: var(--white);
            border-radius: 12px;
            padding: 40px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .services-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 25px;
            margin-bottom: 40px;
        }

        .service-category {
            margin-bottom: 20px;
        }

        .category-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.8em;
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--border-color);
        }

        .service-item {
            background: var(--light-bg);
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid var(--primary-color);
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }

        .service-item:hover {
            box-shadow: 0 4px 12px rgba(0, 165, 233, 0.15);
            transform: translateX(5px);
        }

        .service-header {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 12px;
        }

        .service-checkbox {
            width: 24px;
            height: 24px;
            margin-top: 2px;
            cursor: pointer;
            accent-color: var(--primary-color);
            flex-shrink: 0;
        }

        .service-details {
            flex: 1;
        }

        .service-name {
            font-weight: 600;
            font-size: 1.1em;
            color: var(--dark-color);
            margin-bottom: 5px;
        }

        .service-description {
            font-size: 0.95em;
            color: var(--text-gray);
            margin-bottom: 8px;
            line-height: 1.5;
        }

        .service-timeline {
            font-size: 0.9em;
            color: var(--primary-color);
            font-weight: 500;
        }

        .service-price {
            text-align: right;
            padding-left: 15px;
        }

        .price-label {
            font-size: 0.85em;
            color: var(--text-gray);
            display: block;
            margin-bottom: 5px;
        }

        .price-amount {
            font-size: 1.5em;
            font-weight: 600;
            color: var(--primary-color);
        }

        .summary-section {
            background: linear-gradient(135deg, var(--primary-color) 0%, #0087b8 100%);
            color: var(--white);
            padding: 30px;
            border-radius: 8px;
            margin-bottom: 30px;
        }

        .summary-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .summary-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }

        .summary-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 6px;
            border-left: 3px solid var(--white);
        }

        .summary-label {
            font-size: 0.9em;
            opacity: 0.9;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .summary-value {
            font-size: 1.8em;
            font-weight: 700;
            font-family: 'Montserrat', sans-serif;
        }

        .form-actions {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        button {
            padding: 14px 30px;
            font-size: 1em;
            border: none;
            border-radius: 6px;
            font-family: 'Montserrat', sans-serif;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: var(--white);
        }

        .btn-primary:hover {
            background-color: #0087b8;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 165, 233, 0.3);
        }

        .btn-secondary {
            background-color: var(--dark-color);
            color: var(--white);
        }

        .btn-secondary:hover {
            background-color: #444444;
            transform: translateY(-2px);
        }

        .btn-reset {
            background-color: var(--border-color);
            color: var(--dark-color);
        }

        .btn-reset:hover {
            background-color: #c0c0c0;
        }

        .contact-note {
            text-align: center;
            margin-top: 30px;
            padding-top: 30px;
            border-top: 1px solid var(--border-color);
            color: var(--text-gray);
        }

        .contact-note a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
        }

        .contact-note a:hover {
            text-decoration: underline;
        }

        .no-selection {
            text-align: center;
            padding: 40px;
            color: var(--text-gray);
        }

        .success-message {
            display: none;
            background: var(--success-color);
            color: var(--white);
            padding: 15px;
            border-radius: 6px;
            margin-bottom: 20px;
            text-align: center;
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }

            h1 {
                font-size: 2em;
            }

            .form-wrapper {
                padding: 20px;
            }

            .summary-content {
                grid-template-columns: 1fr;
            }

            .form-actions {
                flex-direction: column;
            }

            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Brandi Russell</h1>
            <p class="subtitle">Service Cost Inquiry Form</p>
        </header>

        <div class="form-wrapper">
            <div class="success-message" id="successMessage">
                ✓ Your inquiry has been prepared! Contact Brandi to discuss your project.
            </div>

            <form id="inquiryForm">
                <!-- Brand Services -->
                <div class="service-category">
                    <h2 class="category-title">Brand Services</h2>
                    
                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Brand Messaging" data-price="125" id="service1">
                            <div class="service-details">
                                <label for="service1" class="service-name">Brand Messaging</label>
                                <p class="service-description">Development of a storytelling Brand Script</p>
                                <span class="service-timeline">⏱️ Timeline: 2-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$125</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Brand Visual Identity" data-price="500" id="service2">
                            <div class="service-details">
                                <label for="service2" class="service-name">Brand Visual Identity</label>
                                <p class="service-description">Development of a visual identity including three brand identity options, one revision, square logo, rectangular wordmark, color palette, and typography</p>
                                <span class="service-timeline">⏱️ Timeline: 4-5 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$500</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Custom Logo" data-price="150" id="service3">
                            <div class="service-details">
                                <label for="service3" class="service-name">Custom Logo</label>
                                <p class="service-description">One custom square logo</p>
                                <span class="service-timeline">⏱️ Timeline: 2 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$150</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="LinkedIn Authority Accelerator" data-price="250" id="service4">
                            <div class="service-details">
                                <label for="service4" class="service-name">LinkedIn Authority Accelerator</label>
                                <p class="service-description">Profile optimization checklist and LinkedIn Banner aligned with your brand's visual identity</p>
                                <span class="service-timeline">⏱️ Timeline: 2-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$250</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Website Services -->
                <div class="service-category">
                    <h2 class="category-title">Website Services</h2>
                    
                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Classic Light Website" data-price="1500" id="service5">
                            <div class="service-details">
                                <label for="service5" class="service-name">Classic Light Website</label>
                                <p class="service-description">7-section, customer-first storytelling website built on Wix, fully optimized for desktop and mobile, with one year hosting and 5 hours post-launch support</p>
                                <span class="service-timeline">⏱️ Timeline: 5-7 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$1,500</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Advanced Core Website" data-price="2500" id="service6">
                            <div class="service-details">
                                <label for="service6" class="service-name">Advanced Core Website</label>
                                <p class="service-description">7-section, up to 3 page website with lead-generating form, fully optimized, one year hosting and 10 hours post-launch support</p>
                                <span class="service-timeline">⏱️ Timeline: 7-10 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$2,500</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Elite E-Commerce Business Site" data-price="4000" id="service7">
                            <div class="service-details">
                                <label for="service7" class="service-name">Elite/E-Commerce Business Site</label>
                                <p class="service-description">Customer-first e-commerce website with up to 3 pages, lead-generating form, fully set up online store with 20 products, one year hosting and 10 hours support</p>
                                <span class="service-timeline">⏱️ Timeline: 7-14 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$4,000</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Budget Website Landing Page" data-price="750" id="service8">
                            <div class="service-details">
                                <label for="service8" class="service-name">Budget Website Landing Page</label>
                                <p class="service-description">5-section, customer-first storytelling landing page built on Canva, one year hosting and 5 hours post-launch support</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$750</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Additional Wix Website Pages" data-price="500" id="service9">
                            <div class="service-details">
                                <label for="service9" class="service-name">Additional Wix Website Pages</label>
                                <p class="service-description">Additional website pages added to Classic or Advanced site</p>
                                <span class="service-timeline">⏱️ Timeline: 1 day</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$500</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Additional Basic Website Pages" data-price="200" id="service10">
                            <div class="service-details">
                                <label for="service10" class="service-name">Additional Basic Website Pages</label>
                                <p class="service-description">Additional website pages added to a Budget Landing Page site</p>
                                <span class="service-timeline">⏱️ Timeline: 1 day</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$200</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Custom Email Account" data-price="150" id="service11">
                            <div class="service-details">
                                <label for="service11" class="service-name">Custom Email Account</label>
                                <p class="service-description">Set up one custom email address using Google Workspace on your domain with spam protection, 2FA, and AI-powered writing assistance</p>
                                <span class="service-timeline">⏱️ Timeline: Per Year</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$150/yr</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Print & Digital Collateral -->
                <div class="service-category">
                    <h2 class="category-title">Print & Digital Collateral</h2>
                    
                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Flyer Design (single-sided)" data-price="125" id="service12">
                            <div class="service-details">
                                <label for="service12" class="service-name">Flyer Design (single-sided)</label>
                                <p class="service-description">One-page promotional flyer optimized for print and PDF with layout, imagery, and copy placement</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$125</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Postcard Design" data-price="100" id="service13">
                            <div class="service-details">
                                <label for="service13" class="service-name">Postcard Design</label>
                                <p class="service-description">Front-and-back postcard design for mailers or handouts, aligned with your brand and sized to printer specs</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$100</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Brochure Design" data-price="250" id="service14">
                            <div class="service-details">
                                <label for="service14" class="service-name">Brochure Design</label>
                                <p class="service-description">Multi-panel brochure design (tri-fold or bi-fold) with layout, image placement, and basic copy formatting</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$250</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Poster Design" data-price="150" id="service15">
                            <div class="service-details">
                                <label for="service15" class="service-name">Poster Design</label>
                                <p class="service-description">Large-format poster for events, promotions, or in-store signage, in print-ready and digital formats</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$150</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="One-Sheet Sales Sheet" data-price="150" id="service16">
                            <div class="service-details">
                                <label for="service16" class="service-name">One-Sheet Sales Sheet</label>
                                <p class="service-description">Polished one-page overview of your offer designed for PDFs, print, and email attachments</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$150</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Business Card Design" data-price="150" id="service17">
                            <div class="service-details">
                                <label for="service17" class="service-name">Business Card Design</label>
                                <p class="service-description">Custom business card layout using your logo, colors, and typography, delivered as print-ready files</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$150</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Letterhead Design" data-price="100" id="service18">
                            <div class="service-details">
                                <label for="service18" class="service-name">Letterhead Design</label>
                                <p class="service-description">Branded letterhead for print and PDF use with margins, header/footer, and typography styling</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$100</span>
                            </div>
                        </div>
                    </div>

                    <div class="service-item">
                        <div class="service-header">
                            <input type="checkbox" class="service-checkbox" data-service="Email Signature Design" data-price="75" id="service19">
                            <div class="service-details">
                                <label for="service19" class="service-name">Email Signature Design</label>
                                <p class="service-description">Clickable email signature layout with logo, contact info, and links for common email clients</p>
                                <span class="service-timeline">⏱️ Timeline: 1-3 days</span>
                            </div>
                            <div class="service-price">
                                <span class="price-label">Brandi Russell LLC</span>
                                <span class="price-amount">$75</span>
                            </div>
                        </div>
                    </div>
                </div>
            </form>

            <!-- Summary Section -->
            <div class="summary-section" id="summarySection" style="display:none;">
                <h3 class="summary-title">Your Estimated Cost</h3>
                <div class="summary-content">
                    <div class="summary-item">
                        <div class="summary-label">Services Selected</div>
                        <div class="summary-value" id="serviceCount">0</div>
                    </div>
                    <div class="summary-item">
                        <div class="summary-label">Estimated Total</div>
                        <div class="summary-value" id="totalCost">$0</div>
                    </div>
                    <div class="summary-item">
                        <div class="summary-label">Timeline Range</div>
                        <div class="summary-value" id="timelineRange">N/A</div>
                    </div>
                </div>
                <p style="margin: 0; opacity: 0.95; font-size: 0.95em;">
                    ✓ Review your selection above and contact Brandi to discuss project details and finalize your quote.
                </p>
            </div>

            <div class="no-selection" id="noSelection">
                <p>Select services above to see your estimated cost</p>
            </div>

            <!-- Action Buttons -->
            <div class="form-actions" style="margin-top: 30px;">
                <button type="button" class="btn-primary" id="copyBtn" style="display:none;">📋 Copy Quote to Clipboard</button>
                <button type="button" class="btn-secondary" id="contactBtn">💬 Contact Brandi</button>
                <button type="button" class="btn-reset" id="resetBtn">Reset Form</button>
            </div>

            <div class="contact-note">
                <p>Have questions? <a href="https://www.brandirussell.com" target="_blank">Visit Brandi's website</a> or reach out directly to discuss your project needs.</p>
            </div>
        </div>
    </div>

    <script>
        const form = document.getElementById('inquiryForm');
        const checkboxes = document.querySelectorAll('.service-checkbox');
        const summarySection = document.getElementById('summarySection');
        const noSelection = document.getElementById('noSelection');
        const serviceCountEl = document.getElementById('serviceCount');
        const totalCostEl = document.getElementById('totalCost');
        const timelineRangeEl = document.getElementById('timelineRange');
        const copyBtn = document.getElementById('copyBtn');
        const contactBtn = document.getElementById('contactBtn');
        const resetBtn = document.getElementById('resetBtn');
        const successMessage = document.getElementById('successMessage');

        // Timeline mapping
        const timelines = {
            'Brand Messaging': '2-3 days',
            'Brand Visual Identity': '4-5 days',
            'Custom Logo': '2 days',
            'LinkedIn Authority Accelerator': '2-3 days',
            'Classic Light Website': '5-7 days',
            'Advanced Core Website': '7-10 days',
            'Elite E-Commerce Business Site': '7-14 days',
            'Budget Website Landing Page': '1-3 days',
            'Additional Wix Website Pages': '1 day',
            'Additional Basic Website Pages': '1 day',
            'Custom Email Account': 'Per Year',
            'Flyer Design (single-sided)': '1-3 days',
            'Postcard Design': '1-3 days',
            'Brochure Design': '1-3 days',
            'Poster Design': '1-3 days',
            'One-Sheet Sales Sheet': '1-3 days',
            'Business Card Design': '1-3 days',
            'Letterhead Design': '1-3 days',
            'Email Signature Design': '1-3 days'
        };

        function updateSummary() {
            const selected = Array.from(checkboxes).filter(cb => cb.checked);
            
            if (selected.length === 0) {
                summarySection.style.display = 'none';
                noSelection.style.display = 'block';
                copyBtn.style.display = 'none';
                return;
            }

            noSelection.style.display = 'none';
            summarySection.style.display = 'block';
            copyBtn.style.display = 'inline-block';

            // Calculate totals
            let totalCost = 0;
            let selectedServices = [];
            let allTimelines = [];

            selected.forEach(checkbox => {
                const price = parseFloat(checkbox.dataset.price);
                const service = checkbox.dataset.service;
                totalCost += price;
                selectedServices.push(service);
                allTimelines.push(timelines[service]);
            });

            // Update display
            serviceCountEl.textContent = selected.length;
            totalCostEl.textContent = '$' + totalCost.toLocaleString();
            
            // Generate timeline range
            const uniqueTimelines = [...new Set(allTimelines)].join(', ');
            timelineRangeEl.textContent = uniqueTimelines || 'Varies';

            // Store selection for later use
            form.selectedServices = selectedServices;
            form.selectedTotal = totalCost;
            form.selectedTimelines = uniqueTimelines;
        }

        // Add event listeners to all checkboxes
        checkboxes.forEach(checkbox => {
            checkbox.addEventListener('change', updateSummary);
        });

        // Copy to clipboard functionality
        copyBtn.addEventListener('click', function() {
            const selected = Array.from(checkboxes).filter(cb => cb.checked);
            let quoteText = 'BRANDI RUSSELL - COST INQUIRY\n';
            quoteText += '================================\n\n';
            quoteText += 'Selected Services:\n';
            
            selected.forEach((checkbox, index) => {
                quoteText += (index + 1) + '. ' + checkbox.dataset.service + ' - $' + checkbox.dataset.price + '\n';
            });
            
            quoteText += '\n================================\n';
            quoteText += 'ESTIMATED TOTAL: $' + form.selectedTotal.toLocaleString() + '\n';
            quoteText += 'Timeline: ' + form.selectedTimelines + '\n';
            quoteText += '\nContact Brandi to finalize your quote.\n';
            quoteText += 'www.brandirussell.com';

            navigator.clipboard.writeText(quoteText).then(() => {
                copyBtn.textContent = '✓ Copied!';
                setTimeout(() => {
                    copyBtn.textContent = '📋 Copy Quote to Clipboard';
                }, 2000);
            });
        });

        // Contact button
        contactBtn.addEventListener('click', function() {
            window.open('https://www.brandirussell.com', '_blank');
        });

        // Reset form
        resetBtn.addEventListener('click', function() {
            checkboxes.forEach(checkbox => checkbox.checked = false);
            updateSummary();
            successMessage.style.display = 'none';
        });

        // Initialize
        updateSummary();
    </script>
</body>
</html>
