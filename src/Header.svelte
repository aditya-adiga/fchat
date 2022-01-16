<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
  {#if $username}
    <img align="left" src={`./jolly.png`} alt="F-CHAT"/>
      <span><img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" /></span>
      <span><strong>{$username}</strong></span>
      <span><button type="button" class="btn mr-md-2 mx-md-0 mb-2 btn-outline-primary btn-round" on:click={signout}>Sign Out</button></span>
    
      
    {:else}
      <h3>F-CHAT</h3>
  {/if}
</header>