+++
title = "Markdown Test"
description = "A markdown test"
date = 2023-09-27
+++

Markdown test


## Headings

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragraphs
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Mollis nunc sed id semper. Vulputate mi sit amet mauris. Nunc eget lorem dolor sed. Elementum tempus egestas sed sed risus pretium quam. Duis at tellus at urna condimentum mattis pellentesque. Urna porttitor rhoncus dolor purus non enim. Et tortor consequat id porta nibh. Viverra adipiscing at in tellus. Non odio euismod lacinia at. Vitae sapien pellentesque habitant morbi tristique senectus et netus et. Amet est placerat in egestas erat imperdiet sed euismod. Pharetra magna ac placerat vestibulum lectus mauris ultrices eros in. Nam libero justo laoreet sit amet cursus sit. Suscipit tellus mauris a diam maecenas sed enim ut sem.

{% aside(float="right") %}
Mauris in aliquam sem fringilla ut morbi tincidunt augue. Volutpat odio facilisis mauris sit amet massa. Pulvinar etiam non quam lacus suspendisse faucibus interdum posuere. Arcu cursus vitae congue mauris rhoncus aenean vel elit. 
{% end %}
Leo vel fringilla est ullamcorper eget nulla facilisi etiam. Lacinia quis vel eros donec ac odio tempor. Amet porttitor eget dolor morbi non. Ut enim blandit volutpat maecenas volutpat blandit. Id faucibus nisl tincidunt eget. Tellus molestie nunc non blandit massa enim nec. Turpis cursus in hac habitasse. Suscipit adipiscing bibendum est ultricies integer quis auctor. At urna condimentum mattis pellentesque id. Velit dignissim sodales ut eu.

## Images

{% figure(src="/img/photo.png") %}
A cute corgi! Image courtesy of [Nataliya Vaitkevich](https://www.pexels.com/@n-voitkevich/).
{% end %}

## Videos

{{ vid(src="/vid/corgi.webm") }}
Video courtesy of [Ron Lach](https://www.pexels.com/@ron-lach/).

## Blockquote

{% quote(author="Cave Johnson") %}
When life gives you lemons? Don't make lemonade. Make life take the lemons back! Get mad! 'I don't want your damn lemons! What am I supposed to do with these?' Demand to see life's manager! Make life rue the day it thought it could give Cave Johnson lemons! Do you know who I am? I'm the man who's going to burn your house down! With the lemons! I'm going to get my engineers to invent a combustible lemon that burns your house down!
{% end %}

## Code

### Inline
`sudo rm -rf /`

### Block
```rust
use std::io;
use rand::Rng;

fn main() {
    let range = 1..=10;
    let mut rng = rand::thread_rng();
    let random_num: u8 = rng.gen_range(range.clone());

    println!("Enter a number between 1 and 10!");

    let mut guess_string = String::new();
    io::stdin().read_line(&mut guess_string).expect("Read failed");
    let guess_num: u8 = guess_string.trim().parse().expect("Not a valid number");

    if guess_num == random_num {
        println!("Correct!");
    } else if range.contains(&guess_num) {
        println!("Incorrect!")
    } else {
        println!("Not in range!");
    }
}
```


## Tables

Left Column | Right Column
----------- | ------------
Left Cell 1 | Right Cell 1
Left Cell 2 | Right Cell 2
  
<br/>
<table>
  <tr>
    <th>Top Row</th>
    <td>Top Cell</td>
  </tr>
  <tr>
    <th>Bottom Row</th>
    <td>Bottom Cell</td>
  </tr>
</table>

<br/>
<table>
  <tr>
    <th></th>
    <th>Column 1</th>
    <th>Column 2</th>
    <th>Column 3</th>
  </tr>
  <tr>
    <th scope="row">Row 1</th>
    <td>1+1</td>
    <td>1+2</td>
    <td>1+3</td>
  </tr>
  <tr>
    <th>Row 2</th>
    <td>2+1</td>
    <td>2+2</td>
    <td>2+3</td>
  </tr>
  <tr>
    <th>Row 3</th>
    <td>3+1</td>
    <td>3+2</td>
    <td>3+3</td>
  </tr>
</table>

## Lists
### Ordered
1. Item 1
2. Item 2
3. Item 3

### Unordered
- Monica
- Erica
- Rita
  - Tina
    - Sandra
    - Mary
  - Jessica

## Misc.

<details>
  <summary>Details drop-down. Great for content warnings, spoilers, etc.</summary>
  ...Or for the perfect punchline delivery!
</details>



## Citations

Wild, dubious claim[^1]

[^1]: Vague, unreliable source