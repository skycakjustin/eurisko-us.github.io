---
layout: archive
title: ""
permalink: /resources/
author_profile: false
--- 

# [<center>Resources</center>](#top)

<div style="width:100%; max-width:800px; margin:auto">  
<center><b><a class="body" href="https://eurisko-us.github.io/resources/#submit-assignment">Submit Assignment</a> • <a class="body" href="https://eurisko-us.github.io/resources/#collaboration-policy">Collaboration Policy</a> • <a class="body" href="https://eurisko-us.github.io/resources/#coding-commandments">Coding Commandments</a></b></center>  
</div>

## [<center>Submit Assignment</center>](#submit-assignment)

<div style="width:100%; max-width:800px; margin:auto"> 

<br>Before you submit your assignment, make sure that your code runs, follows the <a class="body" href="https://eurisko-us.github.io/resources/#coding-commandments">coding commandments</a>, and satisfies ALL the requirements outlined in the assignment!<br><br>

<center><iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdwhanUMP5vbWSdGG7hBJdUswD_QUuN2QDeLeODLXKAkY9hhw/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading...</iframe></center>

</div>

## [<center>Collaboration Policy</center>](#collaboration-policy)

<div style="width:100%; max-width:800px; margin:auto"> 
  In general, you are free to get help from others on assignments. However, you are not allowed to copy (i.e. plagiarize) others' code. (If you copy code and then change the variable names, it's still plagiarism.) If I catch copied code, there will be consequences.
</div>

## [<center>Coding Commandments</center>](#coding-commandments)

<div style="width:100%; max-width:800px; margin:auto"> 

<b>You SHALL:</b>

<font size="3em">

<details>
  <summary>abide by Python conventions</summary>
  <ul>
    <li>variables, functions, and files use <code>snake_case</code></li>
    <li>classes use <code>PascalCase</code></li>
    <li>indents are 4 spaces</li>
  </ul>
</details>

<details>
  <summary>name things what they are</summary>
  <ul>
    <li>variables and classes should be nouns</li>
    <li>functions (including methods) should be verbs</li>
    <li>names should be descriptive. It's okay to make a name several words long if you need. For example, <code>compute_conditional_probability()</code> is WAY better than <code>cp()</code> or <code>prob()</code>.</li>
  </ul> 
</details>

</font>

<br><b>You shall NOT:</b>
<font size="3em">

<details>
  <summary>set a class attribute outside of the class itself</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  A = Matrix(elements = [[1,2], [3,4]])
  B = A.copy()
  B.elements.append([5,6])
  B.num_rows += 1
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  A = Matrix(elements = [[1,2], [3,4]])
  b_elements = A.elements
  b_elements.append([5,6])
  B = Matrix(elements = b_elements)
  </code></pre>
  <br>
</details>

<details>
  <summary>tailor general classes to specific problems</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  poly_regress = PolynomialRegressor()
  poly_regress.ingest_data(sandwich_data)
  poly_regress.solve_coefficients(sandwich_situation = True)
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Do the analysis manually, without the class PolynomialRegressor.
  You can still use code from the class, but you should not actually modify the class.
  </code></pre>
  <br>
</details>

<details>
  <summary>use inheritance in the absence of an "is-a" relationship</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  class Board(Player):
   ...

  (the Board is NOT a Player)
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  class Board:
   ...
  </code></pre>
  <br>
</details>

<details>
  <summary>give two methods similar and non-descriptive names</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  def move():
   ...

  def movement():
   ...
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  def move():
   ...

  def get_previous_movement():
   ...
  </code></pre>
  <br>
</details>

<details>
  <summary>have a single function with two purposes</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  calc_median_or_mean(which="median")
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Use two different functions:

  calc_median()
  calc_mean()
  </code></pre>
  <br>
</details>

<details>
  <summary>use a long list comprehension</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  flips = ' '.join([''.join([['T','H'][round(random.random())] for _ in range(num_flips_per_sample)]) for _ in range(num_samples)]
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Break it up.

  flips = ''
  for _ in range(num_samples):
       sample = ''
       for _ in range(num_flips_per_sample):
            random_flip_is_heads = round(random.random())
            random_flip = ['H', 'T'][random_flip_is_heads]
            sample += random_flip
       flips += ' ' + sample"
  </code></pre>
  <br>
</details>

<details>
  <summary>reference object attributes indirectly</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  "combat_stats = {
       'attack': unit1_attack,
       'defense': unit1_defense,
       'opponent_attack': unit2_attack,
       'opponent_defense': unit2_defense
  }
  if combat_stats['attack'] > combat_stats['opponent_defense']:
       print('hit!')
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Use the object directly.

  if unit1.attack_strength > unit2_defense_strength:
       print('hit!')
  </code></pre>
  <br>
</details>

<details>
  <summary>use arrays to store nonhomogenous data</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  sample_stats = ['HHT', 2/3, 1/3]
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Use a dictionary:

  sample_stats = {
       'flips': 'HHT',
       'proportion_heads': 2/3,
       'proportion_tails': 1/3
  }
  </code></pre>
  <br>
</details>

<details>
  <summary>waste other people's time</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  you get an error, and you think about for 30 seconds, and then you post about it asking for help
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  do all that you can to figure out the error before asking for help
  1. google the error!
  2. keep clicking on links until  everything you've read starts to sound like something you read previously
  3. walk away from the problem and then come back to it later
  4. if you still can't figure it out, then write up a post on discord. Include the following:
        * the error
        * the part of your code
        * the things that you've tried. This is really important for the following reasons:
              1. rubber ducky test (teddy bear test)
              2. so other people don't think you're wasting their time
  </code></pre>
  <br>
</details>

<details>
  <summary>waste your own time</summary>
  <br><font color="red"><b>Don't do this:</b></font>
  <pre><code>
  spending 2 hours messing around with broken code when you've already tried everything you can think of
  </code></pre>
  
  <font color="green"><b>Do this instead:</b></font>
  <pre><code>
  Walk away from the problem and then come back to it later. If you still can't figure it out, then make a post for help (that includes mention of all the things you've tried).
  </code></pre>
  <br>
</details>

</font>
  
</div>
