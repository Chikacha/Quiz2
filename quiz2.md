<tb>1.</tb>
```ruby
 a = 1 
```
宣告一個變數，其值為1
```ruby
@a = 2
```
宣告一個實例變數，其值為1
```ruby
@@a = 5
```
宣告一個類別變數，其值為1
```ruby
user = User.new
```
創造一個新的物件，其類別為User
```ruby
user.name
```
呼叫物件user中的name變數
```ruby
user.name = "Joe"
```
使user中的name變數其值變為Joe

<tb>2.</tb>
module是一個工具庫，不可繼承和new，可供多個類別使用
```ruby
module 替身
  def fight
    puts "オラオラオラオラオラオラ!!!!!"
  end
end

class JoJo  
  attr_accessor :name, :age

  def initialize(name, age)
    @name = name
    @age = age
  end

  include 替身
end

空条承太郎 = JoJo.new("Joutarou", 17)
空条承太郎.fight
```
<tb>3.</tb>

class variable不用new出物件就可以直接呼叫使用

各個被new出來的物件持有自己的instance variable，彼此不共通

<tb>4.</tb>

class method不用new出物件就可以直接呼叫使用

instance method要new出物件才可以被呼叫使用

<tb>5.</tb>

```ruby
def initialize(name, gender, job)
  @name = name
  @gender = gender
  @job = job
end
```

<tb>6.</tb>

A指向Class本身，B指向物件

<tb>7.</tb>

attr_accessor的功能是自動產生Getter和Sette

attr_reader只會產生Getter而attr_writer只會產生Setter

<tb>8.</tb>

public method可以被其他Class呼叫使用

private method只能在自己的Class內部使用

<tb>9.</tb>

Inheritance

用於繼承共通的"特性"，用法如：
```ruby
class Aninal
  def eat
    puts "EAT"
  end
end

class Dog < Animal
end

class Cat < Animal
end

kitty = Cat.new
snoopy = Dog.new
kitty.eat
snoopy.eat
```

Module

類似工具箱，可存放各種功能，用法如

```ruby
module Skill
  def cleanGun
    puts "清槍開始清槍蹲下"
  end
end

class Soldier
  include Skill
end

mike = Soldier.new

mike.cleanGun
```

<tb>10.</tb>

parent class不行，sub class可以

<tb>11.</tb>

Relational Database

一種基於資料關聯性的模型所創建出來的資料庫

SQL

用於操作資料庫的一種語言

