namespace :book do
  desc 'build basic book formats'
  task :build do
    puts "Converting to HTML..."
    `bundle exec asciidoctor brewtarget.asc`
    puts " -- HTML output at brewtarget.html"

    puts "Converting to EPub..."
    `bundle exec asciidoctor-epub3 brewtarget.asc`
    puts " -- Epub output at brewtarget.epub"

    puts "Converting to PDF... (this one takes a while)"
    `bundle exec asciidoctor-pdf brewtarget.asc`
    puts " -- PDF  output at brewtarget.pdf"
  end
end
