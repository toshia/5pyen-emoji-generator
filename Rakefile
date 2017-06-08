# coding: utf-8

SRC_5000兆円 = 'src/5pyen.png'
SRC_欲しい = 'src/hoshii.png'

namespace :'5000pyen' do
  desc '1行の5000兆円を出力します'
  file 'build/5000兆円/single' => ['build/5000兆円'] do
    mkdir_p 'build/5000兆円/single'
    system(*%W<convert -crop 128x128 #{SRC_5000兆円} build/5000兆円/single/5pyen.png>)
    puts 'build/5000兆円/single に、5000兆円(1行)を出力しました'
  end

  desc '2行の5000兆円を出力します'
  file 'build/5000兆円/double' => ['build/5000兆円'] do
    mkdir_p 'build/5000兆円/double'
    system(*%W<convert -crop 64x64 #{SRC_5000兆円} build/5000兆円/double/5pyen.png>)
    puts 'build/5000兆円/double に、5000兆円(2行)を出力しました'
  end

  directory 'build/5000兆円' => 'build'
end

namespace :hosii do
  desc '1行の欲しいを出力します'
  file 'build/欲しい/single' => ['build/欲しい'] do
    mkdir_p 'build/欲しい/single'
    system(*%W<convert -crop 128x128 #{SRC_欲しい} build/欲しい/single/hoshii.png>)
    puts 'build/欲しい/single に、欲しい(1行)を出力しました'
  end

  desc '2行の欲しいを出力します'
  file 'build/欲しい/double' => ['build/欲しい'] do
    mkdir_p 'build/欲しい/double'
    system(*%W<convert -crop 64x64 #{SRC_欲しい} build/欲しい/double/hoshii.png>)
    puts 'build/欲しい/double に、欲しい(2行)を出力しました'
  end

  directory 'build/欲しい' => 'build'
end


task :clean do
  rm_rf 'build'
end

task :default => ['build/5000兆円/single', 'build/5000兆円/double',
                  'build/欲しい/single', 'build/欲しい/double']

directory 'build'
