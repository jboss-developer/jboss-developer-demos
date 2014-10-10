require 'aweplug/extensions/kramdown_demo'

task :default do
  demo = Aweplug::Extensions::Kramdown::Demo.new({
    :push_to_searchisko => false, 
    :url => 'demos.yaml',
    :layout => 'get-started-item',
    :normalize_contributors => false,
    :output_dir => '_site/demos'})
  site = OpenStruct.new({:dir => '_site', :pages => [],:profile => 'development'});
  demo.execute(site)
  puts "all ok!"
end

