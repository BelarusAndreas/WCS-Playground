
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.simpleFooter{
    padding: 70px 0;
    color: #fff;
}

.footerContainer{
    max-width: 1170px;
    margin: 50px auto 0;
}

.row{
    width:100%;
    display:flex;
    flex-wrap: wrap;
}

.footer-col{
    width:25%;
    padding: 0 15px;
}

.footer-col h4{
    font-size: 18px;
    color:#fff;
    font-weight: 500;
    margin-bottom: 35px;
    position: relative;
}

.footer-col h4::before{
    content: '';
    position: absolute;
    left: 0;
    bottom: -10px;
    height: 2px;
    width:50px;
    background: #088178;
    box-sizing: border-box;
}

.footer-col ul{
    list-style: none;
}

.footer-col ul li:not(:last-child){
    margin-bottom: 10px;
}

.footer-col ul li > a{
    font-size: 16px;
    font-weight:300;
    color:#fff;
    text-transform: capitalize;
    text-decoration: none;
    color:#bbb;
    display: block;
    transition: .3s ease;
}

.footer-col ul li > a:hover{
    color:#fff;
    padding-left: 8px;
}

.footer-col .social-icons{
    font-size:16px;
}

.footer-col .social-icons > a{
    display:inline-block;
    width:40px;
    height:40px;
    text-align: center;
    margin: 0 10px 10px 0;
    padding: 0;
    color:#bbb;
    transition: all .3s ease;
    text-decoration: none;
}


.footer-col .social-icons > a:hover{
    transform: translateY(-5px);
    color:#fff;
}

@media (max-width:768px){
    .footer-col{
        margin-bottom: 30px;
        width:50%;
    }
}

@media (max-width:539px){
    .footer-col{
        width:100%;
    }
}
</style>

<div class="simpleFooter">
  <div class="footerContainer">
    <div class="row">
      <div class="footer-col">
        <h4>Titel</h4>
          <ul>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>Titel</h4>
          <ul>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>Titel</h4>
          <ul>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
            <li><a href = '#'>Link</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>Folge uns</h4>
          <div class='social-icons'>
            <a href = '#'><i class="fa-brands fa-square-instagram" style="font-size: 45px;"></i></a>
            <a href = '#'><i class="fa-brands fa-square-youtube" style="font-size: 45px;"></i></a>
            <a href = '#'><i class="fa-brands fa-square-pinterest" style="font-size: 45px;"></i></a>
            <a href = '#'><i class="fa-brands fa-square-facebook" style="font-size: 45px;"></i></a>
          </div>
        </div>
      </div>
    </div>
  </div>
```

### Benutzung:
1.  Gehe zu ACP   ➞  Anpassung   ➞  Templates   ➞  Filter: `DEIN STIL`   ➞  Suche:  `pageFooter`
     Hinweis:  *Sollte das Template noch nicht vorhanden sein, so ist dies aus der Standard-Templategruppe zu kopieren!*
2.  Suche dort nach  `<footer id="pageFooter" class="pageFooter">`  und füge  **davor**  den o.g. Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
3. Fertig!
