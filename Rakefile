require 'aweplug/extensions/kramdown_demo'
require 'awestruct/logger'
require 'logger'
require 'fileutils'

task :default do
  FileUtils.mkdir '.awestruct' unless File::exists?('.awestruct')
  $LOG = Logger.new(Awestruct::AwestructLoggerMultiIO.new(false, STDOUT, File.open('.awestruct/debug.log', 'w')))
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

