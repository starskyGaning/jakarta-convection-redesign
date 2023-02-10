<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
</script>

<section class="container-fluid customers-section">
    <div class="container d-flex flex-column align-items-center">
        <h1>Our Precious Clients</h1>
        <div class="d-flex flex-column flex-md-row logo-row">
            <img src="./images/clients-logos/garena-logo.svg" alt="garena logo">
            <img src="./images/clients-logos/pertamina-logo.svg" alt="pertamina logo">
            <img src="./images/clients-logos/shopee-logo.svg" alt="shopee logo">
            <img src="./images/clients-logos/tokopedia-logo.svg" alt="tokopedia logo">
        </div>
    </div>
</section>

<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    .customers-section{
        background-color: f.$secondary-300;
        .container{
            padding: 5rem 1rem;
            @include f.LG{
                padding: 8rem 0;
            }
            h1{
                @include f.header-1;
                color: f.$primary-300;
                margin-bottom: 3rem;
            }
            .logo-row{
                gap: 3rem;
                img{
                    max-width: 10rem;
                }
            }
        }
    }
</style>