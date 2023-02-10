<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
</script>

<section class="container-fluid blog-section">
    <div class="container d-flex flex-column align-items-center">
        <h1 class="blog-heading">Blog Section</h1>
        <div class="d-flex flex-column blogs-column">
            <div class="d-flex flex-column flex-md-row blogs-row">
                <div class="position-relative blog-card">
                    <img src="./images/blog-section-images/blog-image-1.webp" alt="">
                    <div class="position-absolute card-overlay">
                        <div class="d-flex flex-column align-items-start overlay-content">
                            <h1>Some title</h1>
                            <p>Some text to fill in the void inside this blog card</p>
                            <a href="/">Read more</a>
                        </div>
                    </div>
                </div>
                <div class="position-relative blog-card">
                    <img src="./images/blog-section-images/blog-image-2.webp" alt="">
                    <div class="position-absolute card-overlay">
                        <div class="d-flex flex-column align-items-start overlay-content">
                            <h1>Some title</h1>
                            <p>Some text to fill in the void inside this blog card</p>
                            <a href="/">Read more</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="d-flex flex-column flex-md-row blogs-row">
                <div class="position-relative blog-card">
                    <img src="./images/blog-section-images/blog-image-3.webp" alt="">
                    <div class="position-absolute card-overlay">
                        <div class="d-flex flex-column align-items-start overlay-content">
                            <h1>Some title</h1>
                            <p>Some text to fill in the void inside this blog card</p>
                            <a href="/">Read more</a>
                        </div>
                    </div>
                </div>
                <div class="position-relative blog-card">
                    <img src="./images/blog-section-images/blog-image-4.webp" alt="">
                    <div class="position-absolute card-overlay">
                        <div class="d-flex flex-column align-items-start overlay-content">
                            <h1>Some title</h1>
                            <p>Some text to fill in the void inside this blog card</p>
                            <a href="/">Read more</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    .blog-section{
        background-color: f.$secondary-300;
        .container{
            padding: 8rem 1rem;
            @include f.MD{
                padding: 13rem 0;
            }
            .blog-heading{
                @include f.display-2;
                color: f.$primary-300;
                margin-bottom: 4rem;
                @include f.MD{
                    margin-bottom: 5rem;
                }
            }
        }
    }

    .blogs-column{
        gap: 5rem;
        .blogs-row{
            gap: 5rem;
        }
    }

    .blog-card{
        max-width: 550px;
        img{
            width: 100%;
        }
        .card-overlay{
            padding: 1.5rem;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            height: 100%;
            width: 100%;
            opacity: 0;
            transition: .5s ease;
            background-color: f.$secondary-500;
            .overlay-content{
                h1{
                    @include f.header-1;
                    color: f.$primary-300;
                    margin-bottom: .5rem;
                }
                p{
                    @include f.header-2;
                    color: f.$primary-400;
                    max-width: 300px;
                }
                a{
                    @include f.header-3;
                    background-color: f.$primary-300;
                    color: f.$secondary-300;
                    text-decoration: none;
                    padding: 1rem 2rem;
                    transition: color 500ms ease;
                }
                a:hover{
                    background-color: f.$secondary-300;
                    color: f.$secondary-50;
                }
            }
        }
        .card-overlay:hover{
            opacity: 1;
        }
    }

</style>