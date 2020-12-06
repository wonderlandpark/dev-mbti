<script>
  import {onMount} from 'svelte';
  import Question from './Question.svelte';
  const types = { 
    e: 0, i: 0, 
    s: 0, n: 0,
    t: 0, f: 0,
    j: 0, p: 0
  }
</script>

<style>

  .scroll {
    height: 100vh;
    overflow-y: scroll;
    scroll-snap-type: y mandatory;

    scroll-behavior: smooth;
  }

  .scroll > section {
    height: 100vh;
    scroll-snap-align: start;
    color: white;
  }

  article.hidden {
    
    height: initial;
  }
  :global(body) {
    margin: 0;
    background-color: black;
  }

  .hero {
    background: url('/code.jpg') no-repeat;
    background-size: cover;
    color: white;
    top: 0 !important;
    padding-top: 10em;
  }

  .center {
    text-align: center;
    height: 100vh;
    /* display: flex; */
    /* justify-content: center; */
    /* align-items: center; */
  }

  .bottom {
    bottom: 0;
    position: absolute;
    text-align: center;
  }
  h1 {
    font-size: 5em;
  }

  article {
    color: white;
    padding: 1rem;
  }
</style>

<div class="scroll">
  <article class="hidden">
    HTML은 언어가 아닙니다!!
  </article>
  <section class="hero">
    <div class="center">
      <h1>개발자 MBTI</h1><br/>
      <h2>당신이 어떤 성향의 개발자인지 알아봅시다.</h2>
      <a class="btn btn-primary" href="#question">시작하기</a>
      
    </div>
    
  </section>

  <section id="question">
    <Question question="잔디 관리를 즐긴다"/>
  </section>
</div>