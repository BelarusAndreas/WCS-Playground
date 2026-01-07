

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.row {
  margin: 2%;
}
#searchList{
  background-color: #DCDCDD;
  padding: 2%;
}
dt{
  font-size: 120%; 
  color: #035870;
  font-family: 'Lora', serif;
  margin-top: 1%;
  margin-bottom: 1%;
}
dd{
  font-size: 90%;
  color: #00151b;
  font-family: 'Lora', serif;
}
#submitter {
    margin-top: 10px !important;
}
#errorMsg{
  color: white;
  font-size: 120%;
}
</style>

<div class="container"> 
  <div class="row">
    <div class="col text-center">
     <a href="https://de.wikipedia.org/wiki/Special:Random" target="_blank" class ="btn btn-primary">Zufälliger Artikel</a>
    </div>
  </div>
  <div class="row">
    <div class="col-lg-4 col-lg-offset-4 text-center" id="searchCol">    
      <form class="input-group" id="searchForm">
        <input type="text" id="searchInput" class="form-control" placeholder="Suche nach Artikel...">
        <span class="input-group-btn">
          <button class="btn btn-success" id="submitter" type="submit">Suchen</button>
        </span>
      </form>
     </div>
  </div> 
  <div class="row">
    <div class="col-lg-8 col-lg-offset-2" id="mainContent">      
      <p style="display:none" id="errorMsg" class="text-center">Keine Ergebnisse gefunden!</p>
      <dl style="display: none" id="searchList" class="thumbnail">     
      </dl>   
    </div>
  </div>
</div>

<script>
$(function () {
  // $("#searchList").hide();
  // $("#errorMsg").hide();
  $.ajaxSetup({ cache: false });  
  $('#searchForm').attr('autocomplete', 'off');
  var searchTerm = "";
  $("#searchForm").on('submit', function(e) {  
    e.preventDefault();
    $("#searchList").html(""); 
     e.preventDefault();
     searchTerm = $("#searchInput").val();
     getArticles(searchTerm);   
   });
   function getArticles(string) {  
    $.getJSON("https://de.wikipedia.org/w/api.php?action=query&format=json&origin=*&prop=extracts%7Cinfo&list=&meta=&generator=search&exsentences=1&exlimit=10&exintro=1&explaintext=1&inprop=url&gsrsearch=" + string + "&gsrnamespace=0&gsrlimit=10&gsrwhat=text&gsrinfo=totalhits&gsrprop=", function(data) {
     var count = Object.keys(data).length;
      if(count <=2){
        $("#searchList").hide();
         $("#errorMsg").show();        
      }else {
        $("#errorMsg").hide();
         for(i = 0; i < Object.keys(data.query.pages).length; i++){       
        $("#searchList").append('<a href ="' + data.query.pages[Object.keys(data.query.pages)[i]].fullurl + '" target="_blank"><dt>' + data.query.pages[Object.keys(data.query.pages)[i]].title + "</dt></a>");
        $("#searchList").append("<dd>" + data.query.pages[Object.keys(data.query.pages)[i]].extract + "</dd>");        
     }
      $("#searchList").hide().fadeIn(300);
      }      
  });     
 }
});    
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
