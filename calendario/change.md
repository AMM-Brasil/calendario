<script>
  function getQueryVariable(variable) {
    var query = window.location.search.substring(1);
    var vars = query.split("&");
    for (var i = 0; i < vars.length; i++) {
      var pair = vars[i].split("=");
      if (pair[0] == variable) {
        return pair[1];
      }
    }
    return (false);
  }
  region = getQueryVariable('r');
  if (typeof(Storage) !== "undefined") {
    localStorage.setItem("lastRegion", region);
  } 
  location.href = "{{ site.baseurl }}/calendario/" + region + ".html";
</script>
