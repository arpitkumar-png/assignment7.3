HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.3 — Responsive Product Listing</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="listing-style.css">
</head>
<body>

    <!-- Header -->
    <header class="page-header">
        <h1>Tech Accessories Store</h1>
        <p>Explore our catalog of 6 responsive product cards built with Flexbox wrapping.</p>
    </header>

    <main class="main-container">
        
        <!-- --- 1, 3, 4, 5, 6. Flexbox Product Container (6 Cards) --- -->
        <section class="product-grid">
            
            <!-- Product 1 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=300&auto=format&fit=crop&q=80" alt="Minimalist Watch">
                </div>
                <div class="product-info">
                    <h2>Minimalist Watch</h2>
                    <p class="price">$120.00</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

            <!-- Product 2 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=300&auto=format&fit=crop&q=80" alt="Wireless Headphones">
                </div>
                <div class="product-info">
                    <h2>Wireless Headphones</h2>
                    <p class="price">$199.99</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

            <!-- Product 3 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=300&auto=format&fit=crop&q=80" alt="Running Sneakers">
                </div>
                <div class="product-info">
                    <h2>Running Sneakers</h2>
                    <p class="price">$89.50</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

            <!-- Product 4 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1583394838336-acd977736f90?w=300&auto=format&fit=crop&q=80" alt="Gaming Headset">
                </div>
                <div class="product-info">
                    <h2>Gaming Headset</h2>
                    <p class="price">$149.00</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

            <!-- Product 5 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?w=300&auto=format&fit=crop&q=80" alt="Vintage Camera">
                </div>
                <div class="product-info">
                    <h2>Vintage Camera</h2>
                    <p class="price">$350.00</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

            <!-- Product 6 -->
            <article class="product-card">
                <div class="product-img-box">
                    <img src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?w=300&auto=format&fit=crop&q=80" alt="Smart Fitness Band">
                </div>
                <div class="product-info">
                    <h2>Smart Fitness Band</h2>
                    <p class="price">$59.99</p>
                    <button class="buy-btn">Add to Cart</button>
                </div>
            </article>

        </section>

    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Tech Accessories Store. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: listing-style.css
CSS
/* --- Global Reset & Typography --- */
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
}

/* --- Page Header --- */
.page-header {
    background-color: #0f172a;
    color: #ffffff;
    text-align: center;
    padding: 3rem 1rem;
}

.page-header h1 {
    font-size: 2.2rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    color: #94a3b8;
}

/* --- Main Container --- */
.main-container {
    max-width: 1200px;
    margin: 3rem auto;
    padding: 0 1.5rem;
}

/* ==========================================
   PRODUCT GRID CONTAINER (Flexbox Wrapping)
   ================================---------- */
.product-grid {
    display: flex;                  /* 3. Enable Flexbox */
    flex-wrap: wrap;                /* 3 & 6. Allow cards to wrap to next line on smaller screens */
    justify-content: center;        /* Center items horizontally in container */
    gap: 2rem;                      /* 4. Add consistent spacing between cards */
}

/* ==========================================
   INDIVIDUAL PRODUCT CARD
   ================================---------- */
.product-card {
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.03);
    
    /* 5. Flex Properties: flex-grow, flex-shrink, flex-basis */
    flex: 1 1 280px;                /* Grows, shrinks, and has a base width of 280px */
    max-width: 320px;               /* Prevents cards from stretching too wide on large screens */
    
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.product-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.08);
}

/* Product Image Box */
.product-img-box {
    width: 100%;
    height: 200px;
    background-color: #f1f5f9;
}

.product-img-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* Product Information Content */
.product-info {
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    flex-grow: 1;                   /* Fills available card space evenly */
    justify-content: space-between;
}

.product-info h2 {
    font-size: 1.15rem;
    color: #1e293b;
    margin-bottom: 0.5rem;
}

.price {
    font-size: 1.1rem;
    font-weight: 700;
    color: #2563eb;
    margin-bottom: 1.25rem;
}

/* Buy Button */
.buy-btn {
    width: 100%;
    padding: 0.75rem;
    background-color: #0f172a;
    color: #ffffff;
    font-size: 0.95rem;
    font-weight: 600;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.buy-btn:hover {
    background-color: #2563eb;
}

/* --- Footer --- */
footer {
    text-align: center;
    padding: 2rem;
    background-color: #0f172a;
    color: #94a3b8;
    font-size: 0.9rem;
    margin-top: 4rem;
}