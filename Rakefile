require 'rake/clean'

maruku='lib/maruku-0.5.8'
web_dir="/data/www/doc/media.build-doctor.com/rosetta-stone"
CLEAN.include("stone.pdf","stone.aux", "stone.html",
  "stone.log", "stone.tex", "stone.out")

task :default => [ :clean ] do
  file = 'stone.markdown'
  cmd = "#{maruku}/bin/maruku"
  lib = "#{maruku}/lib"
  ruby "-I #{lib} #{cmd} --pdf #{file}"  if system("pdflatex -help")
  ruby "-I #{lib} #{cmd} --html #{file}"
end

task :publish => [ :default ] do
  mkdir_p(web_dir)
  ["stone.pdf", "style.css" , "license.png", "logo.jpg",  "style.css" ].each  {|f| cp f, web_dir}
  cp "stone.html", File.join(web_dir,"index.html")
end

task :cruise => [:publish]
