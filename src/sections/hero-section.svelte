<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
    // Anime JS
    import anime from 'animejs/lib/anime.es.js';
    // Svelte OnMount
    import { onMount } from 'svelte';

    // AnimeJS Animation on Company Logo
    onMount(() => {
        anime({
            targets : ".animated-logo",
            rotate: 360,
            duration: 5000,
            easing: 'cubicBezier(.5, .5, .5, .5)',
            loop: true,
        })
    })

</script>

<section class="container-fluid hero-section">
    <div class="container d-flex flex-column">
        <div class="d-flex flex-row upper-section">
            <figure class="quote">
                <blockquote>
                    Style is something each of us already has, all we need to do is find it.
                </blockquote>
                <figcaption>
                    &mdash; Diane von Furstenberg
                </figcaption>
            </figure>
        </div>
        <div class="d-flex flex-column align-items-center bottom-section">
            <p class="text-center">Jakarta Convection has all you need to unleashed your imagination into your fashion style</p>
            <img src="./images/company-name.svg" alt="company name svg" class="animated-logo">
        </div>
    </div>
</section>

<style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    .hero-section{
        background-color: f.$secondary-300;
        .container{
            padding: 4rem 1rem;
            @include f.MD{
                padding: 8rem 0;
            }
        }
    }

    .upper-section{
        margin-bottom: 6rem;
        @include f.LG{
            margin-bottom: 8rem
        }
        blockquote{
            @include f.display-1;
            color: f.$primary-300;
            max-width: 1075px;
        }
        figcaption{
            @include f.display-2;
            color: f.$primary-300;
        }
    }

    .bottom-section{
        p{
            @include f.header-1;
            color: f.$primary-300;
            max-width: 870px;
            margin-bottom: 7rem;
            @include f.LG{
                margin-bottom: 9rem;
            }
        }
        img{
            max-width: 11rem;
        }
    }
</style>