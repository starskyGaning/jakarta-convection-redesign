<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
    // Bootstrap Icons
    import 'bootstrap-icons/font/bootstrap-icons.css';
</script>

<section class="container-fluid contact-section" id="contact-section">
    <div class="container d-flex flex-column align-items-start">
        <h1>Contact Us</h1>
        <p>Feel free to contact us if you have any questions regarding our services.</p>
        <p>You can contact us through one of these channels below.</p>
        <div class="d-flex flex-row socials-row">
            <a href="/"><i class="bi bi-instagram"></i></a>
            <a href="/"><i class="bi bi-whatsapp"></i></a>
            <a href="/"><i class="bi bi-linkedin"></i></a>
        </div>
        <h2>Or</h2>
        <a href="/" class="btn">Email Us</a>
    </div>
</section>


<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    .contact-section{
        background-color: f.$secondary-300;
        .container{
            padding: 5rem 1rem;
            @include f.LG{
                padding: 10rem 0;
            }
            h1{
                @include f.display-3;
                color: f.$primary-300;
                margin-bottom: 1.5rem;
                @include f.LG{
                    margin-bottom: 2rem;
                }
            }
            p{
                @include f.header-1;
                color: f.$primary-400;
                max-width: 625px;
                margin-bottom: 1.5rem;
            }
            .socials-row{
                gap: 2rem;
                margin-bottom: 1.5rem;
                @include f.LG{
                    margin-bottom: 2rem;
                }
                .bi{
                    font-size: 2.5rem;
                    color: f.$primary-300;
                    transition: color 800ms ease;
                    @include f.LG{
                        font-size: 3.5rem;
                    }
                }
                .bi:hover{
                    color: f.$primary-50;
                }
            }
            h2{
                @include f.display-2;
                color: f.$primary-300;
                margin-bottom: 1.5rem;
                @include f.LG{
                    margin-bottom: 2rem;
                }
            }
            .btn{
                @include f.header-1;
                background-color: f.$secondary-500;
                color: f.$primary-300;
                padding: 1rem 4rem;
                transition: background-color 800ms ease;
            }
            .btn:hover{
                background-color: f.$secondary-200;
            }
        }
    }
</style>
