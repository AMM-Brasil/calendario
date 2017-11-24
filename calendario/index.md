<script>
  if (typeof(Storage) !== "undefined") {
    lastRegion = localStorage.getItem("lastRegion");
    location.href =
      (lastRegion == null) ?
      "{{ site.baseurl }}/calendario/nacional.html" :
      "{{ site.baseurl }}/calendario/" + lastRegion + ".html";
  } else {
    location.href = "{{ site.baseurl }}/calendario/nacional.html";
  }
</script>
