<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
</svelte:head>
<script lang="js">
    import {
    Image,
    Button,
    Collapse,
    NavbarToggler,
    NavbarBrand,
    Nav,
    Navbar,
    NavItem,
    NavLink,
    Dropdown,
    DropdownToggle,
    DropdownMenu,
    DropdownItem,
    Card,
    CardBody,
    CardFooter,
    CardHeader,
    CardSubtitle,
    CardText,
    CardTitle
  } from '@sveltestrap/sveltestrap';

  let isOpen = false;

  function handleUpdate(event) {
    isOpen = event.detail.isOpen;
  }
  function changeOpened(){
    isOpen = !isOpen
  }
</script>
<style>
    main,footer{
        padding: 5% 10% ;
    }
    section{
        height: 500px;
        background: url("https://open.lutsk.ua/wp-content/uploads/2019/10/youth-center-1024x600.jpg");
        background-size: cover;
    }
</style>
  
  <Navbar dark=true style="width:100%;position: fixed;z-index:1000;background:linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,11,91,1) 23%, rgba(0,212,255,1) 100%);" light expand="md" container="md">
    <NavbarBrand style="width:7%;word-wrap:normal" href="/"><Image style="width:50px; margin:0 10px; 0 0" alt="logo" src="/favicon.png"/>Sveltestrap template</NavbarBrand>
    <NavbarToggler style="width:10%;" on:click={changeOpened} />
        <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
          <Nav class="ms-auto" navbar>
            <NavItem>
              <NavLink href="/">Main</NavLink>
            </NavItem>
            <NavItem>
              <NavLink href="/news/">News</NavLink>
            </NavItem>
            <NavItem>
              <NavLink href="/about/">About</NavLink>
            </NavItem>
          </Nav>
        </Collapse>
  
  </Navbar>
  
<section style="font-size:xxx-large;padding:100px 10%;justify-content:right;align-items:center;display:flex;color:white;">
<span style="text-shadow:black 3px -3px 5px">Activize our <br>Svetestrap!</span>
</section>
<main style="word-wrap:break-word;color:white;background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(46,63,185,1) 13%, rgba(123,234,255,1) 100%);">
    <slot/>
</main>
<footer style="background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,11,91,1) 23%, rgba(0,212,255,1) 100%); color:white">
    <h2>Zone of Bootstrap and <span style="color:yellowgreen">Svelte</span></h2>
    <h6><a href="mailto:vladceresna6@gmail.com">vladceresna6@gmail.com</h6>
    <h6>Copyright © Vlad Ĉereŝna, 2023</h6>
</footer>