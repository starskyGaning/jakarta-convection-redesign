<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
    // Bootstrap Icons
    import 'bootstrap-icons/font/bootstrap-icons.css';
</script>

<footer class="container-fluid">
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-3 d-flex flex-column footers-column socials-column">
                <h2>Socials</h2>
                <div class="d-flex flex-row socials-row">
                    <a href="/"><i class="bi bi-envelope"></i></a>
                    <a href="/"><i class="bi bi-instagram"></i></a>
                    <a href="/"><i class="bi bi-whatsapp"></i></a>
                    <a href="/"><i class="bi bi-linkedin"></i></a>
                </div>
            </div>
            <div class="col-12 col-md-3 footers-column address-column">
                <h2>Address</h2>
                <div class="d-flex flex-column">
                    <p>Kirasyihun Road</p>
                    <p>Doyong Village</p>
                    <p>Alam Jaya</p>
                    <p>Tangerang City</p>
                </div>
            </div>
            <div class="col-12 col-md-3 footers-column hours-column">
                <h2>Operational Hours</h2>
                <div class="d-flex flex-column">
                    <p>Monday - Friday</p>
                    <p>09.00 - 17.00</p>
                    <p>Saturday</p>
                    <p>09.00 - 15.00</p>
                    <p>Sunday</p>
                    <p>Closed</p>
                </div>
            </div>
            <div class="col-12 col-md-3 footers-column customer-column">
                <h2>Customer Support</h2>
                <div class="d-flex flex-column">
                    <a href="/">Size Chart</a>
                    <a href="/">How To Order</a>
                    <a href="/">Available Materials & Colors</a>
                    <a href="/">Disclaimer</a>
                    <a href="/">Privacy Policy</a>
                    <a href="/">Sitemap</a>
                </div>
            </div>
            <div class="col-12 d-flex flex-column align-items-center footers-column creator-column">
                <p>Made by <a href="https://www.linkedin.com/in/starsky-ganing" target="_blank" rel="noreferrer">Starsky Ganing</a></p>
            </div>
        </div>
    </div>
</footer>

<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    footer{
        background-color: f.$primary-300;
        .container{
            padding: 2rem 1rem;
            @include f.LG{
                padding: 2rem 0;
            }
            h2{
                @include f.header-3;
                margin-bottom: .5rem;
                @include f.LG{
                    margin-bottom: 1rem;
                }
            }
            p{
                @include f.body;
                color: f.$secondary-400;
            }
            a{
                @include f.body;
                color: f.$secondary-300;
            }
        }
    }

    .footers-column{
        margin: 1.5rem 0;
        @include f.LG{
            margin: 1rem 0;
        }
    }

    .socials-row{
        gap: 1rem;
        .bi{
            font-size: 1.5rem;
            transition: color 800ms ease;
            @include f.LG{
                font-size: 2rem;
            }
        }
        .bi:hover{
            color: f.$primary-500;
        }
    }

    .address-column p, .hours-column p{
        margin-bottom: .5rem;
    }

    .customer-column a{
        margin-bottom: .5rem;
        transition: color 800ms ease;
    }
    .customer-column a:hover{
        color: f.$primary-500;
    }

    .creator-column{
        a{
            transition: color 800ms ease;
        }
        a:hover{
            color: f.$primary-500;
        }
    }
</style>