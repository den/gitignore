task :default => 'global'

desc "Generate .global_ignore"
task :global do
  global_ignore = FileList['Global/*.gitignore']
  ignore_file = ""
  global_ignore.each do |file|
    ignore_file << IO.read(file) << "\n"
  end
  file_path = ENV['HOME'] + '/.global_ignore'
  File.open(file_path, 'w') do |f|
    f.puts ignore_file
  end
end