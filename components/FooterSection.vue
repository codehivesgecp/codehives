<template>
  <div class="footer">
    <Container class="contents">
      <div class="content-grid">
        <div class="panel">
          <div class="branding">
           
</div>
        </div>

        <!-- ]<div class="panel">
          <h4 class="title">About</h4>
          <a
            rel="noopener noreferrer"
            target="_blank"
            href="https://static.mlh.io/docs/mlh-code-of-conduct.pdf"
            >Code Of Conduct</a
          >
          <a rel="noopener noreferrer" target="_blank" href="/blog"
            >Season 1 Blog</a
          >
          <a rel="noopener noreferrer" target="_blank" href="/team"
            >Know The Team</a
          > -->
          <!-- <a rel="noopener noreferrer" target="_blank" href="/schedule"
            >Schedule</a
          > 

        </div>

      -->
        <div class="panel">
          <h4 class="title">Explore</h4>
          <a href="/events">Events</a>
           <a href="/joining">Joining</a> 
          <a href="/registration">Registration</a>
          <a href="/teams">Teams</a>
                  </div>
 
        <div class="panel">
          <h4 class="title">Find Us Online</h4>
         <!--  <img class="img" src="~/assets/logo2.png" />
 -->          <div class="socialLinks" id="socailLinks">
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="https://discord.com/invite/8nYw3P5Js8"
            >
            <img src="~/assets/Socials/discord.svg" alt="discord" />
           </a>
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="https://twitter.com/code_hives"
            >
              <img src="~/assets/Socials/twitter.svg" alt="twitter" />
            </a>
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="https://www.instagram.com/code.hives/"
            >
              <img src="~/assets/Socials/instagram.svg" alt="instagram" />
            </a>
          </div>
          <div class="socialLinks">
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="https://www.youtube.com/"
            >
              <img src="~/assets/Socials/youtube.svg" alt="youtube" />
            </a>
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="mailto:code.hives@gecpatan.ac.in"
            >
              <img src="~/assets/Socials/mail.svg" alt="email" />
            </a>
            <a
              class="smooth-transition"
              rel="noopener noreferrer"
              target="_blank"
              href="https://www.linkedin.com/in/code-hives-gecp-0830a9250/"
            >
              <img src="~/assets/Socials/linkedin.svg" alt="linkedin" />
            </a>
          </div>
        </div>
      </div>
      <hr />
      <div class="attribution">
        <span>© 2022, CODE HIVES. All rights reserved. </span><br />
        <span>MADE ❤️ BY <a href='https://www.linkedin.com/in/hiren-lalani-8a6ba41b9/' target="_blank">HIREN LALANI </a></span>
      </div>
    </Container>
  </div>
</template>

<script>
import Container from "~/components/Container";
import CopyLink from "~/components/CopyLink";

export default {
  components: {
    Container,
    CopyLink,
  },
  mounted() {
    setTimeout(() => {
      let lastPart;
      if (window.location.href.includes("/prizes")) {
        lastPart = window.location.href.split("/prizes").pop();
        lastPart.replace("/", "");
      } else {
        lastPart = window.location.href.split("/").pop();
      }
      if (lastPart[0] === "#") {
        lastPart = lastPart.substring(1);
        document.getElementById(`${lastPart}`)?.scrollIntoView(true);
      }
    }, 500);
  },
};
</script>

<style lang="scss" scoped>
.footer {
  display: flex;
  flex-direction: column;
  margin-bottom: 2rem;
  align-items: center;
  @include respond-between(md, lg) {
    padding: 40px 20px;
    
  align-items: center;
  }

  @include respond-between(sm, md) {
    text-align: center;
    padding: 40px 20px;
    
  align-items: center;
  }

  @include respond-below(sm) {
    text-align: center;
    padding: 40px 10px;
    
  align-items: center;
  }

  hr {
    width: 85%;
    margin: auto;
  }

  a {
    text-decoration: none;
    color: #848484;
  }
.socialLinks{
  align-items: center;
}
  .contents {
    background-color: #feede3;
    border-radius: 1rem;
    display: flex;
    
  align-items: center;
    flex-direction: column;
  }

  .content-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 100px;
    row-gap: 30px;
    padding: 2rem;

    @include respond-above(lg) {
      padding: 2rem 6rem;
    }

    @include respond-between(md, lg) {
      column-gap: 50px;
    }

    @include respond-below(md) {
      column-gap: 50px;
      grid-template-columns: 1fr 1fr;
      margin: auto;
    }

    @include respond-between(sm, md) {
      column-gap: 30px;
    }

    @include respond-below(xs) {
      grid-template-columns: 1fr;
      margin: auto;
    }
  }

  .panel {
    display: flex;
    flex-direction: column;
    line-height: 2;

    a {
      transition: all 0.3s ease;
      &:hover {
        color: #e85325;
        transition: all 0.3s ease;
      }
    }

    .branding {
      img {
        margin-top: 40px;
        margin-bottom: -30px;

        @include respond-below(md) {
          max-width: 100%;
          margin-top: 60px;
        }

        @include respond-below(xxs) {
          width: 100%;
          margin-bottom: -40px;
        }
      }
    }

    .socialLinks {
      padding: 20px 0 10px;
      margin-left: 5px;
      align-items: center;

      a {
        position: relative;
        padding: 10px;
        margin: 5px;
        background: #231f20;
        border-radius: 49%;
        text-align: center;
        box-shadow: rgba(255, 107, 0, 0.4) 0px 0px 20px 0px;

        &:hover {
          background: #e85325;
          box-shadow: rgba(232, 82, 37, 0.25) 0px 0px 0px 6px;
        }

        img {
          height: 20px;
          width: 20px;
          position: relative;
          top: 4px;
        }
      }
    }

    .description {
      opacity: 0.5;
    }

    .title {
      padding: 10px 0;
    }
  }

  .attribution {
    padding: 10px 20px;
    margin-top: 20px;
    margin-bottom: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    text-align: center;
    font-weight: 600;

    span {
      margin-top: -10px;
      @include respond-below(sm) {
        margin-bottom: 1em;
      }
    }

    img {
     height: 25px;
     width: 25px;
    }
  }
}
</style>
