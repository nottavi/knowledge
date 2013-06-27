knowledge
=========

Liens, code snippets ...

Wordpress
=========

Migration :
UPDATE wp_options
SET option_value = replace(option_value, 'http://example1.ca/site', 'http://example2.ca/site')
WHERE option_name = 'home' OR option_name = 'siteurl';
 
UPDATE wp_posts
SET guid = replace(guid, 'http://example1.ca/site','http://example2.ca/site');
 
UPDATE wp_posts
SET post_content = replace(post_content, 'http://example1.ca/site', 'http://example2.ca/site');
 
UPDATE wp_postmeta
SET meta_value = replace(meta_value, 'http://example1.ca/site', 'http://example2.ca/site');
