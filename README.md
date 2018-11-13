Instructions:

rails new people -d postgresql

cd people
(clean up gem file, create git repo, copy git remote)

git add .

git commit -m ‘initial commit’

git push origin master

rails g model person first_name last_name age:integer hair_color eye_color gender alive:boolean

bundle exec db:create db:migrate

rails g controller people index show
(We will make a partial form later so new and edit are not necessary at this point)

(add resources :people to config.routes, fill out controller methods)

(Fill out model instance method, e.g.

class Person < ApplicationRecord
  
  def full_name
    "#{self.first_name} #{self.last_name}"
  end

end


)