Level 1

class Player
   def play_turn(warrior)
     warrior.walk!
   end
 end

Level 2

class Player
  def play_turn(warrior)
    if warrior.feel.empty?
      warrior.walk!
    else
      warrior.attack!
    end
  end
end

Level 3

class Player
 
   MIN_HEALTH = 15
   
   def play_turn(warrior)
     if warrior.feel.empty?
      if warrior.health < MIN_HEALTH
        warrior.rest!
      else
        warrior.walk!
      end
    else
      warrior.attack!
    end
    
  end
end

Level 4

class Player
   def play_turn(warrior)
      if warrior.feel.empty? then
         if (warrior.health==20) or (warrior.health<@health) then
         warrior.walk!
      else
         warrior.rest!;
      end 
   else
      warrior.attack!; 
   end;
   @health=warrior.health; 
   end; 
end
