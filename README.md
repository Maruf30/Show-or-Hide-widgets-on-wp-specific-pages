# Show-or-Hide-widgets-on-wp-specific-pages


add_filter( 'widget_display_callback', 'jeba_hide_widget_pages', 10, 3 );
function jeba_hide_widget_pages( $instance, $widget, $args ) {
  if ( $widget->id_base == 'pages' ) { // change 'pages' to widget name
     if ( !is_page( 'contact' ) ) {    // change page name
         return false;
     }
  }
}
