require 'fileutils'

namespace :book do
  desc 'Book publishing toolchain'

  # Entry point of the book.
  bookEntry = 'brewtarget.asc'
  # Directory to build the book to
  buildDirectory = 'build'
  # Formats and their associated processor.
  formats = [
    ['html', 'asciidoctor'],
    ['epub3', 'asciidoctor-epub3'],
    ['pdf', 'asciidoctor-pdf']
  ]

  task :build do
    puts 'Build standard book formats'

    if Dir.exists?(buildDirectory)
      puts '[warning] Output already present book:clean to regenerate'
      next
    end

    puts '  Creating output directory'
    Dir.mkdir buildDirectory
    formats.each do |format|
      puts '  Building format : ' + format[0]
      `bundle exec #{format[1]} -D #{buildDirectory} #{bookEntry}`
    end
  end

  task :clean do
    FileUtils.rm_rf(buildDirectory)
  end
end