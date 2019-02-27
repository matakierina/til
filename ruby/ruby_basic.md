## 出力、表示
```ruby
>>> puts "Hello World"
    puts 'Hello World'

# コメント残せるよん
```
  
## 変数を文字列に含める（変数展開）
```ruby
>>> name = "えりな"
    puts "こんにちは、#{name}さん"
    => こんにちは、えりなさん

# 変数を文字列内に入れる場合に使う
```

## 条件式
```ruby
>>> if 条件式
        # 処理内容
    end

>>> if 条件式
        # 処理内容
    elsif 条件式
        # 処理内容
    else
        # 処理内容
    end

>> aとbが一致
    a == b
>> aとbが不一致
    a != b
```

## 配列
```ruby
>> 文字列をまとめた配列
    ["Erina", "Takashi", "Shizuku"]
>> 数字をまとめた配列
    [21, 15, 63]

>>> names = ["Erina", "Takashi", "Shizuku"]
    puts names
    => Erina
       Takashi
       Shizuku
    puts names[1]
    => Takashi
    puts "私の名前は#{names[1]}です"
    => 私の名前はたかしです
```

## 繰り返し処理
``` ruby
>>> 配列 .each do |変数名|
        # 実行したい処理
    end
```

## ハッシュ
```ruby
# キーが文字列の書き方
>> {"name" => "Erina", "age" => 23}

>>> user = {"name" => "Erina", "age" => 23}
    puts user
    => {"name" => "Erina", "age" => 23}
    puts user["name"]
    => Erina

    user["gender"] = "female"
    puts user
    => {"name" => "Erina", "age" => 23, "gender" => "female"}

# キーがシンボルの書き方
>> {:name => "Erina", :age => 23}

>>> user = {:name => "Erina", :age => 23}
    puts user[:name]
    => Erina

# キーがシンボルの書き方（省略形）
>> {name: "Erina", age: 23}

>>> user = {name: "Erina", age: 23}
    puts user[:name]
    => Erina

# nilとは？
=> 「何もない」という意味の特別な値
>>> user = {name: "Erina", age: 23}
    user[:weight]
        # 何も表示されない

# nilを利用したif文
if文の条件
=> false : false と nil
    true : 上記以外

>>> user = {name: "Erina"}
    if user[:age]
      # nil => false
        puts "#{user[:name]}さんは#{user[:age]}歳です"
    else
        puts "#{user[:name]}さんの年齢は秘密です"
    end
    => Erinaさんの年齢は秘密です
```

## 要素がハッシュである配列
``` ruby
>>> users = [
    {name: "Takashi", age: 22},
    {name: "Erina", age: 23}
    ]
    puts users[1]
    => {:name => "Erina", :age => 23}
    puts users[1][:name]
    => Erina

# eachの中でハッシュを使う
>>> users = [
    {name: "Takashi", age: 22},
    {name: "Erina", age: 23}
    ]
    users .each do |user|
        puts user[:name]
    end
    => Takashi
       Erina