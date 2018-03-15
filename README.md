//Practice Shortcode

add_shortcode('our_services', 'service_shortcode');
function service_shortcode($atts){
	extract(shortcode_atts(array(
		's_icon' =>'',
		's_title' =>'',
		's_content' =>'',
	), $atts));
	
	$markup='
	<div class="col-md-3 col-sm-6 col-xs-12">
        <div class="service-item first-service">
            <i class="fa fa-'.$s_icon.'"></i>
            <h4>'.$s_title.'</h4>
            <p>'.$s_content.'</p>
        </div>
    </div> 
	
	';
	return $markup;
}
