<script>
    // Bootstrap Minified CSS
    import 'bootstrap/dist/css/bootstrap.min.css';
    // Bootstrap Minified JS
    import 'bootstrap/dist/js/bootstrap.min.js';
</script>

<nav class="container-fluid navbar navbar-expand-lg bg-body-tertiary">
    <div class="container">
      <a class="navbar-brand" href="/"><img src="./images/company-logo.svg" alt="company logo"></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="/">Home</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="/" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Products
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="/">T-Shirt</a></li>
              <li><a class="dropdown-item" href="/">Polo Shirt</a></li>
              <li><a class="dropdown-item" href="/">Uniforms</a></li>
              <li><a class="dropdown-item" href="/">Jacket & Hoodie</a></li>
              <li><a class="dropdown-item" href="/">Apron</a></li>
              <li><a class="dropdown-item" href="/">Hats</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact-section">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <style lang="scss">
    @use '../foundations/foundations-compiler' as f;

    nav{
        background-color: f.$primary-300;
        .container{
            padding: 1rem;
            @include f.MD{
                padding: 1rem 0;
            }
        }
    }

    .navbar-brand{
        img{
            transition: opacity 800ms ease;
            width: 10rem;
            @include f.LG{
              width: 12rem;
            }
        }
        img:hover{
            opacity: .5;
        }
    }

    .navbar-nav{
        margin-top: 1rem;
        @include f.LG{
            margin-top: 0;
        }
        .nav-item{
            margin: .5rem;
            @include f.LG{
              margin: 0 1rem;
            }
            .nav-link{
                @include f.header-3;
                color: f.$secondary-300;
                transition: color 800ms ease;
            }
            .nav-link:hover{
                color: f.$secondary-200;
            }
        }
    }

    .dropdown-menu{
        background-color: f.$primary-300;
        .dropdown-item{
            @include f.header-3;
            margin: .5rem 0;
            padding: .5rem 1rem;
        }
        .dropdown-item:hover{
            background-color: f.$secondary-300;
            color: f.$secondary-50;
        }
    }

  </style>