---
layout: archive
title: ""
permalink: /resources/
author_profile: false
--- 

# [<center>Resources</center>](#top)

<div style="width:100%; max-width:800px; margin:auto">  
<center><b><a class="body" href="https://eurisko-us.github.io/resources/#submit-assignment">Submit Assignment</a> • <a class="body" href="https://eurisko-us.github.io/resources/#honor-code">Honor Code</a> • <a class="body" href="https://eurisko-us.github.io/resources/#coding-commandments">Coding Commandments</a></b></center>  
</div>

## [<center>Submit Assignment</center>](#submit-assignment)

<div style="width:100%; max-width:800px; margin:auto"> 

<br>Before you submit your assignment, make sure that your code runs and satisfies ALL the requirements outlined in the assignment!<br><br>

<center><iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdwhanUMP5vbWSdGG7hBJdUswD_QUuN2QDeLeODLXKAkY9hhw/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading...</iframe></center>

</div>

## [<center>Honor Code</center>](#honor-code)

<div style="width:100%; max-width:800px; margin:auto"> 
  
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
</details>

</font>
  
</div>
