The HTML File (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pricing Cards & Centered Login Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- ================= SECTION 1: PRICING CARDS ================= -->
    <section class="pricing-section">
        <header class="section-header">
            <h1>Choose Your Plan</h1>
            <p>Flexible options designed to scale with your projects.</p>
        </header>

        <!-- Steps 1, 2, 3, & 4: Flexbox Container for Pricing Cards -->
        <div class="pricing-container">
            
            <!-- Basic Card -->
            <div class="card">
                <h3>Basic</h3>
                <p class="price">$9<span>/mo</span></p>
                <ul class="features-list">
                    <li>1 Website Project</li>
                    <li>Basic Analytics</li>
                    <li>Community Support</li>
                </ul>
                <button class="btn">Choose Basic</button>
            </div>

            <!-- Pro Card (Featured) -->
            <div class="card card-featured">
                <span class="badge">Popular</span>
                <h3>Pro</h3>
                <p class="price">$29<span>/mo</span></p>
                <ul class="features-list">
                    <li>5 Website Projects</li>
                    <li>Advanced Analytics</li>
                    <li>Priority Email Support</li>
                </ul>
                <button class="btn btn-accent">Choose Pro</button>
            </div>

            <!-- Premium Card -->
            <div class="card">
                <h3>Premium</h3>
                <p class="price">$59<span>/mo</span></p>
                <ul class="features-list">
                    <li>Unlimited Projects</li>
                    <li>Real-Time Analytics</li>
                    <li>24/7 Dedicated Support</li>
                </ul>
                <button class="btn">Choose Premium</button>
            </div>

        </div>
    </section>

    <hr class="divider">

    <!-- ================= SECTION 2: CENTERED LOGIN FORM ================= -->
    <!-- Steps 5 & 6: Centering horizontally & vertically using flexbox -->
    <section class="login-section">
        <div class="login-card">
            <h2>Welcome Back</h2>
            <p class="login-subtitle">Please enter your account details.</p>
            
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" placeholder="name@example.com" required>
                </div>
                
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" name="password" placeholder="••••••••" required>
                </div>

                <button type="submit" class="btn btn-accent btn-full">Sign In</button>
            </form>
        </div>
    </section>

</body>
</html>
2. The CSS File (style.css)
CSS
/* Global Reset & Typography */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
    padding: 40px 20px;
}

/* ================= SECTION 1 STYLING: PRICING CARDS ================= */
.pricing-section {
    max-width: 1100px;
    margin: 0 auto 60px auto;
}

.section-header {
    text-align: center;
    margin-bottom: 40px;
}

.section-header h1 {
    font-size: 2.25rem;
    color: #0f172a;
    margin-bottom: 8px;
}

.section-header p {
    color: #64748b;
}

/* Step 3 & 4: Flexbox Container and Alignment for Pricing Cards */
.pricing-container {
    display: flex;
    justify-content: center; /* Centers cards horizontally */
    align-items: stretch;    /* Ensures cards stretch to equal height */
    gap: 30px;               /* Consistent spacing between cards */
    flex-wrap: wrap;         /* Allows cards to wrap nicely on smaller screens */
}

/* Base Card Styling */
.card {
    position: relative;
    background-color: #ffffff;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
    padding: 30px;
    width: 100%;
    max-width: 320px;
    display: flex;
    flex-direction: column; /* Step 6: Stack content vertically inside card */
    justify-content: space-between;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

/* Featured Card Modifier */
.card-featured {
    border-color: #3b82f6;
    box-shadow: 0 10px 20px -3px rgba(59, 130, 246, 0.15);
}

.badge {
    position: absolute;
    top: -12px;
    right: 20px;
    background-color: #3b82f6;
    color: white;
    font-size: 0.75rem;
    font-weight: bold;
    padding: 4px 12px;
    border-radius: 20px;
    text-transform: uppercase;
}

.card h3 {
    font-size: 1.5rem;
    color: #0f172a;
    margin-bottom: 15px;
}

.price {
    font-size: 2.5rem;
    font-weight: 800;
    color: #0f172a;
    margin-bottom: 20px;
}

.price span {
    font-size: 1rem;
    font-weight: 400;
    color: #64748b;
}

.features-list {
    list-style: none;
    margin-bottom: 30px;
    flex-grow: 1; /* Pushes button to bottom of card */
}

.features-list li {
    padding: 8px 0;
    color: #475569;
    border-bottom: 1px solid #f1f5f9;
}

/* Button Styles */
.btn {
    background-color: #f1f5f9;
    color: #1e293b;
    border: none;
    padding: 12px;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.2s;
}

.btn:hover {
    background-color: #e2e8f0;
}

.btn-accent {
    background-color: #3b82f6;
    color: white;
}

.btn-accent:hover {
    background-color: #2563eb;
}

.btn-full {
    width: 100%;
}

.divider {
    border: none;
    border-top: 1px solid #cbd5e1;
    max-width: 800px;
    margin: 60px auto;
}

/* ================= SECTION 2 STYLING: CENTERED LOGIN FORM ================= */
/* Step 5: Center the login form horizontally and vertically using Flexbox */
.login-section {
    display: flex;
    justify-content: center; /* Center horizontally */
    align-items: center;     /* Center vertically */
    min-height: 60vh;        /* Generous viewport space */
}

.login-card {
    background-color: #ffffff;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
    padding: 40px;
    width: 100%;
    max-width: 400px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}

.login-card h2 {
    font-size: 1.75rem;
    color: #0f172a;
    margin-bottom: 6px;
}

.login-subtitle {
    color: #64748b;
    font-size: 0.9rem;
    margin-bottom: 24px;
}

.form-group {
    display: flex;
    flex-direction: column; /* Step 6: Stack label and input vertically */
    gap: 6px;
    margin-bottom: 20px;
}

.form-group label {
    font-size: 0.875rem;
    font-weight: 600;
    color: #1e293b;
}

.form-group input {
    padding: 10px 14px;
    border: 1px solid #cbd5e1;
    border-radius: 6px;
    font-size: 1rem;
    font-family: inherit;
}

.form-group input:focus {
    outline: none;
    border-color: #3b82f6;
    box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.15);
}