
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.burger-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transition: .3s ease;
  cursor: pointer;
  gap: 0;
  .menu-item {
    position: relative;        
      span {
        display: block;
      }        
      .text {
        position: absolute;
        opacity: 0;
        top: 50%;
        transition: .3s ease;
        transition-delay: .2s;
        width: 100px;
      }   
      &:nth-child(even) {
        .text {
          left:120%;
          transform: translate(30px,-50%);
          opacity: 0;
        }
      }        
      &:nth-child(odd) {
        .text {
          right:120%;
          transform: translate(-30px,-50%);
          opacity: 0;
          text-align: right;
        }
      }
    }    
    &.open {
      gap: 1rem;
      .menu-item {
        &:nth-child(even) {
          .text {
            opacity: 1;
            transform: translate(0, -50%);
          }
        }
        &:nth-child(odd) {
          .text {
            opacity: 1;
            transform: translate(0, -50%);
          }
        }
      }
    }
  }
  .bun {
    width: 60px;
    height: 10px;
    background: #D28B46;    
    &.bun-top {
      border-radius: 15px 15px 0 0;
      position: relative;
      height: 20px;        
      .seeds {
        width: 6px;
        height: 3px;
        background: #fffdd0;
        border-radius: 6px;
        position: absolute;            
        &:first-child {
          top:1px;
          left:10px;
          transform: rotate(20deg);
        }
        &:nth-child(2) {
          top:4px;
          left:42px;
          transform: rotate(-15deg);
        }
        &:nth-child(3) {
          top:2px;
          left:51px;
          transform: rotate(60deg);
        }
        &:nth-child(4) {
          top:1px;
          left:24px;
          transform: rotate(-8deg);
        }
        &:nth-child(5) {
          top:0px;
          left:35px;
          transform: rotate(25deg);
        }
      }
    }    
    &.bun-bottom {
      border-radius: 0 0 5px 5px;
    }
  }
  .steack {
    width: 64px;
    height: 12px;
    border-radius: 5px;
    background: #592720;
  }
  .cheese {
    position: relative;
    width: 60px;
    height: 3px;
    border-radius: 2px;
    background: #ffeb00;
    z-index: 5;  
    &:after, &:before {
      content:"";
      width: 4px;
      height: 10px;
      border-radius: 0 0 20px 20px;
      display: block;
      position: absolute;
      background: inherit;
      right:0;
      top:0;
    }    
    &:before {
      right:20px;
      height: 12px;
      width: 8px;
    }
  }
  .salad {
    width: 65px;
    height: 2px;
    background: green;
  }
  .tomato {
    position: relative;
    width: 60px;
    height: 4px;   
    &:before, &:after {
      content:'';
      display: block;
      width: 28px;
      height: 2px;
      background: red;
      border-radius: 2px;
      border: 1px solid #cd2626;
    }    
    &:before {
      position: absolute;
      left:3px;
      transform: rotate(2deg);
    }  
    &:after {
      position: absolute;
      left:28px;
      transform: rotate(-2deg);
    }
  }
  .text {
    color: #fff;
    font-family: sans-serif;
}
</style>

<div class="burger-wrapper">
  <div class="menu-item">
    <span class="bun bun-top">
    <span class="seeds"></span>
    <span class="seeds"></span>
    <span class="seeds"></span>
    <span class="seeds"></span>
    <span class="seeds"></span>
    </span><span class="text">Brötchen oben</span>
  </div>
  <div class="menu-item">
    <span class="tomato"></span><span class="text">Tomaten</span>
  </div>
  <div class="menu-item">
    <span class="salad"></span><span class="text">Salat</span>
  </div>
  <div class="menu-item">
    <span class="cheese"></span><span class="text">Käse</span>
  </div>
  <div class="menu-item">
    <span class="steack"></span><span class="text">Patti</span>
  </div>
  <div class="menu-item">
    <span class="bun bun-bottom"></span><span class="text">Brötchen unten</span>    
  </div>
</div>

<script>
  document.querySelector('.burger-wrapper').addEventListener('click', function(){
    document.querySelector('.burger-wrapper').classList.toggle('open');
  })
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen / Seiten
2.  Klicke auf  + Box / Seite hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
