<script lang="ts">
import "../app.css";
import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Footer, FooterBrand, FooterCopyright, FooterIcon, FooterLink, FooterLinkGroup  } from 'flowbite-svelte';
import logoIcon from "$lib/images/logo.svg";
import { DarkMode } from 'flowbite-svelte';
</script>

<Navbar>
    <NavBrand href="/">
      <img src={logoIcon} class="me-3 h-6 sm:h-9" alt="Logo" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Portfolio</span>
    </NavBrand>
    <NavHamburger  />
    <NavUl>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/docs/components/navbar">Navbar</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
    <DarkMode />
  </Navbar>
<slot>
</slot>

<Footer>
    <div class="sm:flex sm:items-center sm:justify-between">
    <FooterCopyright href="/" by="Andreas Changa Network™" year={2024} />
    <FooterLinkGroup ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
      <FooterLink href="/">About</FooterLink>
      <FooterLink href="/">Privacy Policy</FooterLink>
      <FooterLink href="/">Licensing</FooterLink>
      <FooterLink href="/">Contact</FooterLink>
    </FooterLinkGroup>
    </div>
  </Footer>