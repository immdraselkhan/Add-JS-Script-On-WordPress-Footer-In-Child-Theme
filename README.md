# Add this code on your function.php file

add_action('wp_footer', 'cookie_footer_js');
    function cookie_footer_js() {
      echo '
    <script src="https://cdn.jsdelivr.net/npm/cookieconsent@3/build/cookieconsent.min.js" data-cfasync="false"></script>
    <script>
    window.cookieconsent.initialise({
      "palette": {
        "popup": {
          "background": "#000"
        },
        "button": {
          "background": "#ff66c4",
          "text": "#ffffff"
        }
      },
      "theme": "classic",
      "content": {
        "href": "/privacy-policy/"
      }
    });
    </script>';
}
