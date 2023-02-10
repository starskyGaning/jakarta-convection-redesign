<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
</script>

<section class="container-fluid about-section">
    <div class="container d-flex flex-column">
        <div class="d-flex flex-column upper-section align-items-start">
            <div class="d-flex flex-column align-items-start">
                <h1>A little bit about us</h1>
                <p>Jakarta Convection is an industrial-class garment maker that excels in all types of garment, starting from casual everyday shirts to customized uniforms.</p>
            </div>
        </div>
        <div class="d-flex flex-column bottom-section align-items-end">
            <div class="d-flex flex-column align-items-start">
                <h1>Why us?</h1>
                <p>Jakarta Convection has more than 10+ years of experience in handling different types of request, with different materials, colors, styling, etc.</p>
                <p>We’ve also obtained partnerships with various companies as their exclusive uniform maker, pretty sure that speaks volume in itself.</p>
            </div>
        </div>
    </div>
</section>

<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    .about-section{
        background-color: f.$secondary-300;
        .container{
            padding: 7rem 1rem;
            @include f.LG{
                padding: 10rem 0;
            }
            h1{
                @include f.display-3;
                color: f.$primary-300;
                margin-bottom: 1.5rem;
            }
            p{
                @include f.header-1;
                color: f.$primary-300;
                max-width: 710px;
            }
        }
    }

    .upper-section{
        margin-bottom: 5rem;
        @include f.LG{
            margin-bottom: 12rem;
        }
    }

    .bottom-section{
        p{
            margin-bottom: 1.5rem;
            @include f.LG{
                margin-bottom: 2rem;
            }
        }
    }

</style>