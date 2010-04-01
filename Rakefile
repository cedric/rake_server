task :init do
  system('notify-send "starting up"')
end

task :shout do
  system('notify-send "Hey!"')
end

task :pid do
  system("notify-send #{Process.pid}")
end

task :relax do
  sleep(10)
end

task :print do
  puts ENV['MESSAGE']
end

task :hello do
  puts "Hello, world!"
end

task :setup_server do
  RakeServer::Server.before_fork do
    `notify-send "#{Process.pid}"`
  end
  RakeServer::Server.after_fork do
    `notify-send "#{Process.pid}"`
  end
end

namespace :namespace do
  task :shout do
    system('notify-send "Namespace::Hey!"')
  end
end
