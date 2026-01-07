### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
$blue: #23242a;
$grey: #f2f3f6;
$light-grey: lighten($grey, 2%);
$dark-grey: darken($grey, 10%);
@keyframes shake {
   0%, 100% {transform: translateX(0);} 
   10%, 30%, 50%, 70% {transform: translateX(-5px);} 
   20%, 40%, 60%, 80% {transform: translateX(5px);} 
}
@mixin center {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  margin: auto;
}
.container {
  @include center;
  width: 300px;
  height: 300px;
  background: $grey;
  padding: 1em;
  border: 1px solid $dark-grey;
  box-shadow: 0 1px 2px rgba(0,0,0,0.05), 0 5px 10px rgba(0,0,0,0.05);;
  border-radius: 3px;
  overflow: hidden;
}
.input-query {
  width: 100%;
  padding: 0.5em;
  border: 1px solid $dark-grey;
  border-radius: 3px;
  font-size: 1em;  
  &:focus ~ .counter {
    opacity: 0.1;
    transition: opacity 1s ease-in;
  }
}
.list-wrap {
  margin-top: 0.4em;
  overflow-y: auto;
  overflow-x: hidden;
}
.list {
  max-height: 220px;
}
.list-item {
  font-size: 0.9em;
  padding: 0.5em 0.8em;
  border-bottom: 1px solid $dark-grey;
  border-top: 1px solid white;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  word-wrap: normal;
  max-width: 100%;
  &:first-child {
    border-top: none;
  }
  &:last-child {
    border-bottom: none;
  }
}
.list-item-link {
  color: #444;
  text-decoration: none;
}
.list-item--disable {
  text-align: center;
  border-bottom: none;
  animation: shake 0.6s;
  color: #9da1b1;
}
.counter {
  position: absolute;
  bottom: -15px;
  right: 10px;
  z-index: 0;
  font-size: 3.5em;
  color: black;
  transform: translateY(0);
  opacity: 0;
}
</style>

<div class="container" data-behaviour="search-on-list">
  <input type="text" class="input-query" data-search-on-list="search" placeholder="Suche ..."/>
  <span class="counter" data-search-on-list="counter"></span>
  <div class="list-wrap">
  <ul class="list" data-search-on-list="list">
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Michael <span class="item-list-subtext">Jackson</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Paul <span class="item-list-subtext">McCartney</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Modern<span class="item-list-subtext">Talking</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Cindy<span class="item-list-subtext">Lauper</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Bonnie<span class="item-list-subtext">Tailer</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Depeche <span class="item-list-subtext">Mode</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Phil <span class="item-list-subtext">Collins</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Billy <span class="item-list-subtext">Ocean</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Mike <span class="item-list-subtext">Oldfield</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Bryan <span class="item-list-subtext">Adams</span></a>
    </li>
    <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Alice <span class="item-list-subtext">Cooper</span></a>
    </li>
       <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Barclay <span class="item-list-subtext">James Harvest</span></a>
    </li>
       <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Boney <span class="item-list-subtext">M</span></a>
    </li>
       <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Duran <span class="item-list-subtext">Duran</span></a>
    </li>
       <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Elton <span class="item-list-subtext">John</span></a>
    </li>
           <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Fine <span class="item-list-subtext">Young Cannibal</span></a>
    </li>
           <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Kim <span class="item-list-subtext">Wild</span></a>
    </li>
           <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Kate <span class="item-list-subtext">Ryan</span></a>
    </li>
           <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Nino <span class="item-list-subtext">De Angelo</span></a>
    </li>
               <li class="list-item" data-search-on-list="list-item">
      <a href="" class="list-item-link">Paul <span class="item-list-subtext">Young</span></a>
    </li>
  </ul>
  </div>
</div>

<script>
(function() {
  function format(text) {
    return text.replace(/ /g,'').replace(/(<([^>]+)>)/ig, '').toLowerCase();  
  }
  var SearchOnList = {
    $LIST           : '[data-search-on-list=list]',
    $SEARCH         : '[data-search-on-list=search]',
    $LIST_ITEM      : '[data-search-on-list=list-item]',
    $COUNTER        : '[data-search-on-list=counter]',
    TEMPLATE_EMTPY  : '<li class="list-item list-item--disable">No results found</li>', 
    init: function($element) {
      this.items = [];
      this.itemsMatched = [];
      this.$element = $element;
      this.$list = this.$element.find(this.$LIST);
      this.$search = this.$element.find(this.$SEARCH);
      this.$counter = this.$element.find(this.$COUNTER); 
      this.items = this._getAllItems();
      this.itemsMatched = this.items; 
      this._updateCounter();
      this._handleResults();
      this._setEventListeners();
    },   
    _setEventListeners: function() {
      this.$search
        .on('keyup', $.proxy(this._onKeyup, this))
        .on('query:changed', $.proxy(this._handleQueryChanged, this))
        .on('query:results:some', $.proxy(this._handleResults, this))
        .on('query:results:none', $.proxy(this._handleNoResults, this))
    }, 
    _onKeyup: function() {
      var query = this.$search.val(),
          previousQuery = this.$search.data('previousQuery', query);
      if (this._queryChanged()) {
        this.$search.trigger('query:changed', { 
          query: query, 
          previousQuery: previousQuery 
        });
      }
    },
    _queryChanged: function() {
      var query = this.$search.val();
      if ($.trim(query).length === 0 && this.$search.data('previousQuery') === undefined) {
        return false;
      }
      return true;
    },
    _handleQueryChanged: function(e, data) {   
      this.itemsMatched = this.items.map(function(item) {
        if (format(item.name).match(format(data.query))) {
          return { 
            name: item.name, 
            visible: true 
          } 
        }
        return { 
          name: item.name, 
          visible: false
        } 
      });    
      this._render();
      this._updateCounter();
    },   
    _handleNoResults: function() {
      this.$list.html(this.TEMPLATE_EMTPY);
    },  
    _handleResults: function() {
      this.$list.empty().append(this._renderItemsVisible())
    }, 
    _someItemsVisible: function() {
      return this.itemsMatched.some(function(item) { 
        return item.visible;
      });
    },
    _render: function() {
      (this._someItemsVisible()) ?
        this.$search.trigger('query:results:some') :
        this.$search.trigger('query:results:none'); 
    },  
    _updateCounter: function() {
      (this._someItemsVisible()) ?
        this.$counter.text(this._renderItemsVisible().length) :
        this.$counter.text('');
    }, 
    _getAllItems: function() {
      var $items = this.$list.find(this.$LIST_ITEM);  
      return $items.map(function() {
        var $item = $(this);      
        return {
          name: $item.html(),
          visible: true
        };
      }).toArray();     
    },   
    _renderItemsVisible: function() {
      var itemInTemplate;
      return this.itemsMatched.sort(function(a, b) {
        if (a.name < b.name) return -1
        if (a.name > b.name) return 1;
        return 0;
      }).reduce(function(items, item) {
        itemInTemplate = '<li class="list-item" data-search-on-list="list-item">' + item.name + '</li>';
        if (item.visible) {
          items.push(itemInTemplate);
        }  
        return items;
      }, []);
    }
  };  
  window.SearchOnList = SearchOnList;
})();
SearchOnList.init($('[data-behaviour=search-on-list]'));
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

