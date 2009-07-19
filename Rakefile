require 'rake/clean'

web_dir="/data/www/doc/media.build-doctor.com/rosetta-stone"
CLEAN.include("stone.pdf","stone.aux", "stone.html",
  "stone.log", "stone.tex", "stone.out")

task :default => [ :clean ] do
  file = 'stone.markdown'
  cmd = 'maruku'
  sh "#{cmd} --pdf #{file}"  if system("pdflatex -help > /dev/null 2>&1")
  sh "#{cmd} --html #{file}"
end

task :publish => [ :default ] do
  mkdir_p(web_dir)
  ["stone.pdf", "style.css" , "license.png", "logo.jpg",  "style.css" ].each  {|f| cp f, web_dir}
  cp "stone.html", File.join(web_dir,"index.html")
end

task :cruise => [:publish]
