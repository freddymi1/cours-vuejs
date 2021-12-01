<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light" id="sticky-nav">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">{{title}}</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#home">Home</a>
            </li>
          </ul>

          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="btn" aria-current="page" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    props:{
        title: String
    }
}
</script>

<style scoped>
    .navbar {
        position: relative;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
        padding-top: 1rem;
        padding-bottom: 1rem;
    }

    /* .sticky-nav {
        top: 3rem;
        background: #323a45e7;
        width: 90%;
        margin: auto;
        position: relative !important;
        padding: 1rem!important;
        z-index: 1;
        margin: auto !important;
        order: 0;
        border: 2px solid #1490af60;
        border-radius: 10px;
        box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.2);
    } */

    .btn{
        background: #1490af !important;
        border: none !important;
        border-radius: 20px !important;
        font-weight: 600 !important;
        transition: all .3s ease;
        color: #fff;
    }
    .btn:hover{
        background: #08708a !important;
        color: #fff;
    }
</style>