$heroes = []

def add_hero(name, secret_identity, weakness)
  $heroes << {
    name: name, 
    secret_identity: secret_identity, 
    weakness: weakness
    }
  "Hero Added"
end

def list_hero
   if $heroes.count < 1
    puts "\nNo heroes here"
  else
    puts "\n" 
  $heroes.each do |hero|
    puts hero[:name]
  end
end
call_methods
end

def list_hero_full
  if $heroes.count < 1
    puts "\nNo heroes here"
  else
    puts "\n" 
  $heroes.each do |hero|
    puts "#{hero[:name]}, #{hero[:secret_identity]}, #{hero[:weakness]}"
  end
end
call_methods
end

def authorization
  puts "Enter the password"
  password = gets.chomp
  if password == "1234"
    list_hero_full
  else
    puts "Incorrect password"
    list_heroes
  end
end

def create_hero
  puts "Enter superhero name"
  name = gets.chomp
  puts "Enter hero's real identity"
  secret_identity = gets.chomp
  puts "Enter weakness"
  weakness = gets.chomp
  add_hero(name, secret_identity, weakness)
  puts "#{name} added"
  call_methods
end

def remove_hero
  puts "Enter superhero name to delete"
  name = gets.chomp
  $heroes.reject! {|hero| hero[:name].downcase == name.downcase}
  puts "Delete Successful"
  call_methods
end

def menu
  print "\n------------------------------------------------------------
Would you like to:
  1. List Superheroes
  2. List Superheroes with their secret identities
  3. Add a new Superhero
  4. Remove fallen superheroes
  5. Exit
------------------------------------------------------------\n=> "
  choice = gets.chomp
  return choice
end

# Call functions based on choice
def call_methods
  choice = menu
  if choice == "1"
    list_hero
    elsif choice == "2"
      authorization
      elsif choice == "3"
        create_hero
        elsif choice == "4"
          remove_hero
          elsif choice == "5"
            exit
            else
              print "Incorrect input"
              call_methods
  end
end

call_methods
