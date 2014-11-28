first_post_thumbnail_size(130, 100, true);

if (has_post_thumbnail()) {
	the_post_thumbnail(); // display the featured image
} else {
	// set the featured image
	$attachments = get_posts(array(
		'post_type' => 'attachment', 
		'post_mime_type'=>'image', 
		'posts_per_page' => 0, 
		'post_parent' => $post->ID, 
		'order'=>'ASC'
	));
	if ($attachments) {
		foreach ($attachments as $attachment) {
			first_post_thumbnail_size($post->ID, $attachment->ID);
			break;
		}
		the_post_thumbnail(); 		// display the featured image
	}
}
