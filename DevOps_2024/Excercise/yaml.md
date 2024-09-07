# YAML
[Description](#description)

[Syntax and Structure](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#syntax-and-structure)
- [Key Value Pairs](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#key-value-pairs)
- [Indentation](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#identation)
- [Lists](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#lists)
- [Nested Structures](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#nested-strucutres)
- [Scalars](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#scalars)
- [Comments](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#comments)
- [Tags](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#tags)
- [Anchors and Aliases](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#anchors-and-aliases)
- [Multiline Strings](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#multiline-strings)

[Data Types](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#data-types)
- [Scalars](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#1-scalars)
- [Sequences (Lists)](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#2-sequences-lists)
- [Mappings (Dictionaries)](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#3-mappings-dictionaries)
- [Nested Structures](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#4-nested-structures)
- [Multiline Strings](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#multiline-strings)
- [Anchors and Aliases](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#anchors-and-aliases)
- [Sets](https://github.com/manav-dl/aws_Meetup-2023/blob/main/DevOps_2024/Excercise/yaml.md#7-sets)

## Description
- Data serialization (process of converting structured data into a format that can be easily stored or transmitted and reconstructed later) standard for programming languages.
- Used for config files and data exchange between languages with diff data structures.

## Syntax and Structure:
### Key-Value Pairs:
- Uses key-value pairs to represent data
- Key followed by a colon and a space then the value.
```YAML
name: John Doe
age: 30
```
### Identation:
- YAML uses indentation to denote structure.
- Indentation done using spaces (not tabs).
```yaml
person: 
 name: John Doe  
 age: 30
```
### Lists:
- YAML uses dash (`-`) followed by a space to denote list items.
```yaml
fruits:  
 - apple  
 - banana  
 - cherry
```
### Nested Strucutres:
- YAML supports nested structures, created by further identing the child elements.
```yaml
person:
 name: John Doe
 age: 30
 address: 
  street: 221 Baker Street
  city: London
  state: CA
  zip: 123456
```
### Scalars:
- Scalars are basic data types like strings, numbers, booleans, null, dates, and timestamps.
- Most scalars can be written without quotes (`" "`) but quotes can be used if needed.
```yaml
name: John Doe
age: 30
is_active: true
date_of_birth: 2000-02-29
```
### Comments:
- YAML supports comments using the `#` character.
```yaml
# This is a comment
name: Joe
age: 25
```
### Tags:
- YAML allows custom data types using tags.
```yaml
!!str "This is a string"
!!int 123
```
### Anchors and Aliases
- YAML supports anchors (`&anchor_name`) and aliases (`*anchor_name`) to reuse content.
- `<<` operator is part of YAML's merge key syntax which enables merging the contents of one mapping into another.
```yaml
default_config: &default_config
 host: localhost
 post: 8080

development:
 <<: *default_config
 debug: true

production:
 <<: *default_config
 host: example.com
```
#### Explanation:
**Example 1: Reusing a list**
```yaml
default_fruits: &default_fruits
 - apple
 - banana
 - cherry

fruit_basket:
 <<: *default_fruits
 - orange
 - grape
```
Without anchors and aliases:
```yaml
fruit_basket:
 - apple
 - banana
 - cherry
 - orange
 - grape
```
**Example 2: Reusing a Nested Structure**
```yaml
default_address: &default_address
 street: 123 Main St
  city: Anytown
  state: CA
  zip: 12345

person1:
 name: John Doe
 address: *default_address

person2:
 name: Jane Smith
 address: *default_address
```
Without anchors and aliases:
```yaml
person1:  
 name: John Doe  
 address:    
  street: 123 Main St
  city: Anytown    
  state: CA   
  zip: 12345
person2:  
 name: Jane Smith  
 address:
  street: 123 Main St    
  city: Anytown    
  state: CA    
  zip: 12345
```
**Example 3: Reusing a Complex Structure**
```yaml
default_settings: &default_settings
 theme: dark
 font_size: 14
 notifications:
  email: true
  sms: false

user1:
 <<: *default_settings
 username: user1
 notifications:
  email: false

user2:
 <<: *default_settings
 username: user2
 font_size: 16
```
Without anchors and aliases:
```yaml
user1:  
 theme: dark  
 font_size: 14  
 notifications:    
  email: false    
  sms: false  
 username: user1

user2:  
 theme: dark  
 font_size: 16  
 notifications:    
  email: true    
  sms: false
 username: user2
```
### Multiline Strings:
- YAML supports multiline strings using the `|` character for block text and the `>` character for folded text.
```yaml
description: |
 This is a mutliline
 string with line breaks

summary: >
 This is a folded
 string where line breaks
 are converted to spaces.
```
## Data Types:
### 1. Scalars:
- Represent single values and include strings, numbers, booleans, null, dates, and timestamps.
#### Strings:
```yaml
name: John Doe
description: "This is a string with quotes."
```
#### Numbers:
```yaml
age: 30
height: 5.9
```
#### Booleans:
```yaml
is_active: true
is_disabled: false
```
#### Null:
```yaml
value: null
```
#### Dates and Timestamps:
```yaml
date_of_birth: 1990-01-01
timestamp: 2023-10-05T14:48:00Z
```
### 2. Sequences (Lists):
- Ordered collections of values, similar to arrays in programming languages.
#### Basic List:
```yaml
fruits:  
 - apple
 - banana  
 - cherry
```
#### Inline List:
```yaml
fruits: [apple, banana, cherry]
```
### 3. Mappings (Dictionaries):
- Mappings are collection of key-value pairs, similar to dictionaries in programming languages.
#### Basic Mapping:
```yaml
person:  
 name: John Doe  
 age: 30  
 is_active: true
```
#### Inline Mapping:
```yaml
person: {name: John Doe, age: 30, is_active: true}
```
### 4. Nested Structures:
- Nested structures enables creating complex data hierarchies.
#### Nested Mapping:
```yaml
person:  
 name: John Doe  
 age: 30  
 address:    
  street: 123 Main St    
  city: Anytown    
  state: CA    
  zip: 12345
```
#### Nested List:
```yaml
users:  
 - name: John Doe    
   age: 30  
 - name: Jane Smith
   age: 25
```
### 5. Multiline Strings:
[Multiline Strings](#multiline-strings)
### 6. Anchors and Aliases:
[Anchors and Aliases](#anchors-and-aliases)
### 7. Sets:
- Unordered collection of unique values
```yaml
unique_fruits: !!set
 ? apple
 ? banana
 ? cherry
```
