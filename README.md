# sbr-mustervorlagen
Mustervorlagen für SBR-Websites Post Postbank Telekom zum Einbinden

Der folgende PHP-Code muss in die Datei "functions.php" oder einem geeigneten Plugin für Snippets eingefügt werden:

function show_file_func( $atts ) {
  extract( shortcode_atts( array(
    'file' => ''
  ), $atts ) );
  
  if ($file!='')
  return @file_get_contents($file);
}
add_shortcode( 'show_file', 'show_file_func' );

Quelle: https://pixeltuner.de/wordpress-externe-dateien-per-shortcode-integrieren/

Danach wird der folgende Shortcode in die Seite, dem Beitrag oder einem Widget hinzugefügt:

[show_file file="URL"]

Der Wert "URL" wird durch die Adresse der jeweiligen Vorlage ersetzt.

Shortcode zur Datenschutzerklärung:
[show_file file="https://raw.githubusercontent.com/m266/sbr-mustervorlagen/master/sbr-datenschutz.html"]

Shortcode für die SBR-Gremien:
