task :build do
  Dir[File.join(File.expand_path('..', __FILE__), '**', '*template.html')].each do |template|
    md = template.sub(/template.html$/, 'md')
    html = template.sub(/template.html$/, 'html')
    if File.exists?(md)
      guts = File.read(template)
      File.open(html, 'w') do |f|
        f.print guts.sub(/\s+#{Regexp.escape("<!-- include #{File.basename(md)} -->")}/, File.read(md))
      end
    end
  end
end