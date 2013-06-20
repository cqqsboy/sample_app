# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard 'rspec', :version => 2 do
watch(%r{ˆapp/controllers/(.+) (controller)\.rb$}) do |m|
["spec/routing/#{m[1]} routing spec.rb",
"spec/#{m[2]}s/#{m[1]} #{m[2]} spec.rb",
"spec/acceptance/#{m[1]} spec.rb",
(m[1][/ pages/] ? "spec/requests/#{m[1]} spec.rb" :
"spec/requests/#{m[1].singularize} pages spec.rb")]
end
watch(%r{ˆapp/views/(.+)/}) do |m|
"spec/requests/#{m[1].singularize} pages spec.rb"
end

end

