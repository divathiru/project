# Project Responsive Web Design using Bootstrap
# Date:
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
Project.html
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&family=Roboto+Slab:wght@700&display=swap" rel="stylesheet">
    <style>
        .f1{
            font-family: 'Roboto Slab', serif;
            padding-left: 10px;
            margin-top: 27px;
        }
        
        body {
            background-color: #f8f9fa;
        }
        /* Card Styling */

        .card {
            border: none;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .card img {
    max-height: 180px;
    object-fit: cover;
    cursor: pointer;
    display: block;  /* Ensures the image is treated as a block element */
    width: 100%;     /* Ensure the image stretches across the available width */
    z-index: 1;      /* Ensure the image is rendered above other elements */
}

        .card:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        /* Fade-in Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s ease-out forwards;
        }
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        /* Gallery Title */
        .gallery-title {
            text-align: center;
            margin: 50px;
            font-weight: bold;
        }
        /* Pagination Styling */
        .pagination .page-link {
            color: #343a40;
        }
        .pagination .page-item.active .page-link {
            background-color: #343a40;
            border-color: #343a40;
            color: #fff;
        }
        .i1{
            height: 70px;
            width: 100%;
            background-size: cover;
            
        }
        .about-us {
            background-color: #fff;
            padding: 2rem;
            margin-top: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .about-us h2 {
            text-align: center;
            margin-bottom: 1rem;
        }
        .about-us p {
            text-align: justify;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-dark bg-dark">
        <div class="container d-flex justify-content-between align-items-center">
            <!-- Left Side -->
            <div class="d-flex">
                <a class="navbar-brand me-3" href="#">
                    <img src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Dribbble3_colored_svg-512.png" class="i1" />
                </a>
                <a class="nav-link text-light me-3 f1" href="#gallery">Gallery</a>
                <a class="nav-link text-light me-3 f1" href="#aboutUs">About Us</a>
            </div>
            
            <!-- Right Side -->
            <div>
                <a href="login.html" target="_blank"><button class="btn btn-outline-light" type="button">Login</button></a>
                <a href="signup.html" target="_blank"><button class="btn btn-outline-light" type="button">Sign Up</button></a>
            </div>
        </div>
    </nav>
    
    
    <!-- Gallery Title -->
     <header class="bg-white text-muted shadow pt-3 pb-2">
        <div class="gallery-title">
            <h2>Popular Shots Now</h2>
        </div>
    </header>

    <div class="container">
        <div id="gallery"  class="row g-4">
            <!-- Repeatable Card with Fade-in Animation -->
            <!-- Card 1 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in">
                <div class="card">
                    <img src="https://media.wired.com/photos/5fb70f2ce7b75db783b7012c/master/pass/Gear-Photos-597589287.jpg" class="i1">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 1</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 1</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 1,500 &nbsp; 👁️ 300
                        </p>
                    </div>
                </div>
            </div>
            
            <!-- Duplicate Cards -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 3</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 3</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,000 &nbsp; 👁️ 500
                        </p>
                    </div>
                </div>
            </div>
            <!-- Add more cards as needed -->
              <!-- Card 4 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 4</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 4</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 900 &nbsp; 👁️ 250
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 5 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 5</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 5</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 1,200 &nbsp; 👁️ 320
                        </p>
                    </div>
                </div>
            </div>
            <!-- Duplicate the same structure for additional cards -->
            <!-- Card 6 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 6</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 6</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,500 &nbsp; 👁️ 600
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 7-->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 6</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 7</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,800 &nbsp; 👁️ 690
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 8-->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 6</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 8</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,750 &nbsp; 👁️ 650
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 9</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 9</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 1,500 &nbsp; 👁️ 300
                        </p>
                    </div>
                </div>
            </div>
            <!-- Duplicate for Multiple Cards (Example: Cards 2-12) -->
            <!-- Card 2 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.2s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 10</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 10</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 1,700 &nbsp; 👁️ 450
                        </p>
                    </div>
                </div>
            </div>
            <!-- Duplicate Cards -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 11</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 11</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,000 &nbsp; 👁️ 500
                        </p>
                    </div>
                </div>
            </div>
            <!-- Add more cards as needed -->
              <!-- Card 4 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 12</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 12</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 900 &nbsp; 👁️ 250
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 5 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 13</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 13</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 1,200 &nbsp; 👁️ 320
                        </p>
                    </div>
                </div>
            </div>
            <!-- Duplicate the same structure for additional cards -->
            <!-- Card 6 -->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 14</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 14</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,500 &nbsp; 👁️ 600
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 7-->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 15</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 15</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,800 &nbsp; 👁️ 690
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 8-->
            <div class="col-md-4 col-sm-6 col-lg-3 fade-in" style="animation-delay: 0.4s;">
                <div class="card">
                    <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Placeholder">
                    <div class="card-body text-center">
                        <h5 class="card-title">Project 16</h5>
                        <p class="card-text text-muted">
                            <small>by Designer 16</small>
                        </p>
                        <p class="text-secondary">
                            ❤️ 2,750 &nbsp; 👁️ 650
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>



    <!-- Pagination -->
    <nav aria-label="Page navigation" class="mt-4">
        <ul class="pagination justify-content-center">
            <li class="page-item">
                <button class="page-link" id="prevButton" onclick="changePage(-1)" disabled>Previous</button>
            </li>
            <li class="page-item">
                <button class="page-link" id="nextButton" onclick="changePage(1)">Next</button>
            </li>
        </ul>
    </nav>    

    <!-- Lightbox Modal -->
    <div class="modal fade" id="lightboxModal" tabindex="-1" aria-labelledby="lightboxModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="lightboxModalLabel">Image Preview</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <img id="lightboxImage" src="" class="img-fluid w-100" alt="Enlarged Image">
                </div>
                <div class="modal-footer justify-content-between">
                    <button class="btn btn-secondary" onclick="navigateLightbox(-1)">Previous</button>
                    <button class="btn btn-secondary" onclick="navigateLightbox(1)">Next</button>
                </div>
            </div>
        </div>
    </div>
            <!-- About Us Section -->
            <div class="about-us" id="aboutUs">
                <style>
                    .about-us {
                        font-family: 'Raleway', sans-serif;
                        padding: 50px 20px;
                        background-color: #f8f9fa;
                        color: #333;
                        text-align: center;
                    }
                    .about-us h2 {
                        font-family: 'Roboto Slab', serif;
                        font-size: 2.5rem;
                        margin-bottom: 20px;
                        color: #000;
                    }
                    .about-us p {
                        font-size: 1.2rem;
                        line-height: 1.8;
                        margin-bottom: 20px;
                    }
                    .about-us img {
                        max-width: 100%;
                        height: auto;
                        border-radius: 10px;
                        margin-top: 30px;
                    }
                </style>
            
                <h2>About Us</h2>
                <p>
                    We are a team of passionate designers and developers who aim to bring the best design and creative work to the world. Our platform provides a space for designers to showcase their work, connect with like-minded creatives, and inspire others. We believe in the power of community and collaboration, and we are committed to supporting designers in their creative journey.
                </p>
                <p>
                    Our mission is to provide a platform that helps designers grow their networks, gain exposure, and elevate their work to new heights. Whether you are a graphic designer, UX/UI designer, or digital artist, Dribbble is the place to share your shots, receive feedback, and find inspiration for your next project.
                </p>
                <img src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" style="height: 500px;" alt="About Us Image">
            </div>
            
    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3 mt-4">
        <p>&copy; 2024 24005998 | Created with Bootstrap</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

    <script>
        const cardsData = {
            1: [
                { title: "Project 1", designer: "Arne Bivrin", likes: 1500, views: 300, imgSrc: "https://media.wired.com/photos/5fb70f2ce7b75db783b7012c/master/pass/Gear-Photos-597589287.jpg" },
                { title: "Project 2", designer: "Brad Winegar", likes: 1700, views: 450, imgSrc: "https://burst.shopifycdn.com/photos/beach-sunset-thailand.jpg?width=1000&format=pjpg&exif=0&iptc=0" },
                { title: "Project 3", designer: "Elena Mihailova", likes: 2000, views: 500, imgSrc: "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg" },
                { title: "Project 4", designer: "John Makris", likes: 900, views: 250, imgSrc: "https://cdn.pixabay.com/photo/2023/12/06/21/07/photo-8434386_1280.jpg" },
                { title: "Project 5", designer: "Franklin Neto", likes: 1200, views: 320, imgSrc: "https://c4.wallpaperflare.com/wallpaper/850/884/43/creative-pictures-bubbles-leaves-nature-plants-wallpaper-preview.jpg" },
                { title: "Project 6", designer: "Zuidema Renate", likes: 2500, views: 600, imgSrc: "https://www.photopills.com/sites/default/files/photopillers/benito-gaztelugatxe.jpg" },
                { title: "Project 7", designer: "Therese Asplund", likes: 2800, views: 690, imgSrc: "https://i.etsystatic.com/8073388/r/il/8e53f8/806908565/il_570xN.806908565_lyd0.jpg" },
                { title: "Project 8", designer: "Rares Besliu", likes: 2750, views: 650, imgSrc: "https://images.unsplash.com/photo-1542312940-2b6aaa1b28eb?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fHBob3RvZ3JhcGh5fGVufDB8fDB8fHww" },
            ],
            2: [
                { title: "Project 9", designer: "Anna Almen", likes: 1500, views: 300, imgSrc: "https://static.vecteezy.com/system/resources/thumbnails/047/576/896/small_2x/happy-yellow-ball-in-graffiticovered-alleyway-photo.jpg" },
                { title: "Project 10", designer: "Remuna Beca", likes: 1700, views: 450, imgSrc: "https://cdn.expertphotography.com/wp-content/uploads/2022/03/aesthetic-pictures-city-landscape.jpg" },
                { title: "Project 11", designer: "Massimo Giorgetta", likes: 2000, views: 500, imgSrc: "https://images.unsplash.com/photo-1509518408633-d42f618a2bdc?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                { title: "Project 12", designer: "Marta Losiewicz", likes: 900, views: 250, imgSrc: "https://images.unsplash.com/photo-1482190382612-7eb03c633035?q=80&w=1899&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                { title: "Project 13", designer: "Benny Chan", likes: 1200, views: 320, imgSrc: "https://images.unsplash.com/photo-1508423304245-0594de88eba4?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                { title: "Project 14", designer: "Giorgia Corniola", likes: 2500, views: 600, imgSrc: "https://images.unsplash.com/photo-1503753024571-3e39032c3807?q=80&w=1997&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                { title: "Project 15", designer: "Gea Strucks", likes: 2800, views: 690, imgSrc: "https://images.unsplash.com/photo-1510235444592-b8085c451b20?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                { title: "Project 16", designer: "Ben Connolly", likes: 2750, views: 650, imgSrc: "https://images.unsplash.com/photo-1510327073072-f898a7dbe0c2?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" },
                
            ]
        };
    
        let currentImageIndex = 0;
        const lightboxImages = [];
        let currentPage = 1;
        const totalPages = Object.keys(cardsData).length;
    
        function loadCards(page) {
            const gallery = document.getElementById('gallery');
            gallery.innerHTML = '';
    
            lightboxImages.length = 0;
    
            cardsData[page].forEach((card, index) => {
                lightboxImages.push(card.imgSrc);
                const cardHTML = `
                    <div class="col-md-4 col-sm-6 col-lg-3 fade-in">
                        <div class="card">
                            <img src="${card.imgSrc}" class="card-img-top" alt="${card.title}" onclick="openLightbox(${index})">
                            <div class="card-body text-center">
                                <h5 class="card-title">${card.title}</h5>
                                <p class="text-muted">by ${card.designer}</p>
                                <p>❤️ ${card.likes} 👁️ ${card.views}</p>
                            </div>
                        </div>
                    </div>
                `;
                gallery.insertAdjacentHTML('beforeend', cardHTML);
            });
        }
    
        function openLightbox(index) {
            currentImageIndex = index;
            document.getElementById('lightboxImage').src = lightboxImages[currentImageIndex];
            const lightboxModal = new bootstrap.Modal(document.getElementById('lightboxModal'));
            lightboxModal.show();
        }
    
        function navigateLightbox(step) {
            currentImageIndex = (currentImageIndex + step + lightboxImages.length) % lightboxImages.length;
            document.getElementById('lightboxImage').src = lightboxImages[currentImageIndex];
        }
    
        function changePage(direction) {
            currentPage += direction;
    
            // Disable buttons at boundaries
            document.getElementById('prevButton').disabled = currentPage === 1;
            document.getElementById('nextButton').disabled = currentPage === totalPages;
    
            // Load the new page
            loadCards(currentPage);
        }
    
        // Ensure the initial state
        document.getElementById('prevButton').disabled = currentPage === 1;
        document.getElementById('nextButton').disabled = currentPage === totalPages;
    
        // Initial load
        loadCards(currentPage);
    </script>
    
</body>
</html>

~~~
Login.html
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Login Page</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            background: #000;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #fff;
        }
        .card {
            border-radius: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            background: #fff;
            color: #000;
        }
        .card-header {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            text-align: center;
            font-size: 1.5rem;
            font-weight: bold;
            color: #000;
            background: #f8f9fa;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
        }
        .card-header img {
            width: 30px;
            height: 30px;
        }
        .btn-primary {
            background-color: #000;
            border: none;
            color: #fff;
        }
        .btn-primary:hover {
            background-color: #333;
        }
        .form-control:focus {
            box-shadow: none;
            border-color: #000;
        }
        .link:hover {
            text-decoration: underline;
            color: #000;
        }
        .text-center a {
            color: #000;
        }
        .text-center a:hover {
            text-decoration: underline;
            color: #000;
        }
    </style>
</head>
<body>
    <div class="card p-4" style="width: 22rem;">
        <div class="card-header">
            Login
        </div>
        <div class="card-body">
            <form>
                <div class="mb-3">
                    <label for="email" class="form-label">Email address</label>
                    <input type="email" class="form-control" id="email" placeholder="Enter your email" required>
                </div>
                <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input type="password" class="form-control" id="password" placeholder="Enter your password" required>
                </div>
                <div class="d-flex justify-content-between align-items-center">
                    <div>
                        <input type="checkbox" id="rememberMe">
                        <label for="rememberMe" class="form-label">Remember me</label>
                    </div>
                    <a href="#" class="text-decoration-none link">Forgot Password?</a>
                </div>
                <button type="submit" class="btn btn-primary w-100 mt-3">Login</button>
            </form>
        </div>
        <div class="text-center mt-3">
            <span>Don't have an account? <a href="signup.html" target="_blank" class="text-decoration-none link">Sign Up</a></span>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
~~~
Sigunp.html
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Sign Up Page</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            background: #000;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #fff;
        }
        .card {
            border-radius: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            background: #fff;
            color: #000;
        }
        .card-header {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            text-align: center;
            font-size: 1.5rem;
            font-weight: bold;
            color: #000;
            background: #f8f9fa;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
        }
        .card-header img {
            width: 30px;
            height: 30px;
        }
        .btn-primary {
            background-color: #000;
            border: none;
            color: #fff;
        }
        .btn-primary:hover {
            background-color: #333;
        }
        .form-control:focus {
            box-shadow: none;
            border-color: #000;
        }
        .link:hover {
            text-decoration: underline;
            color: #000;
        }
        .text-center a {
            color: #000;
        }
        .text-center a:hover {
            text-decoration: underline;
            color: #000;
        }
    </style>
</head>
<body>
    <div class="card p-4" style="width: 22rem;">
        <div class="card-header">
            Sign Up
        </div>
        <div class="card-body">
            <form>
                <div class="mb-3">
                    <label for="fullName" class="form-label">Full Name</label>
                    <input type="text" class="form-control" id="fullName" placeholder="Enter your full name" required>
                </div>
                <div class="mb-3">
                    <label for="email" class="form-label">Email address</label>
                    <input type="email" class="form-control" id="email" placeholder="Enter your email" required>
                </div>
                <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input type="password" class="form-control" id="password" placeholder="Enter your password" required>
                </div>
                <div class="mb-3">
                    <label for="confirmPassword" class="form-label">Confirm Password</label>
                    <input type="password" class="form-control" id="confirmPassword" placeholder="Confirm your password" required>
                </div>
                <button type="submit" class="btn btn-primary w-100 mt-3">Sign Up</button>
            </form>
        </div>
        <div class="text-center mt-3">
            <span>Already have an account? <a href="login.html" target="_blank" class="text-decoration-none link">Login</a></span>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
~~~
# OUTPUT:
![Screenshot 2024-12-20 105641](https://github.com/user-attachments/assets/0fb9624f-50c9-4f49-98f4-5184c3565016)

![Screenshot 2024-12-20 105654](https://github.com/user-attachments/assets/f4d4b76e-d0d5-43a0-a91a-f5aa542d6d5e)

![Screenshot 2024-12-20 105713](https://github.com/user-attachments/assets/1b3924f3-996b-4f93-8acd-6ae8baa34a57)

![Screenshot 2024-12-20 105730](https://github.com/user-attachments/assets/8bcda529-ff92-4702-94d9-13d31a8950a8)

![Screenshot 2024-12-20 105802](https://github.com/user-attachments/assets/5fad1aa3-9be6-41f0-9ee7-7334fbee9f0b)

![Screenshot 2024-12-20 105826](https://github.com/user-attachments/assets/058700f0-cbe7-4052-add0-18396f029742)

![Screenshot 2024-12-20 105851](https://github.com/user-attachments/assets/1dcf59d7-8019-47c7-9cce-3dc29d731dc4)

![Screenshot 2024-12-20 105952](https://github.com/user-attachments/assets/e0598222-ca70-42e6-9958-3d52e6a37492)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
