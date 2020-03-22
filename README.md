# neo4j

## Atividade Prática – Neo4j

Todas as perguntas e comandos estão documentadas no arquivo [Jupyter Notebook](https://github.com/cassiomedeiros/neo4j/blob/master/src/neo4j.ipynb).

Escolhi essa ferramenta por conta dos recursos gráficos que ela permite para documentar o código e visualisar as respostas dos comandos.

Orientações para instalar o Jupyter Notebook clique [aqui](https://jupyter.readthedocs.io/en/latest/install.html).

### Dependências

- [Python >= 3.6](https://www.python.org/downloads/)
- [py2neo](https://py2neo.org/v4/)

## Exercício 1- Retrieving Nodes

#### Exercise 1.1: Retrieve all nodes from the database


```python
execute_query("match (n) return n")
```
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>n</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'title': 'The Matrix', 'tagline': 'Welcome to...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>{'name': 'Keanu Reeves', 'born': 1964}</td>
    </tr>
    <tr>
      <th>2</th>
      <td>{'name': 'Carrie-Anne Moss', 'born': 1967}</td>
    </tr>
    <tr>
      <th>3</th>
      <td>{'name': 'Laurence Fishburne', 'born': 1961}</td>
    </tr>
    <tr>
      <th>4</th>
      <td>{'name': 'Hugo Weaving', 'born': 1960}</td>
    </tr>
    <tr>
      <th>5</th>
      <td>{'name': 'Lilly Wachowski', 'born': 1967}</td>
    </tr>
    <tr>
      <th>6</th>
      <td>{'name': 'Lana Wachowski', 'born': 1965}</td>
    </tr>
    <tr>
      <th>7</th>
      <td>{'name': 'Joel Silver', 'born': 1952}</td>
    </tr>
    <tr>
      <th>8</th>
      <td>{'name': 'Emil Eifrem', 'born': 1978}</td>
    </tr>
    <tr>
      <th>9</th>
      <td>{'title': 'The Matrix Reloaded', 'tagline': 'F...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>{'title': 'The Matrix Revolutions', 'tagline':...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>{'title': 'The Devil's Advocate', 'tagline': '...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>{'name': 'Charlize Theron', 'born': 1975}</td>
    </tr>
    <tr>
      <th>13</th>
      <td>{'name': 'Al Pacino', 'born': 1940}</td>
    </tr>
    <tr>
      <th>14</th>
      <td>{'name': 'Taylor Hackford', 'born': 1944}</td>
    </tr>
    <tr>
      <th>15</th>
      <td>{'title': 'A Few Good Men', 'tagline': 'In the...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>{'name': 'Tom Cruise', 'born': 1962}</td>
    </tr>
    <tr>
      <th>17</th>
      <td>{'name': 'Jack Nicholson', 'born': 1937}</td>
    </tr>
    <tr>
      <th>18</th>
      <td>{'name': 'Demi Moore', 'born': 1962}</td>
    </tr>
    <tr>
      <th>19</th>
      <td>{'name': 'Kevin Bacon', 'born': 1958}</td>
    </tr>
    <tr>
      <th>20</th>
      <td>{'name': 'Kiefer Sutherland', 'born': 1966}</td>
    </tr>
    <tr>
      <th>21</th>
      <td>{'name': 'Noah Wyle', 'born': 1971}</td>
    </tr>
    <tr>
      <th>22</th>
      <td>{'name': 'Cuba Gooding Jr.', 'born': 1968}</td>
    </tr>
    <tr>
      <th>23</th>
      <td>{'name': 'Kevin Pollak', 'born': 1957}</td>
    </tr>
    <tr>
      <th>24</th>
      <td>{'name': 'J.T. Walsh', 'born': 1943}</td>
    </tr>
    <tr>
      <th>25</th>
      <td>{'name': 'James Marshall', 'born': 1967}</td>
    </tr>
    <tr>
      <th>26</th>
      <td>{'name': 'Christopher Guest', 'born': 1948}</td>
    </tr>
    <tr>
      <th>27</th>
      <td>{'name': 'Rob Reiner', 'born': 1947}</td>
    </tr>
    <tr>
      <th>28</th>
      <td>{'name': 'Aaron Sorkin', 'born': 1961}</td>
    </tr>
    <tr>
      <th>29</th>
      <td>{'title': 'Top Gun', 'tagline': 'I feel the ne...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>141</th>
      <td>{'title': 'Hoffa', 'tagline': 'He didn't want ...</td>
    </tr>
    <tr>
      <th>142</th>
      <td>{'name': 'Danny DeVito', 'born': 1944}</td>
    </tr>
    <tr>
      <th>143</th>
      <td>{'name': 'John C. Reilly', 'born': 1965}</td>
    </tr>
    <tr>
      <th>144</th>
      <td>{'title': 'Apollo 13', 'tagline': 'Houston, we...</td>
    </tr>
    <tr>
      <th>145</th>
      <td>{'name': 'Ed Harris', 'born': 1950}</td>
    </tr>
    <tr>
      <th>146</th>
      <td>{'name': 'Bill Paxton', 'born': 1955}</td>
    </tr>
    <tr>
      <th>147</th>
      <td>{'title': 'Twister', 'tagline': 'Don't Breathe...</td>
    </tr>
    <tr>
      <th>148</th>
      <td>{'name': 'Philip Seymour Hoffman', 'born': 1967}</td>
    </tr>
    <tr>
      <th>149</th>
      <td>{'name': 'Jan de Bont', 'born': 1943}</td>
    </tr>
    <tr>
      <th>150</th>
      <td>{'title': 'Cast Away', 'tagline': 'At the edge...</td>
    </tr>
    <tr>
      <th>151</th>
      <td>{'name': 'Robert Zemeckis', 'born': 1951}</td>
    </tr>
    <tr>
      <th>152</th>
      <td>{'title': 'One Flew Over the Cuckoo's Nest', '...</td>
    </tr>
    <tr>
      <th>153</th>
      <td>{'name': 'Milos Forman', 'born': 1932}</td>
    </tr>
    <tr>
      <th>154</th>
      <td>{'title': 'Something's Gotta Give', 'released'...</td>
    </tr>
    <tr>
      <th>155</th>
      <td>{'name': 'Diane Keaton', 'born': 1946}</td>
    </tr>
    <tr>
      <th>156</th>
      <td>{'name': 'Nancy Meyers', 'born': 1949}</td>
    </tr>
    <tr>
      <th>157</th>
      <td>{'title': 'Bicentennial Man', 'tagline': 'One ...</td>
    </tr>
    <tr>
      <th>158</th>
      <td>{'name': 'Chris Columbus', 'born': 1958}</td>
    </tr>
    <tr>
      <th>159</th>
      <td>{'title': 'Charlie Wilson's War', 'tagline': '...</td>
    </tr>
    <tr>
      <th>160</th>
      <td>{'name': 'Julia Roberts', 'born': 1967}</td>
    </tr>
    <tr>
      <th>161</th>
      <td>{'title': 'The Polar Express', 'tagline': 'Thi...</td>
    </tr>
    <tr>
      <th>162</th>
      <td>{'title': 'A League of Their Own', 'tagline': ...</td>
    </tr>
    <tr>
      <th>163</th>
      <td>{'name': 'Madonna', 'born': 1954}</td>
    </tr>
    <tr>
      <th>164</th>
      <td>{'name': 'Geena Davis', 'born': 1956}</td>
    </tr>
    <tr>
      <th>165</th>
      <td>{'name': 'Lori Petty', 'born': 1963}</td>
    </tr>
    <tr>
      <th>166</th>
      <td>{'name': 'Penny Marshall', 'born': 1943}</td>
    </tr>
    <tr>
      <th>167</th>
      <td>{'name': 'Paul Blythe'}</td>
    </tr>
    <tr>
      <th>168</th>
      <td>{'name': 'Angela Scope'}</td>
    </tr>
    <tr>
      <th>169</th>
      <td>{'name': 'Jessica Thompson'}</td>
    </tr>
    <tr>
      <th>170</th>
      <td>{'name': 'James Thompson'}</td>
    </tr>
  </tbody>
</table>
<p>171 rows × 1 columns</p>
</div>



#### Exercise 1.2: Examine the data model for the graph


```python
execute_query('CALL db.schema()')
```



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodes</th>
      <th>relationships</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[{'indexes': [], 'name': 'Movie', 'constraints...</td>
      <td>[{}, {}, {}, {}, {}, {}]</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 1.3: Retrieve all Person nodes.


```python
execute_query("match (p:Person) return p.name, p.born")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p.born</th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1964.0</td>
      <td>Keanu Reeves</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1967.0</td>
      <td>Carrie-Anne Moss</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1961.0</td>
      <td>Laurence Fishburne</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1960.0</td>
      <td>Hugo Weaving</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1967.0</td>
      <td>Lilly Wachowski</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1965.0</td>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1952.0</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1978.0</td>
      <td>Emil Eifrem</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1975.0</td>
      <td>Charlize Theron</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1940.0</td>
      <td>Al Pacino</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1944.0</td>
      <td>Taylor Hackford</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1962.0</td>
      <td>Tom Cruise</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1937.0</td>
      <td>Jack Nicholson</td>
    </tr>
    <tr>
      <th>13</th>
      <td>1962.0</td>
      <td>Demi Moore</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1958.0</td>
      <td>Kevin Bacon</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1966.0</td>
      <td>Kiefer Sutherland</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1971.0</td>
      <td>Noah Wyle</td>
    </tr>
    <tr>
      <th>17</th>
      <td>1968.0</td>
      <td>Cuba Gooding Jr.</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1957.0</td>
      <td>Kevin Pollak</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1943.0</td>
      <td>J.T. Walsh</td>
    </tr>
    <tr>
      <th>20</th>
      <td>1967.0</td>
      <td>James Marshall</td>
    </tr>
    <tr>
      <th>21</th>
      <td>1948.0</td>
      <td>Christopher Guest</td>
    </tr>
    <tr>
      <th>22</th>
      <td>1947.0</td>
      <td>Rob Reiner</td>
    </tr>
    <tr>
      <th>23</th>
      <td>1961.0</td>
      <td>Aaron Sorkin</td>
    </tr>
    <tr>
      <th>24</th>
      <td>1957.0</td>
      <td>Kelly McGillis</td>
    </tr>
    <tr>
      <th>25</th>
      <td>1959.0</td>
      <td>Val Kilmer</td>
    </tr>
    <tr>
      <th>26</th>
      <td>1962.0</td>
      <td>Anthony Edwards</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1933.0</td>
      <td>Tom Skerritt</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1961.0</td>
      <td>Meg Ryan</td>
    </tr>
    <tr>
      <th>29</th>
      <td>1944.0</td>
      <td>Tony Scott</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>103</th>
      <td>NaN</td>
      <td>Naomie Harris</td>
    </tr>
    <tr>
      <th>104</th>
      <td>1957.0</td>
      <td>Michael Clarke Duncan</td>
    </tr>
    <tr>
      <th>105</th>
      <td>1953.0</td>
      <td>David Morse</td>
    </tr>
    <tr>
      <th>106</th>
      <td>1968.0</td>
      <td>Sam Rockwell</td>
    </tr>
    <tr>
      <th>107</th>
      <td>1955.0</td>
      <td>Gary Sinise</td>
    </tr>
    <tr>
      <th>108</th>
      <td>1959.0</td>
      <td>Patricia Clarkson</td>
    </tr>
    <tr>
      <th>109</th>
      <td>1959.0</td>
      <td>Frank Darabont</td>
    </tr>
    <tr>
      <th>110</th>
      <td>1938.0</td>
      <td>Frank Langella</td>
    </tr>
    <tr>
      <th>111</th>
      <td>1969.0</td>
      <td>Michael Sheen</td>
    </tr>
    <tr>
      <th>112</th>
      <td>1960.0</td>
      <td>Oliver Platt</td>
    </tr>
    <tr>
      <th>113</th>
      <td>1944.0</td>
      <td>Danny DeVito</td>
    </tr>
    <tr>
      <th>114</th>
      <td>1965.0</td>
      <td>John C. Reilly</td>
    </tr>
    <tr>
      <th>115</th>
      <td>1950.0</td>
      <td>Ed Harris</td>
    </tr>
    <tr>
      <th>116</th>
      <td>1955.0</td>
      <td>Bill Paxton</td>
    </tr>
    <tr>
      <th>117</th>
      <td>1967.0</td>
      <td>Philip Seymour Hoffman</td>
    </tr>
    <tr>
      <th>118</th>
      <td>1943.0</td>
      <td>Jan de Bont</td>
    </tr>
    <tr>
      <th>119</th>
      <td>1951.0</td>
      <td>Robert Zemeckis</td>
    </tr>
    <tr>
      <th>120</th>
      <td>1932.0</td>
      <td>Milos Forman</td>
    </tr>
    <tr>
      <th>121</th>
      <td>1946.0</td>
      <td>Diane Keaton</td>
    </tr>
    <tr>
      <th>122</th>
      <td>1949.0</td>
      <td>Nancy Meyers</td>
    </tr>
    <tr>
      <th>123</th>
      <td>1958.0</td>
      <td>Chris Columbus</td>
    </tr>
    <tr>
      <th>124</th>
      <td>1967.0</td>
      <td>Julia Roberts</td>
    </tr>
    <tr>
      <th>125</th>
      <td>1954.0</td>
      <td>Madonna</td>
    </tr>
    <tr>
      <th>126</th>
      <td>1956.0</td>
      <td>Geena Davis</td>
    </tr>
    <tr>
      <th>127</th>
      <td>1963.0</td>
      <td>Lori Petty</td>
    </tr>
    <tr>
      <th>128</th>
      <td>1943.0</td>
      <td>Penny Marshall</td>
    </tr>
    <tr>
      <th>129</th>
      <td>NaN</td>
      <td>Paul Blythe</td>
    </tr>
    <tr>
      <th>130</th>
      <td>NaN</td>
      <td>Angela Scope</td>
    </tr>
    <tr>
      <th>131</th>
      <td>NaN</td>
      <td>Jessica Thompson</td>
    </tr>
    <tr>
      <th>132</th>
      <td>NaN</td>
      <td>James Thompson</td>
    </tr>
  </tbody>
</table>
<p>133 rows × 2 columns</p>
</div>



### Exercise 1.4: Retrieve all Movie nodes


```python
execute_query("MATCH (m:Movie) RETURN m.title, m.tagline, m.released")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.released</th>
      <th>m.tagline</th>
      <th>m.title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1999</td>
      <td>Welcome to the Real World</td>
      <td>The Matrix</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2003</td>
      <td>Free your mind</td>
      <td>The Matrix Reloaded</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2003</td>
      <td>Everything that has a beginning has an end</td>
      <td>The Matrix Revolutions</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1997</td>
      <td>Evil has its winning ways</td>
      <td>The Devil's Advocate</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1992</td>
      <td>In the heart of the nation's capital, in a cou...</td>
      <td>A Few Good Men</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1986</td>
      <td>I feel the need, the need for speed.</td>
      <td>Top Gun</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2000</td>
      <td>The rest of his life begins now.</td>
      <td>Jerry Maguire</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1986</td>
      <td>For some, it's the last real taste of innocenc...</td>
      <td>Stand By Me</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1997</td>
      <td>A comedy from the heart that goes for the throat.</td>
      <td>As Good as It Gets</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1998</td>
      <td>After life there is more. The end is just the ...</td>
      <td>What Dreams May Come</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1999</td>
      <td>First loves last. Forever.</td>
      <td>Snow Falling on Cedars</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1998</td>
      <td>At odds in life... in love on-line.</td>
      <td>You've Got Mail</td>
    </tr>
    <tr>
      <th>12</th>
      <td>1993</td>
      <td>What if someone you never met, someone you nev...</td>
      <td>Sleepless in Seattle</td>
    </tr>
    <tr>
      <th>13</th>
      <td>1990</td>
      <td>A story of love, lava and burning desire.</td>
      <td>Joe Versus the Volcano</td>
    </tr>
    <tr>
      <th>14</th>
      <td>1998</td>
      <td>At odds in life... in love on-line.</td>
      <td>When Harry Met Sally</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1996</td>
      <td>In every life there comes a time when that thi...</td>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2000</td>
      <td>Pain heals, Chicks dig scars... Glory lasts fo...</td>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2006</td>
      <td>Based on the extraordinary true story of one m...</td>
      <td>RescueDawn</td>
    </tr>
    <tr>
      <th>18</th>
      <td>1996</td>
      <td>Come as you are</td>
      <td>The Birdcage</td>
    </tr>
    <tr>
      <th>19</th>
      <td>1992</td>
      <td>It's a hell of a thing, killing a man</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>20</th>
      <td>1995</td>
      <td>The hottest data on earth. In the coolest head...</td>
      <td>Johnny Mnemonic</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2012</td>
      <td>Everything is connected</td>
      <td>Cloud Atlas</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2006</td>
      <td>Break The Codes</td>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2006</td>
      <td>Freedom! Forever!</td>
      <td>V for Vendetta</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2008</td>
      <td>Speed has no limits</td>
      <td>Speed Racer</td>
    </tr>
    <tr>
      <th>25</th>
      <td>2009</td>
      <td>Prepare to enter a secret world of assassins</td>
      <td>Ninja Assassin</td>
    </tr>
    <tr>
      <th>26</th>
      <td>1999</td>
      <td>Walk a mile you'll never forget.</td>
      <td>The Green Mile</td>
    </tr>
    <tr>
      <th>27</th>
      <td>2008</td>
      <td>400 million people were waiting for the truth.</td>
      <td>Frost/Nixon</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1992</td>
      <td>He didn't want law. He wanted justice.</td>
      <td>Hoffa</td>
    </tr>
    <tr>
      <th>29</th>
      <td>1995</td>
      <td>Houston, we have a problem.</td>
      <td>Apollo 13</td>
    </tr>
    <tr>
      <th>30</th>
      <td>1996</td>
      <td>Don't Breathe. Don't Look Back.</td>
      <td>Twister</td>
    </tr>
    <tr>
      <th>31</th>
      <td>2000</td>
      <td>At the edge of the world, his journey begins.</td>
      <td>Cast Away</td>
    </tr>
    <tr>
      <th>32</th>
      <td>1975</td>
      <td>If he's crazy, what does that make you?</td>
      <td>One Flew Over the Cuckoo's Nest</td>
    </tr>
    <tr>
      <th>33</th>
      <td>2003</td>
      <td>None</td>
      <td>Something's Gotta Give</td>
    </tr>
    <tr>
      <th>34</th>
      <td>1999</td>
      <td>One robot's 200 year journey to become an ordi...</td>
      <td>Bicentennial Man</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2007</td>
      <td>A stiff drink. A little mascara. A lot of nerv...</td>
      <td>Charlie Wilson's War</td>
    </tr>
    <tr>
      <th>36</th>
      <td>2004</td>
      <td>This Holiday Season… Believe</td>
      <td>The Polar Express</td>
    </tr>
    <tr>
      <th>37</th>
      <td>1992</td>
      <td>Once in a lifetime you get a chance to do some...</td>
      <td>A League of Their Own</td>
    </tr>
  </tbody>
</table>
</div>



## Exercicio 2 – Filtering queries using property values

#### Exercise 2.1: Retrieve all movies that were released in a specific year.


```python
execute_query("match (m:Movie {released: 2003}) return m").values
```




    array([[(_9:Movie {released: 2003, tagline: 'Free your mind', title: 'The Matrix Reloaded'})],
           [(_10:Movie {released: 2003, tagline: 'Everything that has a beginning has an end', title: 'The Matrix Revolutions'})],
           [(_154:Movie {released: 2003, title: "Something's Gotta Give"})]],
          dtype=object)



#### Exercise 2.2: View the retrieved results as a table


```python
execute_query("match (m:Movie {released: 2003}) return m.title, m.tagline, m.released")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.released</th>
      <th>m.tagline</th>
      <th>m.title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2003</td>
      <td>Free your mind</td>
      <td>The Matrix Reloaded</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2003</td>
      <td>Everything that has a beginning has an end</td>
      <td>The Matrix Revolutions</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2003</td>
      <td>None</td>
      <td>Something's Gotta Give</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 2.3: Query the database for all property keys


```python
execute_query('call db.propertyKeys')
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>propertyKey</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tagline</td>
    </tr>
    <tr>
      <th>1</th>
      <td>title</td>
    </tr>
    <tr>
      <th>2</th>
      <td>released</td>
    </tr>
    <tr>
      <th>3</th>
      <td>born</td>
    </tr>
    <tr>
      <th>4</th>
      <td>name</td>
    </tr>
    <tr>
      <th>5</th>
      <td>roles</td>
    </tr>
    <tr>
      <th>6</th>
      <td>summary</td>
    </tr>
    <tr>
      <th>7</th>
      <td>rating</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 2.4: Retrieve all Movies released in a specific year, returning their titles.


```python
execute_query('match (m:Movie {released: 2006}) return m.title')
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>RescueDawn</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>2</th>
      <td>V for Vendetta</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 2.5: Display title, released, and tagline values for every Movie node in the graph.


```python
execute_query('match (m:Movie {released: 2006}) return m.title, m.released, m.taglines')
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.released</th>
      <th>m.taglines</th>
      <th>m.title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2006</td>
      <td>None</td>
      <td>RescueDawn</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2006</td>
      <td>None</td>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2006</td>
      <td>None</td>
      <td>V for Vendetta</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 2.6: Display more user-friendly headers in the table


```python
execute_query("""match (m:Movie)
                 return m.title as `Movie Title`, 
                        m.released as Released, 
                        m.tagline as `Tag Line`""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie Title</th>
      <th>Released</th>
      <th>Tag Line</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Matrix</td>
      <td>1999</td>
      <td>Welcome to the Real World</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Matrix Reloaded</td>
      <td>2003</td>
      <td>Free your mind</td>
    </tr>
    <tr>
      <th>2</th>
      <td>The Matrix Revolutions</td>
      <td>2003</td>
      <td>Everything that has a beginning has an end</td>
    </tr>
    <tr>
      <th>3</th>
      <td>The Devil's Advocate</td>
      <td>1997</td>
      <td>Evil has its winning ways</td>
    </tr>
    <tr>
      <th>4</th>
      <td>A Few Good Men</td>
      <td>1992</td>
      <td>In the heart of the nation's capital, in a cou...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Top Gun</td>
      <td>1986</td>
      <td>I feel the need, the need for speed.</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jerry Maguire</td>
      <td>2000</td>
      <td>The rest of his life begins now.</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Stand By Me</td>
      <td>1986</td>
      <td>For some, it's the last real taste of innocenc...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>As Good as It Gets</td>
      <td>1997</td>
      <td>A comedy from the heart that goes for the throat.</td>
    </tr>
    <tr>
      <th>9</th>
      <td>What Dreams May Come</td>
      <td>1998</td>
      <td>After life there is more. The end is just the ...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Snow Falling on Cedars</td>
      <td>1999</td>
      <td>First loves last. Forever.</td>
    </tr>
    <tr>
      <th>11</th>
      <td>You've Got Mail</td>
      <td>1998</td>
      <td>At odds in life... in love on-line.</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Sleepless in Seattle</td>
      <td>1993</td>
      <td>What if someone you never met, someone you nev...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Joe Versus the Volcano</td>
      <td>1990</td>
      <td>A story of love, lava and burning desire.</td>
    </tr>
    <tr>
      <th>14</th>
      <td>When Harry Met Sally</td>
      <td>1998</td>
      <td>At odds in life... in love on-line.</td>
    </tr>
    <tr>
      <th>15</th>
      <td>That Thing You Do</td>
      <td>1996</td>
      <td>In every life there comes a time when that thi...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>The Replacements</td>
      <td>2000</td>
      <td>Pain heals, Chicks dig scars... Glory lasts fo...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>RescueDawn</td>
      <td>2006</td>
      <td>Based on the extraordinary true story of one m...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>The Birdcage</td>
      <td>1996</td>
      <td>Come as you are</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Unforgiven</td>
      <td>1992</td>
      <td>It's a hell of a thing, killing a man</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Johnny Mnemonic</td>
      <td>1995</td>
      <td>The hottest data on earth. In the coolest head...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Cloud Atlas</td>
      <td>2012</td>
      <td>Everything is connected</td>
    </tr>
    <tr>
      <th>22</th>
      <td>The Da Vinci Code</td>
      <td>2006</td>
      <td>Break The Codes</td>
    </tr>
    <tr>
      <th>23</th>
      <td>V for Vendetta</td>
      <td>2006</td>
      <td>Freedom! Forever!</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Speed Racer</td>
      <td>2008</td>
      <td>Speed has no limits</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Ninja Assassin</td>
      <td>2009</td>
      <td>Prepare to enter a secret world of assassins</td>
    </tr>
    <tr>
      <th>26</th>
      <td>The Green Mile</td>
      <td>1999</td>
      <td>Walk a mile you'll never forget.</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Frost/Nixon</td>
      <td>2008</td>
      <td>400 million people were waiting for the truth.</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Hoffa</td>
      <td>1992</td>
      <td>He didn't want law. He wanted justice.</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Apollo 13</td>
      <td>1995</td>
      <td>Houston, we have a problem.</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Twister</td>
      <td>1996</td>
      <td>Don't Breathe. Don't Look Back.</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Cast Away</td>
      <td>2000</td>
      <td>At the edge of the world, his journey begins.</td>
    </tr>
    <tr>
      <th>32</th>
      <td>One Flew Over the Cuckoo's Nest</td>
      <td>1975</td>
      <td>If he's crazy, what does that make you?</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Something's Gotta Give</td>
      <td>2003</td>
      <td>None</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Bicentennial Man</td>
      <td>1999</td>
      <td>One robot's 200 year journey to become an ordi...</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Charlie Wilson's War</td>
      <td>2007</td>
      <td>A stiff drink. A little mascara. A lot of nerv...</td>
    </tr>
    <tr>
      <th>36</th>
      <td>The Polar Express</td>
      <td>2004</td>
      <td>This Holiday Season… Believe</td>
    </tr>
    <tr>
      <th>37</th>
      <td>A League of Their Own</td>
      <td>1992</td>
      <td>Once in a lifetime you get a chance to do some...</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 3 - Filtering queries using relationships

### Exercise 3.1: Display the schema of the database.


```python
execute_query("call db.schema").values
```




    array([[list([(_-5:Movie {constraints: [], indexes: [], name: 'Movie'}), (_-6:Person {constraints: [], indexes: [], name: 'Person'})]),
            list([(Person)-[:ACTED_IN {}]->(Movie), (Person)-[:REVIEWED {}]->(Movie), (Person)-[:PRODUCED {}]->(Movie), (Person)-[:WROTE {}]->(Movie), (Person)-[:FOLLOWS {}]->(Person), (Person)-[:DIRECTED {}]->(Movie)])]],
          dtype=object)



#### Exercise 3.2: Retrieve all people who wrote the movie Speed Racer.


```python
execute_query("match (p:Person)-[:WROTE]->(m:Movie {title: 'Speed Racer'}) return p.name as Person")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Lilly Wachowski</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 3.3: Retrieve all movies that are connected to the person, Tom Hanks.


```python
execute_query("match (m:Movie)<--(:Person {name: 'Tom Hanks'}) return m.title as Movie")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Apollo 13</td>
    </tr>
    <tr>
      <th>1</th>
      <td>You've Got Mail</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A League of Their Own</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Joe Versus the Volcano</td>
    </tr>
    <tr>
      <th>4</th>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>5</th>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Cloud Atlas</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Cast Away</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Green Mile</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Sleepless in Seattle</td>
    </tr>
    <tr>
      <th>10</th>
      <td>The Polar Express</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Charlie Wilson's War</td>
    </tr>
    <tr>
      <th>12</th>
      <td>That Thing You Do</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 3.4: Retrieve information about the relationships Tom Hankshad with the set of movies retrieved earlier


```python
execute_query("match (m:Movie)-[rel]-(:Person {name: 'Tom Hanks'}) return m.title as Movie, type(rel) as Relationships")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Relationships</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Apollo 13</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>You've Got Mail</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A League of Their Own</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Joe Versus the Volcano</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>That Thing You Do</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>The Da Vinci Code</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Cloud Atlas</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Cast Away</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Green Mile</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Sleepless in Seattle</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>The Polar Express</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Charlie Wilson's War</td>
      <td>ACTED_IN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>That Thing You Do</td>
      <td>DIRECTED</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 3.5: Retrieve information about the roles that Tom Hanks acted in.


```python
execute_query("match (m:Movie)-[rel:ACTED_IN]-(:Person {name: 'Tom Hanks'}) return m.title as Movie, rel.roles as Roles")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Roles</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Apollo 13</td>
      <td>[Jim Lovell]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>You've Got Mail</td>
      <td>[Joe Fox]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A League of Their Own</td>
      <td>[Jimmy Dugan]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Joe Versus the Volcano</td>
      <td>[Joe Banks]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>That Thing You Do</td>
      <td>[Mr. White]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>The Da Vinci Code</td>
      <td>[Dr. Robert Langdon]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Cloud Atlas</td>
      <td>[Zachry, Dr. Henry Goose, Isaac Sachs, Dermot ...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Cast Away</td>
      <td>[Chuck Noland]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Green Mile</td>
      <td>[Paul Edgecomb]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Sleepless in Seattle</td>
      <td>[Sam Baldwin]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>The Polar Express</td>
      <td>[Hero Boy, Father, Conductor, Hobo, Scrooge, S...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Charlie Wilson's War</td>
      <td>[Rep. Charlie Wilson]</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 4 – Filtering queries using WHERE clause

#### Exercise 4.1: Retrieve all movies that Tom Cruise acted in


```python
execute_query("match (m:Movie)-[:ACTED_IN]-(p:Person) where p.name = 'Tom Cruise' return m.title as Movie")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jerry Maguire</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Top Gun</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A Few Good Men</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.2: Retrieve all people that were born in the 70’s.


```python
execute_query("match (p:Person) where p.born >= 1970 and p.born < 1980 return p.name as Person")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Emil Eifrem</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Charlize Theron</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Noah Wyle</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Jerry O'Connell</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jay Mohr</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Regina King</td>
    </tr>
    <tr>
      <th>6</th>
      <td>River Phoenix</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Corey Feldman</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Wil Wheaton</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Ethan Hawke</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Rick Yune</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Dave Chappelle</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Liv Tyler</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Brooke Langton</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Christian Bale</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Audrey Tautou</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Paul Bettany</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.3: Retrieve the actors who acted in the movie The Matrix who were born after 1960.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie) 
                 where m.title = 'The Matrix' and p.born >= 1960 
                 return p.name as Actor, p.born as Born""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Born</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Emil Eifrem</td>
      <td>1978</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Hugo Weaving</td>
      <td>1960</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Laurence Fishburne</td>
      <td>1961</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Carrie-Anne Moss</td>
      <td>1967</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Keanu Reeves</td>
      <td>1964</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.4: Retrieve all movies by testing the node label and a property.


```python
execute_query("match (m) where m:Movie and m.released = 2000 return m.title as Movie")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jerry Maguire</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Cast Away</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.5: Retrieve all people that wrote movies by testing the relationship between two nodes.


```python
execute_query("""match (p)-[rel]->(m) 
                 where p:Person and type(rel) = 'WROTE' and m:Movie
                 return p.name as Person""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Aaron Sorkin</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jim Cash</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Cameron Crowe</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Nora Ephron</td>
    </tr>
    <tr>
      <th>4</th>
      <td>David Mitchell</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Lilly Wachowski</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Lilly Wachowski</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Nancy Meyers</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.6: Retrieve all people in the graph that do not have a property.


```python
execute_query("""match (p:Person)
                 where not exists(p.born)
                 return p.name as Person""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Naomie Harris</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Paul Blythe</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Angela Scope</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Jessica Thompson</td>
    </tr>
    <tr>
      <th>4</th>
      <td>James Thompson</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.7: Retrieve all people related to movies where the relationship has a property.


```python
execute_query("""match (p:Person)-[rel]->(m:Movie)
                 where exists(rel.rating)
                 return p.name as Person, m.title as Movie, rel.rating as Rating""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Person</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jerry Maguire</td>
      <td>Jessica Thompson</td>
      <td>92</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Replacements</td>
      <td>James Thompson</td>
      <td>100</td>
    </tr>
    <tr>
      <th>2</th>
      <td>The Replacements</td>
      <td>Angela Scope</td>
      <td>62</td>
    </tr>
    <tr>
      <th>3</th>
      <td>The Replacements</td>
      <td>Jessica Thompson</td>
      <td>65</td>
    </tr>
    <tr>
      <th>4</th>
      <td>The Birdcage</td>
      <td>Jessica Thompson</td>
      <td>45</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Unforgiven</td>
      <td>Jessica Thompson</td>
      <td>85</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Cloud Atlas</td>
      <td>Jessica Thompson</td>
      <td>95</td>
    </tr>
    <tr>
      <th>7</th>
      <td>The Da Vinci Code</td>
      <td>Jessica Thompson</td>
      <td>68</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Da Vinci Code</td>
      <td>James Thompson</td>
      <td>65</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.8: Retrieve all actors whose name begins with James.


```python
execute_query("match (p:Person) where p.name starts with 'James' return p.name as Actor")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Marshall</td>
    </tr>
    <tr>
      <th>1</th>
      <td>James L. Brooks</td>
    </tr>
    <tr>
      <th>2</th>
      <td>James Cromwell</td>
    </tr>
    <tr>
      <th>3</th>
      <td>James Thompson</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.9: Retrieve all REVIEW relationships from the graph with filtered results.


```python
execute_query("""match (:Person)-[r:REVIEWED]->(m:Movie)
                WHERE toLower(r.summary) contains 'fun'
                RETURN  m.title as Movie, r.summary as Review, r.rating as Rating""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Rating</th>
      <th>Review</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Replacements</td>
      <td>62</td>
      <td>Pretty funny at times</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Replacements</td>
      <td>65</td>
      <td>Silly, but fun</td>
    </tr>
    <tr>
      <th>2</th>
      <td>The Da Vinci Code</td>
      <td>65</td>
      <td>Fun, but a little far fetched</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.10: Retrieve all people who have produced a movie, but have not directed a movie.


```python
execute_query("""match (p:Person)-[:PRODUCED]->(m:Movie)
                 where not ((p)-[:DIRECTED]->(m)) return p.name as Person, m.title as Movie""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Matrix</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Matrix Reloaded</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>2</th>
      <td>The Matrix Revolutions</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>3</th>
      <td>When Harry Met Sally</td>
      <td>Nora Ephron</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Cloud Atlas</td>
      <td>Stefan Arndt</td>
    </tr>
    <tr>
      <th>5</th>
      <td>V for Vendetta</td>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>6</th>
      <td>V for Vendetta</td>
      <td>Lilly Wachowski</td>
    </tr>
    <tr>
      <th>7</th>
      <td>V for Vendetta</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Speed Racer</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Ninja Assassin</td>
      <td>Lana Wachowski</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Ninja Assassin</td>
      <td>Joel Silver</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Ninja Assassin</td>
      <td>Lilly Wachowski</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.11: Retrieve the movies and their actors where one of the actors also directed the movie.


```python
execute_query("""match (p1:Person)-[:ACTED_IN]->(m:Movie)<-[:ACTED_IN]-(p2:Person)
                 where exists ((p2)-[:DIRECTED]->(m)) 
                 return p1.name as Actor, m.title as Movie, p2.name as Director""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Director</th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Liv Tyler</td>
      <td>Tom Hanks</td>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Charlize Theron</td>
      <td>Tom Hanks</td>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Gene Hackman</td>
      <td>Clint Eastwood</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Richard Harris</td>
      <td>Clint Eastwood</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>4</th>
      <td>John C. Reilly</td>
      <td>Danny DeVito</td>
      <td>Hoffa</td>
    </tr>
    <tr>
      <th>5</th>
      <td>J.T. Walsh</td>
      <td>Danny DeVito</td>
      <td>Hoffa</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jack Nicholson</td>
      <td>Danny DeVito</td>
      <td>Hoffa</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.12: Retrieve all movies that were released in a set of years.


```python
execute_query("match (m:Movie) where m.released in [1999, 2007, 2000] return m.title as Movie, m.released as Released")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Released</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Matrix</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jerry Maguire</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Snow Falling on Cedars</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>3</th>
      <td>The Replacements</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>The Green Mile</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Cast Away</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Bicentennial Man</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Charlie Wilson's War</td>
      <td>2007</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 4.13: Retrieve the movies that have an actor’s role that is the name of the movie.


```python
execute_query("""match (p:Person)-[rel:ACTED_IN]-(m:Movie)
                 where m.title in rel.roles
                 return p.name as Person, m.title as Movie""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jerry Maguire</td>
      <td>Tom Cruise</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Johnny Mnemonic</td>
      <td>Keanu Reeves</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Speed Racer</td>
      <td>Emile Hirsch</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Hoffa</td>
      <td>Jack Nicholson</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 5 – Controlling query processing

#### Exercise 5.1: Retrieve data using multiple MATCH patterns

Write a Cypher query that retrieves all movies that Gene Hackman has acted it, along with the directors of the movies. In addition, retrieve the actors that acted in the same movies as Gene Hackman. Return the name of the movie, the name of the director, and the names of actors that worked with Gene Hackman.


```python
execute_query("""match (p1:Person)-[:ACTED_IN]->(m:Movie)<-[:DIRECTED]-(d:Person), (p2:Person)-[:ACTED_IN]->(m)
                 where p1.name = 'Gene Hackman'
                 return m.title as Movie, d.name as Director, p2.name as Actor
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Director</th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Clint Eastwood</td>
      <td>Clint Eastwood</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Richard Harris</td>
      <td>Clint Eastwood</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Robin Williams</td>
      <td>Mike Nichols</td>
      <td>The Birdcage</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Nathan Lane</td>
      <td>Mike Nichols</td>
      <td>The Birdcage</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Brooke Langton</td>
      <td>Howard Deutch</td>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Keanu Reeves</td>
      <td>Howard Deutch</td>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Orlando Jones</td>
      <td>Howard Deutch</td>
      <td>The Replacements</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.2: Retrieve particular nodes that have a relationship.

Retrieve all nodes that the person named James Thompson directly has the FOLLOWS relationship in either direction.


```python
execute_query("""match (p1:Person)-[:FOLLOWS]-(p2:Person)
                 where p1.name = 'James Thompson'
                 return p1.name, p2.name""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Thompson</td>
      <td>Jessica Thompson</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.3: Modify the query to retrieve nodes that are exactly three hops away.


```python
execute_query("""match (p1:Person)-[:FOLLOWS*3]-(p2:Person)
                 where p1.name = 'James Thompson'
                 return p1.name, p2.name""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Thompson</td>
      <td>Paul Blythe</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.4: Modify the query to retrieve nodes that are one and two hops away.


```python
execute_query("""match (p1:Person)-[:FOLLOWS*1..2]-(p2:Person)
                 where p1.name = 'James Thompson'
                 return p1.name, p2.name""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Thompson</td>
      <td>Jessica Thompson</td>
    </tr>
    <tr>
      <th>1</th>
      <td>James Thompson</td>
      <td>Angela Scope</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.5: Modify the query to retrieve particular nodes that are connected no matter how many hops are required.


```python
execute_query("""match (p1:Person)-[:FOLLOWS*]-(p2:Person)
                 where p1.name = 'James Thompson'
                 return p1.name, p2.name""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Thompson</td>
      <td>Jessica Thompson</td>
    </tr>
    <tr>
      <th>1</th>
      <td>James Thompson</td>
      <td>Angela Scope</td>
    </tr>
    <tr>
      <th>2</th>
      <td>James Thompson</td>
      <td>Paul Blythe</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.6: Specify optional data to be retrieved during the query.


```python
execute_query("""match (p:Person)
                 where p.name starts with 'James'
                 optional match (p)-[:DIRECTED]->(m:Movie)
                 return p.name as Person, m.title as Title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
      <th>Title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>James Marshall</td>
      <td>Ninja Assassin</td>
    </tr>
    <tr>
      <th>1</th>
      <td>James Marshall</td>
      <td>V for Vendetta</td>
    </tr>
    <tr>
      <th>2</th>
      <td>James L. Brooks</td>
      <td>As Good as It Gets</td>
    </tr>
    <tr>
      <th>3</th>
      <td>James Cromwell</td>
      <td>None</td>
    </tr>
    <tr>
      <th>4</th>
      <td>James Thompson</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.7: Retrieve nodes by collecting a list.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 return p.name as Actor, collect(m.title) as Movies
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Movies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Emil Eifrem</td>
      <td>[The Matrix]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Hugo Weaving</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Laurence Fishburne</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Carrie-Anne Moss</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Keanu Reeves</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Al Pacino</td>
      <td>[The Devil's Advocate]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Charlize Theron</td>
      <td>[The Devil's Advocate, That Thing You Do]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>James Marshall</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kevin Pollak</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>J.T. Walsh</td>
      <td>[A Few Good Men, Hoffa]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Aaron Sorkin</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Cuba Gooding Jr.</td>
      <td>[A Few Good Men, Jerry Maguire, As Good as It ...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Christopher Guest</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Noah Wyle</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Kiefer Sutherland</td>
      <td>[A Few Good Men, Stand By Me]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Kevin Bacon</td>
      <td>[A Few Good Men, Frost/Nixon, Apollo 13]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Demi Moore</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Jack Nicholson</td>
      <td>[A Few Good Men, As Good as It Gets, Hoffa, On...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Tom Cruise</td>
      <td>[A Few Good Men, Top Gun, Jerry Maguire]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Val Kilmer</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Meg Ryan</td>
      <td>[Top Gun, You've Got Mail, Sleepless in Seattl...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Tom Skerritt</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Kelly McGillis</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Anthony Edwards</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Jerry O'Connell</td>
      <td>[Jerry Maguire, Stand By Me]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Bonnie Hunt</td>
      <td>[Jerry Maguire, The Green Mile]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Jay Mohr</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Jonathan Lipnicki</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Renee Zellweger</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Kelly Preston</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>72</th>
      <td>Paul Bettany</td>
      <td>[The Da Vinci Code]</td>
    </tr>
    <tr>
      <th>73</th>
      <td>John Hurt</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>74</th>
      <td>Stephen Rea</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>75</th>
      <td>Natalie Portman</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>76</th>
      <td>Ben Miles</td>
      <td>[V for Vendetta, Speed Racer, Ninja Assassin]</td>
    </tr>
    <tr>
      <th>77</th>
      <td>Emile Hirsch</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>78</th>
      <td>Rain</td>
      <td>[Speed Racer, Ninja Assassin]</td>
    </tr>
    <tr>
      <th>79</th>
      <td>Christina Ricci</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>80</th>
      <td>Susan Sarandon</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>81</th>
      <td>John Goodman</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Matthew Fox</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Naomie Harris</td>
      <td>[Ninja Assassin]</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Sam Rockwell</td>
      <td>[The Green Mile, Frost/Nixon]</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Patricia Clarkson</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>86</th>
      <td>Michael Clarke Duncan</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>87</th>
      <td>David Morse</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Gary Sinise</td>
      <td>[The Green Mile, Apollo 13]</td>
    </tr>
    <tr>
      <th>89</th>
      <td>Michael Sheen</td>
      <td>[Frost/Nixon]</td>
    </tr>
    <tr>
      <th>90</th>
      <td>Frank Langella</td>
      <td>[Frost/Nixon]</td>
    </tr>
    <tr>
      <th>91</th>
      <td>Oliver Platt</td>
      <td>[Frost/Nixon, Bicentennial Man]</td>
    </tr>
    <tr>
      <th>92</th>
      <td>John C. Reilly</td>
      <td>[Hoffa]</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Danny DeVito</td>
      <td>[Hoffa, One Flew Over the Cuckoo's Nest]</td>
    </tr>
    <tr>
      <th>94</th>
      <td>Ed Harris</td>
      <td>[Apollo 13]</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Bill Paxton</td>
      <td>[Apollo 13, Twister, A League of Their Own]</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Philip Seymour Hoffman</td>
      <td>[Twister, Charlie Wilson's War]</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Diane Keaton</td>
      <td>[Something's Gotta Give]</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Julia Roberts</td>
      <td>[Charlie Wilson's War]</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Madonna</td>
      <td>[A League of Their Own]</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Geena Davis</td>
      <td>[A League of Their Own]</td>
    </tr>
    <tr>
      <th>101</th>
      <td>Lori Petty</td>
      <td>[A League of Their Own]</td>
    </tr>
  </tbody>
</table>
<p>102 rows × 2 columns</p>
</div>



#### Exercise 5.9: Retrieve nodes as lists and return data associated with the corresponding lists.


```python
execute_query("""match (p:Person)-[:REVIEWED]->(m:Movie)
                 return m.title as Movie, count(p) as NumReviews, collect(p.name) as Reviewers
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>NumReviews</th>
      <th>Reviewers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jerry Maguire</td>
      <td>1</td>
      <td>[Jessica Thompson]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Replacements</td>
      <td>3</td>
      <td>[James Thompson, Angela Scope, Jessica Thompson]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>The Birdcage</td>
      <td>1</td>
      <td>[Jessica Thompson]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Unforgiven</td>
      <td>1</td>
      <td>[Jessica Thompson]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Cloud Atlas</td>
      <td>1</td>
      <td>[Jessica Thompson]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>The Da Vinci Code</td>
      <td>2</td>
      <td>[Jessica Thompson, James Thompson]</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.10: Retrieve nodes and their relationships as lists.

Retrieve all directors, their movies, and people who acted in the movies, returning the name of the director, the number of actors the director has worked with, and the list of actors.


```python
execute_query("""match (d:Person)-[:DIRECTED]->(m:Movie)<-[:ACTED_IN]-(p:Person)
                 return m.title as Movie, d.name as Director, count(p.name) as `Number Actors`, collect(p.name) as Actors
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Director</th>
      <th>Movie</th>
      <th>Number Actors</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>Lana Wachowski</td>
      <td>The Matrix</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>Lilly Wachowski</td>
      <td>The Matrix</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>Lana Wachowski</td>
      <td>The Matrix Reloaded</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>Lilly Wachowski</td>
      <td>The Matrix Reloaded</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>Lana Wachowski</td>
      <td>The Matrix Revolutions</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>Lilly Wachowski</td>
      <td>The Matrix Revolutions</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Al Pacino, Charlize Theron, Keanu Reeves]</td>
      <td>Taylor Hackford</td>
      <td>The Devil's Advocate</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[James Marshall, Kevin Pollak, J.T. Walsh, Aar...</td>
      <td>Rob Reiner</td>
      <td>A Few Good Men</td>
      <td>12</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Val Kilmer, Meg Ryan, Tom Skerritt, Kelly McG...</td>
      <td>Tony Scott</td>
      <td>Top Gun</td>
      <td>6</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>Cameron Crowe</td>
      <td>Jerry Maguire</td>
      <td>9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Jerry O'Connell, River Phoenix, Marshall Bell...</td>
      <td>Rob Reiner</td>
      <td>Stand By Me</td>
      <td>7</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Helen Hunt, Jack Nicholson, Cuba Gooding Jr.,...</td>
      <td>James L. Brooks</td>
      <td>As Good as It Gets</td>
      <td>4</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Robin Williams, Cuba Gooding Jr., Max von Syd...</td>
      <td>Vincent Ward</td>
      <td>What Dreams May Come</td>
      <td>5</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Ethan Hawke, Rick Yune, Max von Sydow, James ...</td>
      <td>Scott Hicks</td>
      <td>Snow Falling on Cedars</td>
      <td>4</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Tom Hanks, Parker Posey, Greg Kinnear, Meg Ry...</td>
      <td>Nora Ephron</td>
      <td>You've Got Mail</td>
      <td>6</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Meg Ryan, Victor Garber, Tom Hanks, Bill Pull...</td>
      <td>Nora Ephron</td>
      <td>Sleepless in Seattle</td>
      <td>6</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Tom Hanks, Nathan Lane, Meg Ryan]</td>
      <td>John Patrick Stanley</td>
      <td>Joe Versus the Volcano</td>
      <td>3</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Carrie Fisher, Billy Crystal, Bruno Kirby, Me...</td>
      <td>Rob Reiner</td>
      <td>When Harry Met Sally</td>
      <td>4</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Tom Hanks, Liv Tyler, Charlize Theron]</td>
      <td>Tom Hanks</td>
      <td>That Thing You Do</td>
      <td>3</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Brooke Langton, Keanu Reeves, Orlando Jones, ...</td>
      <td>Howard Deutch</td>
      <td>The Replacements</td>
      <td>4</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Zach Grenier, Steve Zahn, Christian Bale, Mar...</td>
      <td>Werner Herzog</td>
      <td>RescueDawn</td>
      <td>4</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Robin Williams, Nathan Lane, Gene Hackman]</td>
      <td>Mike Nichols</td>
      <td>The Birdcage</td>
      <td>3</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Clint Eastwood, Gene Hackman, Richard Harris]</td>
      <td>Clint Eastwood</td>
      <td>Unforgiven</td>
      <td>3</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Ice-T, Dina Meyer, Keanu Reeves, Takeshi Kitano]</td>
      <td>Robert Longo</td>
      <td>Johnny Mnemonic</td>
      <td>4</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Tom Hanks, Jim Broadbent, Halle Berry, Hugo W...</td>
      <td>Tom Tykwer</td>
      <td>Cloud Atlas</td>
      <td>4</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Tom Hanks, Jim Broadbent, Halle Berry, Hugo W...</td>
      <td>Lana Wachowski</td>
      <td>Cloud Atlas</td>
      <td>4</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Tom Hanks, Jim Broadbent, Halle Berry, Hugo W...</td>
      <td>Lilly Wachowski</td>
      <td>Cloud Atlas</td>
      <td>4</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Tom Hanks, Ian McKellen, Audrey Tautou, Paul ...</td>
      <td>Ron Howard</td>
      <td>The Da Vinci Code</td>
      <td>4</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[John Hurt, Stephen Rea, Natalie Portman, Hugo...</td>
      <td>James Marshall</td>
      <td>V for Vendetta</td>
      <td>5</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Emile Hirsch, Rain, Christina Ricci, Ben Mile...</td>
      <td>Lana Wachowski</td>
      <td>Speed Racer</td>
      <td>7</td>
    </tr>
    <tr>
      <th>30</th>
      <td>[Emile Hirsch, Rain, Christina Ricci, Ben Mile...</td>
      <td>Lilly Wachowski</td>
      <td>Speed Racer</td>
      <td>7</td>
    </tr>
    <tr>
      <th>31</th>
      <td>[Rain, Ben Miles, Rick Yune, Naomie Harris]</td>
      <td>James Marshall</td>
      <td>Ninja Assassin</td>
      <td>4</td>
    </tr>
    <tr>
      <th>32</th>
      <td>[Sam Rockwell, Bonnie Hunt, Patricia Clarkson,...</td>
      <td>Frank Darabont</td>
      <td>The Green Mile</td>
      <td>8</td>
    </tr>
    <tr>
      <th>33</th>
      <td>[Sam Rockwell, Michael Sheen, Frank Langella, ...</td>
      <td>Ron Howard</td>
      <td>Frost/Nixon</td>
      <td>5</td>
    </tr>
    <tr>
      <th>34</th>
      <td>[John C. Reilly, Danny DeVito, J.T. Walsh, Jac...</td>
      <td>Danny DeVito</td>
      <td>Hoffa</td>
      <td>4</td>
    </tr>
    <tr>
      <th>35</th>
      <td>[Tom Hanks, Ed Harris, Gary Sinise, Kevin Baco...</td>
      <td>Ron Howard</td>
      <td>Apollo 13</td>
      <td>5</td>
    </tr>
    <tr>
      <th>36</th>
      <td>[Helen Hunt, Bill Paxton, Philip Seymour Hoffm...</td>
      <td>Jan de Bont</td>
      <td>Twister</td>
      <td>4</td>
    </tr>
    <tr>
      <th>37</th>
      <td>[Helen Hunt, Tom Hanks]</td>
      <td>Robert Zemeckis</td>
      <td>Cast Away</td>
      <td>2</td>
    </tr>
    <tr>
      <th>38</th>
      <td>[Danny DeVito, Jack Nicholson]</td>
      <td>Milos Forman</td>
      <td>One Flew Over the Cuckoo's Nest</td>
      <td>2</td>
    </tr>
    <tr>
      <th>39</th>
      <td>[Keanu Reeves, Diane Keaton, Jack Nicholson]</td>
      <td>Nancy Meyers</td>
      <td>Something's Gotta Give</td>
      <td>3</td>
    </tr>
    <tr>
      <th>40</th>
      <td>[Robin Williams, Oliver Platt]</td>
      <td>Chris Columbus</td>
      <td>Bicentennial Man</td>
      <td>2</td>
    </tr>
    <tr>
      <th>41</th>
      <td>[Julia Roberts, Tom Hanks, Philip Seymour Hoff...</td>
      <td>Mike Nichols</td>
      <td>Charlie Wilson's War</td>
      <td>3</td>
    </tr>
    <tr>
      <th>42</th>
      <td>[Tom Hanks]</td>
      <td>Robert Zemeckis</td>
      <td>The Polar Express</td>
      <td>1</td>
    </tr>
    <tr>
      <th>43</th>
      <td>[Tom Hanks, Madonna, Rosie O'Donnell, Geena Da...</td>
      <td>Penny Marshall</td>
      <td>A League of Their Own</td>
      <td>6</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.11: Retrieve the actors who have acted in exactly five movies.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 with p, count(m.title) as numberMovies
                 where numberMovies = 5
                 return p.name as Actor
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Hugo Weaving</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jack Nicholson</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Meg Ryan</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 5.12: Retrieve the movies that have at least 2 directors with other optional data.

Retrieve the movies that have at least 2 directors, and optionally the names of people who reviewed the movies.


```python
execute_query("""match (m:Movie)
                 with m, size((:Person)-[:DIRECTED]->(m)) as numberDirectors
                 where numberDirectors >= 2
                 optional match (p:Person)-[:REVIEWED]->(m)
                 return m.title as Movie, numberDirectors as Directors, p.name as Reviewers
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Directors</th>
      <th>Movie</th>
      <th>Reviewers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>The Matrix</td>
      <td>None</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>The Matrix Reloaded</td>
      <td>None</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>The Matrix Revolutions</td>
      <td>None</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>Cloud Atlas</td>
      <td>Jessica Thompson</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>Speed Racer</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 6 – Controlling results returned

#### Exercise 6.1: Execute a query that returns duplicate records.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 where m.released >= 1990 and m.released <= 2000
                 return distinct m.released as Released, m.title as Movie, collect(p.name) as Actors 
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Movie</th>
      <th>Released</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>The Matrix</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Al Pacino, Charlize Theron, Keanu Reeves]</td>
      <td>The Devil's Advocate</td>
      <td>1997</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[James Marshall, Kevin Pollak, J.T. Walsh, Aar...</td>
      <td>A Few Good Men</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>Jerry Maguire</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Helen Hunt, Jack Nicholson, Cuba Gooding Jr.,...</td>
      <td>As Good as It Gets</td>
      <td>1997</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Robin Williams, Cuba Gooding Jr., Max von Syd...</td>
      <td>What Dreams May Come</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Ethan Hawke, Rick Yune, Max von Sydow, James ...</td>
      <td>Snow Falling on Cedars</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Tom Hanks, Parker Posey, Greg Kinnear, Meg Ry...</td>
      <td>You've Got Mail</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Meg Ryan, Victor Garber, Tom Hanks, Bill Pull...</td>
      <td>Sleepless in Seattle</td>
      <td>1993</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Tom Hanks, Nathan Lane, Meg Ryan]</td>
      <td>Joe Versus the Volcano</td>
      <td>1990</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Carrie Fisher, Billy Crystal, Bruno Kirby, Me...</td>
      <td>When Harry Met Sally</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Tom Hanks, Liv Tyler, Charlize Theron]</td>
      <td>That Thing You Do</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Brooke Langton, Keanu Reeves, Orlando Jones, ...</td>
      <td>The Replacements</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Robin Williams, Nathan Lane, Gene Hackman]</td>
      <td>The Birdcage</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Clint Eastwood, Gene Hackman, Richard Harris]</td>
      <td>Unforgiven</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Ice-T, Dina Meyer, Keanu Reeves, Takeshi Kitano]</td>
      <td>Johnny Mnemonic</td>
      <td>1995</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Sam Rockwell, Bonnie Hunt, Patricia Clarkson,...</td>
      <td>The Green Mile</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[John C. Reilly, Danny DeVito, J.T. Walsh, Jac...</td>
      <td>Hoffa</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Tom Hanks, Ed Harris, Gary Sinise, Kevin Baco...</td>
      <td>Apollo 13</td>
      <td>1995</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Helen Hunt, Bill Paxton, Philip Seymour Hoffm...</td>
      <td>Twister</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Helen Hunt, Tom Hanks]</td>
      <td>Cast Away</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Robin Williams, Oliver Platt]</td>
      <td>Bicentennial Man</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Tom Hanks, Madonna, Rosie O'Donnell, Geena Da...</td>
      <td>A League of Their Own</td>
      <td>1992</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 6.2: Modify the query to eliminate duplication.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 where m.released >= 1990 and m.released <= 2000
                 return m.released as Released, collect(m.title) as Movies, collect(p.name) as Actors 
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Movies</th>
      <th>Released</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>[The Matrix, The Matrix, The Matrix, The Matri...</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Al Pacino, Charlize Theron, Keanu Reeves, Hel...</td>
      <td>[The Devil's Advocate, The Devil's Advocate, T...</td>
      <td>1997</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[James Marshall, Kevin Pollak, J.T. Walsh, Aar...</td>
      <td>[A Few Good Men, A Few Good Men, A Few Good Me...</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>[Jerry Maguire, Jerry Maguire, Jerry Maguire, ...</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Robin Williams, Cuba Gooding Jr., Max von Syd...</td>
      <td>[What Dreams May Come, What Dreams May Come, W...</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Meg Ryan, Victor Garber, Tom Hanks, Bill Pull...</td>
      <td>[Sleepless in Seattle, Sleepless in Seattle, S...</td>
      <td>1993</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Tom Hanks, Nathan Lane, Meg Ryan]</td>
      <td>[Joe Versus the Volcano, Joe Versus the Volcan...</td>
      <td>1990</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Tom Hanks, Liv Tyler, Charlize Theron, Robin ...</td>
      <td>[That Thing You Do, That Thing You Do, That Th...</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Ice-T, Dina Meyer, Keanu Reeves, Takeshi Kita...</td>
      <td>[Johnny Mnemonic, Johnny Mnemonic, Johnny Mnem...</td>
      <td>1995</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 6.3: Modify the query to eliminate more duplication.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 where m.released >= 1990 and m.released <= 2000
                 return m.released as Released, collect(distinct m.title) as Movies, collect(distinct p.name) as Actors 
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Movies</th>
      <th>Released</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>[The Matrix, Snow Falling on Cedars, The Green...</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Al Pacino, Charlize Theron, Keanu Reeves, Hel...</td>
      <td>[The Devil's Advocate, As Good as It Gets]</td>
      <td>1997</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[James Marshall, Kevin Pollak, J.T. Walsh, Aar...</td>
      <td>[A Few Good Men, Unforgiven, Hoffa, A League o...</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>[Jerry Maguire, The Replacements, Cast Away]</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Robin Williams, Cuba Gooding Jr., Max von Syd...</td>
      <td>[What Dreams May Come, You've Got Mail, When H...</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Meg Ryan, Victor Garber, Tom Hanks, Bill Pull...</td>
      <td>[Sleepless in Seattle]</td>
      <td>1993</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Tom Hanks, Nathan Lane, Meg Ryan]</td>
      <td>[Joe Versus the Volcano]</td>
      <td>1990</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Tom Hanks, Liv Tyler, Charlize Theron, Robin ...</td>
      <td>[That Thing You Do, The Birdcage, Twister]</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Ice-T, Dina Meyer, Keanu Reeves, Takeshi Kita...</td>
      <td>[Johnny Mnemonic, Apollo 13]</td>
      <td>1995</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 6.4: Sort results returned.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 where m.released >= 1990 and m.released <= 2000
                 return m.released as Released, collect(distinct m.title) as Movies, collect(distinct p.name) as Actors 
                 order by m.released desc
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Movies</th>
      <th>Released</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>[Jerry Maguire, The Replacements, Cast Away]</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>[The Matrix, Snow Falling on Cedars, The Green...</td>
      <td>1999</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Robin Williams, Cuba Gooding Jr., Max von Syd...</td>
      <td>[What Dreams May Come, You've Got Mail, When H...</td>
      <td>1998</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Al Pacino, Charlize Theron, Keanu Reeves, Hel...</td>
      <td>[The Devil's Advocate, As Good as It Gets]</td>
      <td>1997</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Tom Hanks, Liv Tyler, Charlize Theron, Robin ...</td>
      <td>[That Thing You Do, The Birdcage, Twister]</td>
      <td>1996</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Ice-T, Dina Meyer, Keanu Reeves, Takeshi Kita...</td>
      <td>[Johnny Mnemonic, Apollo 13]</td>
      <td>1995</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Meg Ryan, Victor Garber, Tom Hanks, Bill Pull...</td>
      <td>[Sleepless in Seattle]</td>
      <td>1993</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[James Marshall, Kevin Pollak, J.T. Walsh, Aar...</td>
      <td>[A Few Good Men, Unforgiven, Hoffa, A League o...</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Tom Hanks, Nathan Lane, Meg Ryan]</td>
      <td>[Joe Versus the Volcano]</td>
      <td>1990</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 6.5: Retrieve the top 5 ratings and their associated movies.


```python
execute_query("""match (:Person)-[r:REVIEWED]->(m:Movie)
                 return m.title as Movie, r.rating as Rating
                 order by r.rating desc limit 5""")
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Replacements</td>
      <td>100</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Cloud Atlas</td>
      <td>95</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Jerry Maguire</td>
      <td>92</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Unforgiven</td>
      <td>85</td>
    </tr>
    <tr>
      <th>4</th>
      <td>The Da Vinci Code</td>
      <td>68</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 6.6: Retrieve all actors that have not appeared in more than 3 movies.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 with p.name as Actor, count(m.name) as numberMovies, collect(m.title) as Movies
                 where numberMovies <=3
                 return Actor, Movies
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Movies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Emil Eifrem</td>
      <td>[The Matrix]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Hugo Weaving</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Laurence Fishburne</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Carrie-Anne Moss</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Keanu Reeves</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Al Pacino</td>
      <td>[The Devil's Advocate]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Charlize Theron</td>
      <td>[The Devil's Advocate, That Thing You Do]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>James Marshall</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Kevin Pollak</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>J.T. Walsh</td>
      <td>[A Few Good Men, Hoffa]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Aaron Sorkin</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Cuba Gooding Jr.</td>
      <td>[A Few Good Men, Jerry Maguire, As Good as It ...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Christopher Guest</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Noah Wyle</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Kiefer Sutherland</td>
      <td>[A Few Good Men, Stand By Me]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Kevin Bacon</td>
      <td>[A Few Good Men, Frost/Nixon, Apollo 13]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Demi Moore</td>
      <td>[A Few Good Men]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Jack Nicholson</td>
      <td>[A Few Good Men, As Good as It Gets, Hoffa, On...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Tom Cruise</td>
      <td>[A Few Good Men, Top Gun, Jerry Maguire]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Val Kilmer</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Meg Ryan</td>
      <td>[Top Gun, You've Got Mail, Sleepless in Seattl...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Tom Skerritt</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Kelly McGillis</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Anthony Edwards</td>
      <td>[Top Gun]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Jerry O'Connell</td>
      <td>[Jerry Maguire, Stand By Me]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Bonnie Hunt</td>
      <td>[Jerry Maguire, The Green Mile]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Jay Mohr</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Jonathan Lipnicki</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Renee Zellweger</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Kelly Preston</td>
      <td>[Jerry Maguire]</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>72</th>
      <td>Paul Bettany</td>
      <td>[The Da Vinci Code]</td>
    </tr>
    <tr>
      <th>73</th>
      <td>John Hurt</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>74</th>
      <td>Stephen Rea</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>75</th>
      <td>Natalie Portman</td>
      <td>[V for Vendetta]</td>
    </tr>
    <tr>
      <th>76</th>
      <td>Ben Miles</td>
      <td>[V for Vendetta, Speed Racer, Ninja Assassin]</td>
    </tr>
    <tr>
      <th>77</th>
      <td>Emile Hirsch</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>78</th>
      <td>Rain</td>
      <td>[Speed Racer, Ninja Assassin]</td>
    </tr>
    <tr>
      <th>79</th>
      <td>Christina Ricci</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>80</th>
      <td>Susan Sarandon</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>81</th>
      <td>John Goodman</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Matthew Fox</td>
      <td>[Speed Racer]</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Naomie Harris</td>
      <td>[Ninja Assassin]</td>
    </tr>
    <tr>
      <th>84</th>
      <td>Sam Rockwell</td>
      <td>[The Green Mile, Frost/Nixon]</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Patricia Clarkson</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>86</th>
      <td>Michael Clarke Duncan</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>87</th>
      <td>David Morse</td>
      <td>[The Green Mile]</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Gary Sinise</td>
      <td>[The Green Mile, Apollo 13]</td>
    </tr>
    <tr>
      <th>89</th>
      <td>Michael Sheen</td>
      <td>[Frost/Nixon]</td>
    </tr>
    <tr>
      <th>90</th>
      <td>Frank Langella</td>
      <td>[Frost/Nixon]</td>
    </tr>
    <tr>
      <th>91</th>
      <td>Oliver Platt</td>
      <td>[Frost/Nixon, Bicentennial Man]</td>
    </tr>
    <tr>
      <th>92</th>
      <td>John C. Reilly</td>
      <td>[Hoffa]</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Danny DeVito</td>
      <td>[Hoffa, One Flew Over the Cuckoo's Nest]</td>
    </tr>
    <tr>
      <th>94</th>
      <td>Ed Harris</td>
      <td>[Apollo 13]</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Bill Paxton</td>
      <td>[Apollo 13, Twister, A League of Their Own]</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Philip Seymour Hoffman</td>
      <td>[Twister, Charlie Wilson's War]</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Diane Keaton</td>
      <td>[Something's Gotta Give]</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Julia Roberts</td>
      <td>[Charlie Wilson's War]</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Madonna</td>
      <td>[A League of Their Own]</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Geena Davis</td>
      <td>[A League of Their Own]</td>
    </tr>
    <tr>
      <th>101</th>
      <td>Lori Petty</td>
      <td>[A League of Their Own]</td>
    </tr>
  </tbody>
</table>
<p>102 rows × 2 columns</p>
</div>



## Exercício 7 – Working with cypher data

#### Exercício 7 – Working with cypher data

Write a Cypher query that retrieves all actors that acted in movies, and also retrieves the producers for those movies. During the query, collect the names of the actors and the names of the producers. Return the movie titles, along with the list of actors for each movie, and the list of producers for each movie making sure there is no duplication of data. Order the results returned based upon the size of the list of actors.


```python
execute_query("""match (a:Person)-[:ACTED_IN]->(m:Movie)<-[:PRODUCED]-(p:Person)
                 with m.title as Movies, collect(distinct a.name) as Actors, collect(distinct p.name) as Producers
                 return Movies, Actors, Producers
                 order by size(Actors) desc
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actors</th>
      <th>Movies</th>
      <th>Producers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Jerry O'Connell, Bonnie Hunt, Jay Mohr, Cuba ...</td>
      <td>Jerry Maguire</td>
      <td>[Cameron Crowe]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Emile Hirsch, Rain, Christina Ricci, Ben Mile...</td>
      <td>Speed Racer</td>
      <td>[Joel Silver]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Emil Eifrem, Hugo Weaving, Laurence Fishburne...</td>
      <td>The Matrix</td>
      <td>[Joel Silver]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[John Hurt, Stephen Rea, Natalie Portman, Hugo...</td>
      <td>V for Vendetta</td>
      <td>[Lana Wachowski, Lilly Wachowski, Joel Silver]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>The Matrix Reloaded</td>
      <td>[Joel Silver]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Hugo Weaving, Laurence Fishburne, Carrie-Anne...</td>
      <td>The Matrix Revolutions</td>
      <td>[Joel Silver]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Carrie Fisher, Billy Crystal, Bruno Kirby, Me...</td>
      <td>When Harry Met Sally</td>
      <td>[Nora Ephron, Rob Reiner]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Tom Hanks, Jim Broadbent, Halle Berry, Hugo W...</td>
      <td>Cloud Atlas</td>
      <td>[Stefan Arndt]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Rain, Ben Miles, Rick Yune, Naomie Harris]</td>
      <td>Ninja Assassin</td>
      <td>[Lana Wachowski, Joel Silver, Lilly Wachowski]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Keanu Reeves, Diane Keaton, Jack Nicholson]</td>
      <td>Something's Gotta Give</td>
      <td>[Nancy Meyers]</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 7.2: Collect a list

Write a Cypher query that retrieves all actors that acted in movies, and collects the list of movies for any actor that acted in more than five movies. Return the name of the actor and the list.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 with p.name as Actor, collect(m.title) as Movies
                 where size(Movies) > 5
                 return Actor, Movies
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Movies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Keanu Reeves</td>
      <td>[The Matrix, The Matrix Reloaded, The Matrix R...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Tom Hanks</td>
      <td>[You've Got Mail, Sleepless in Seattle, Joe Ve...</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 7.3: Unwind a list

Modify the query you just wrote so that before the query processing ends, you unwind the list of movies and then return the name of the actor and the title of the associated movie


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 with p.name as Actor, collect(m) as Movies
                 where size(Movies) > 5
                 with Actor, Movies unwind Movies as Movie
                 return Actor, Movie.title as Movie
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Actor</th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Keanu Reeves</td>
      <td>The Matrix</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Keanu Reeves</td>
      <td>The Matrix Reloaded</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Keanu Reeves</td>
      <td>The Matrix Revolutions</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Keanu Reeves</td>
      <td>The Devil's Advocate</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Keanu Reeves</td>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Keanu Reeves</td>
      <td>Johnny Mnemonic</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Keanu Reeves</td>
      <td>Something's Gotta Give</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Tom Hanks</td>
      <td>You've Got Mail</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Tom Hanks</td>
      <td>Sleepless in Seattle</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Tom Hanks</td>
      <td>Joe Versus the Volcano</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Tom Hanks</td>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Tom Hanks</td>
      <td>Cloud Atlas</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Tom Hanks</td>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Tom Hanks</td>
      <td>The Green Mile</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tom Hanks</td>
      <td>Apollo 13</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Tom Hanks</td>
      <td>Cast Away</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Tom Hanks</td>
      <td>Charlie Wilson's War</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Tom Hanks</td>
      <td>The Polar Express</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Tom Hanks</td>
      <td>A League of Their Own</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 7.4: Perform a calculation with the date type

Write a query that retrieves all movies that Tom Hanks acted in, returning the title of the movie, the year the movie was released, the number of years ago that the movie was released, and the age of Tom when the movie was released.


```python
execute_query("""match (p:Person)-[:ACTED_IN]->(m:Movie)
                 where p.name = 'Tom Hanks'
                 return m.title as Movie, 
                        m.released as Released, 
                        date().year - m.released as YearsAgoReleased, 
                        m.released - p.born as Age
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Movie</th>
      <th>Released</th>
      <th>YearsAgoReleased</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>39</td>
      <td>Apollo 13</td>
      <td>1995</td>
      <td>25</td>
    </tr>
    <tr>
      <th>1</th>
      <td>42</td>
      <td>You've Got Mail</td>
      <td>1998</td>
      <td>22</td>
    </tr>
    <tr>
      <th>2</th>
      <td>36</td>
      <td>A League of Their Own</td>
      <td>1992</td>
      <td>28</td>
    </tr>
    <tr>
      <th>3</th>
      <td>34</td>
      <td>Joe Versus the Volcano</td>
      <td>1990</td>
      <td>30</td>
    </tr>
    <tr>
      <th>4</th>
      <td>40</td>
      <td>That Thing You Do</td>
      <td>1996</td>
      <td>24</td>
    </tr>
    <tr>
      <th>5</th>
      <td>50</td>
      <td>The Da Vinci Code</td>
      <td>2006</td>
      <td>14</td>
    </tr>
    <tr>
      <th>6</th>
      <td>56</td>
      <td>Cloud Atlas</td>
      <td>2012</td>
      <td>8</td>
    </tr>
    <tr>
      <th>7</th>
      <td>44</td>
      <td>Cast Away</td>
      <td>2000</td>
      <td>20</td>
    </tr>
    <tr>
      <th>8</th>
      <td>43</td>
      <td>The Green Mile</td>
      <td>1999</td>
      <td>21</td>
    </tr>
    <tr>
      <th>9</th>
      <td>37</td>
      <td>Sleepless in Seattle</td>
      <td>1993</td>
      <td>27</td>
    </tr>
    <tr>
      <th>10</th>
      <td>48</td>
      <td>The Polar Express</td>
      <td>2004</td>
      <td>16</td>
    </tr>
    <tr>
      <th>11</th>
      <td>51</td>
      <td>Charlie Wilson's War</td>
      <td>2007</td>
      <td>13</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 8 – Creating nodes

#### Exercise 8.1: Create a Movie node

Create a Movie node for the movie with the title, Forrest Gump.


```python
execute_query("""create (m:Movie {title: 'Forrest Gump'})
                 return m
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'title': 'Forrest Gump'}</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.2: Retrieve the newly-created node.


```python
execute_query("""match (m:Movie {title: 'Forrest Gump'})
                 return m.title as Movie
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.3: Create a Person node.

Create a Person node for the person with the name, Robin Wright.


```python
execute_query("""create (p:Person {name: 'Robin Wright'})
                 return p
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'name': 'Robin Wright'}</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.4: Retrieve the newly-created node.


```python
execute_query("""match (p:Person {name: 'Robin Wright'})
                 return p.name as Person
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Person</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Robin Wright</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.5: Add a label to a node

Add the label OlderMovie to any Movie node that was released before 2010.


```python
execute_query("""match (m:Movie)
                 where m.released < 2010
                 set m:olderMovie
                 return labels(m)
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>labels(m)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>30</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>31</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>32</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>33</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>34</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>35</th>
      <td>[Movie, olderMovie]</td>
    </tr>
    <tr>
      <th>36</th>
      <td>[Movie, olderMovie]</td>
    </tr>
  </tbody>
</table>
</div>



### Exercise 8.6: Retrieve the node using the new label.


```python
execute_query("""match (m:Movie)
                 where m:olderMovie
                 return m.title, m.released, m.olderMovie
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.olderMovie</th>
      <th>m.released</th>
      <th>m.title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>None</td>
      <td>1999</td>
      <td>The Matrix</td>
    </tr>
    <tr>
      <th>1</th>
      <td>None</td>
      <td>2003</td>
      <td>The Matrix Reloaded</td>
    </tr>
    <tr>
      <th>2</th>
      <td>None</td>
      <td>2003</td>
      <td>The Matrix Revolutions</td>
    </tr>
    <tr>
      <th>3</th>
      <td>None</td>
      <td>1997</td>
      <td>The Devil's Advocate</td>
    </tr>
    <tr>
      <th>4</th>
      <td>None</td>
      <td>1992</td>
      <td>A Few Good Men</td>
    </tr>
    <tr>
      <th>5</th>
      <td>None</td>
      <td>1986</td>
      <td>Top Gun</td>
    </tr>
    <tr>
      <th>6</th>
      <td>None</td>
      <td>2000</td>
      <td>Jerry Maguire</td>
    </tr>
    <tr>
      <th>7</th>
      <td>None</td>
      <td>1986</td>
      <td>Stand By Me</td>
    </tr>
    <tr>
      <th>8</th>
      <td>None</td>
      <td>1997</td>
      <td>As Good as It Gets</td>
    </tr>
    <tr>
      <th>9</th>
      <td>None</td>
      <td>1998</td>
      <td>What Dreams May Come</td>
    </tr>
    <tr>
      <th>10</th>
      <td>None</td>
      <td>1999</td>
      <td>Snow Falling on Cedars</td>
    </tr>
    <tr>
      <th>11</th>
      <td>None</td>
      <td>1998</td>
      <td>You've Got Mail</td>
    </tr>
    <tr>
      <th>12</th>
      <td>None</td>
      <td>1993</td>
      <td>Sleepless in Seattle</td>
    </tr>
    <tr>
      <th>13</th>
      <td>None</td>
      <td>1990</td>
      <td>Joe Versus the Volcano</td>
    </tr>
    <tr>
      <th>14</th>
      <td>None</td>
      <td>1998</td>
      <td>When Harry Met Sally</td>
    </tr>
    <tr>
      <th>15</th>
      <td>None</td>
      <td>1996</td>
      <td>That Thing You Do</td>
    </tr>
    <tr>
      <th>16</th>
      <td>None</td>
      <td>2000</td>
      <td>The Replacements</td>
    </tr>
    <tr>
      <th>17</th>
      <td>None</td>
      <td>2006</td>
      <td>RescueDawn</td>
    </tr>
    <tr>
      <th>18</th>
      <td>None</td>
      <td>1996</td>
      <td>The Birdcage</td>
    </tr>
    <tr>
      <th>19</th>
      <td>None</td>
      <td>1992</td>
      <td>Unforgiven</td>
    </tr>
    <tr>
      <th>20</th>
      <td>None</td>
      <td>1995</td>
      <td>Johnny Mnemonic</td>
    </tr>
    <tr>
      <th>21</th>
      <td>None</td>
      <td>2006</td>
      <td>The Da Vinci Code</td>
    </tr>
    <tr>
      <th>22</th>
      <td>None</td>
      <td>2006</td>
      <td>V for Vendetta</td>
    </tr>
    <tr>
      <th>23</th>
      <td>None</td>
      <td>2008</td>
      <td>Speed Racer</td>
    </tr>
    <tr>
      <th>24</th>
      <td>None</td>
      <td>2009</td>
      <td>Ninja Assassin</td>
    </tr>
    <tr>
      <th>25</th>
      <td>None</td>
      <td>1999</td>
      <td>The Green Mile</td>
    </tr>
    <tr>
      <th>26</th>
      <td>None</td>
      <td>2008</td>
      <td>Frost/Nixon</td>
    </tr>
    <tr>
      <th>27</th>
      <td>None</td>
      <td>1992</td>
      <td>Hoffa</td>
    </tr>
    <tr>
      <th>28</th>
      <td>None</td>
      <td>1995</td>
      <td>Apollo 13</td>
    </tr>
    <tr>
      <th>29</th>
      <td>None</td>
      <td>1996</td>
      <td>Twister</td>
    </tr>
    <tr>
      <th>30</th>
      <td>None</td>
      <td>2000</td>
      <td>Cast Away</td>
    </tr>
    <tr>
      <th>31</th>
      <td>None</td>
      <td>1975</td>
      <td>One Flew Over the Cuckoo's Nest</td>
    </tr>
    <tr>
      <th>32</th>
      <td>None</td>
      <td>2003</td>
      <td>Something's Gotta Give</td>
    </tr>
    <tr>
      <th>33</th>
      <td>None</td>
      <td>1999</td>
      <td>Bicentennial Man</td>
    </tr>
    <tr>
      <th>34</th>
      <td>None</td>
      <td>2007</td>
      <td>Charlie Wilson's War</td>
    </tr>
    <tr>
      <th>35</th>
      <td>None</td>
      <td>2004</td>
      <td>The Polar Express</td>
    </tr>
    <tr>
      <th>36</th>
      <td>None</td>
      <td>1992</td>
      <td>A League of Their Own</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.7: Add the Female label to selected nodes.

Add the label Female to all Person nodes that has a person whose name starts with Robin.


```python
execute_query("""match (p:Person)
                 where p.name starts with 'Robin'
                 set p:Female
                 return p.name
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Robin Williams</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Robin Wright</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.8: Retrieve all Female nodes


```python
execute_query("""match (p:Person)
                 where p:Female
                 return p.name
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Robin Williams</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Robin Wright</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.9: Remove the Female label from the nodes that have this label


```python
execute_query("""match (p:Person)
                 where p:Female
                 remove p:Female
                 return p.name
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Robin Williams</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Robin Wright</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.10: View the current schema of the graph


```python
execute_query("call db.schema").values
```




    array([[list([(_-10:Movie {constraints: [], indexes: [], name: 'Movie'}), (_-12:olderMovie {constraints: [], indexes: [], name: 'olderMovie'}), (_-11:Person {constraints: [], indexes: [], name: 'Person'})]),
            list([(Person)-[:ACTED_IN {}]->(olderMovie), (Person)-[:ACTED_IN {}]->(Movie), (Person)-[:REVIEWED {}]->(Movie), (Person)-[:REVIEWED {}]->(olderMovie), (Person)-[:PRODUCED {}]->(Movie), (Person)-[:PRODUCED {}]->(olderMovie), (Person)-[:WROTE {}]->(Movie), (Person)-[:WROTE {}]->(olderMovie), (Person)-[:FOLLOWS {}]->(Person), (Person)-[:DIRECTED {}]->(olderMovie), (Person)-[:DIRECTED {}]->(Movie)])]],
          dtype=object)



#### Exercise 8.11: Add properties to a movie.

Add the following properties to the movie, Forrest Gump:

released: 1994

tagline: Life is like a box of chocolates…​you never know what you’re gonna get.

lengthInMinutes: 142


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 set m:olderMovie,
                     m.released = 1994, 
                     m.tagline = 'Life is like a box of chocolates…​you never know what you’re gonna get.',
                     m.lengthInMinutes = 142
                 return m
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'lengthInMinutes': 142, 'tagline': 'Life is l...</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.12: Retrieve an OlderMovie node to confirm the label and properties.


```python
execute_query("""match (m:olderMovie)
                 where m.title = 'Forrest Gump'
                 return m
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'lengthInMinutes': 142, 'tagline': 'Life is l...</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 8.13: Add properties to the person, Robin Wright

dd the following properties to the person, Robin Wright:

born: 1966

birthPlace: Dallas


```python
execute_query("""match (p:Person)
                 where p.name = 'Robin Wright'
                 set p.born = 1966, 
                     p.birthPlace = 'Dallas'
                 return p
              """).values
```




    array([[(_172:Person {birthPlace: 'Dallas', born: 1966, name: 'Robin Wright'})]],
          dtype=object)



#### Exercise 8.14: Retrieve an updated Person node.


```python
execute_query("""match (p:Person)
                 where p.name = 'Robin Wright'
                 return p
              """).values
```




    array([[(_172:Person {birthPlace: 'Dallas', born: 1966, name: 'Robin Wright'})]],
          dtype=object)



#### Exercise 8.15: Remove a property from a Movie node

Remove the lengthInMinutes property from the movie, Forrest Gump.


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 set m.lengthInMinutes = null
                 return m
              """).values
```




    array([[(_171:Movie:olderMovie {released: 1994, tagline: 'Life is like a box of chocolates\u2026\u200byou never know what you\u2019re gonna get.', title: 'Forrest Gump'})]],
          dtype=object)



#### Exercise 8.16: Retrieve the node to confirm that the property has been removed.


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 return m
              """).values
```




    array([[(_171:Movie:olderMovie {released: 1994, tagline: 'Life is like a box of chocolates\u2026\u200byou never know what you\u2019re gonna get.', title: 'Forrest Gump'})]],
          dtype=object)



#### Exercise 8.17: Remove a property from a Person node.

Remove the birthPlace property from the person, Robin Wright.


```python
execute_query("""match (p:Person)
                 where p.name = 'Robin Wright'
                 set p.birthPlace = null
                 return p
              """).values
```




    array([[(_172:Person {born: 1966, name: 'Robin Wright'})]], dtype=object)



#### Exercise 8.18: Retrieve the node to confirm that the property has been removed.


```python
execute_query("""match (p:Person)
                 where p.name = 'Robin Wright'
                 return p
              """).values
```




    array([[(_172:Person {born: 1966, name: 'Robin Wright'})]], dtype=object)



## Exercício 9 – Creating relationships

#### Exercise 9.1: Create ACTED_IN relationships

Create the ACTED_IN relationship between the actors, Robin Wright, Tom Hanks, and Gary Sinise and the movie, Forrest Gump.


```python
execute_query("""match (p:Person), (m:Movie)
                 where p.name in ['Robin Wright', 'Tom Hanks', 'Gary Sinise']
                       and m.title = 'Forrest Gump'
                CREATE (p)-[:ACTED_IN]->(m)
                return p.name, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Tom Hanks</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Forrest Gump</td>
      <td>Gary Sinise</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Forrest Gump</td>
      <td>Robin Wright</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.2: Create DIRECTED relationships.

Create the DIRECTED relationship between Robert Zemeckis and the movie, Forrest Gump.


```python
execute_query("""match (p:Person), (m:Movie)
                 where p.name = 'Robert Zemeckis'
                       and m.title = 'Forrest Gump'
                CREATE (p)-[:DIRECTED]->(m)
                return p.name, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Robert Zemeckis</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.3: Create a HELPED relationship

Create a new relationship, HELPED from Tom Hanks to Gary Sinise.


```python
execute_query("""match (p1:Person), (p2:Person)
                 where p1.name = 'Tom Hanks'
                       and p2.name = 'Gary Sinise'
                CREATE (p1)-[:HELPED]->(p2)
                return p1.name, p2.name
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Tom Hanks</td>
      <td>Gary Sinise</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.4: Query nodes and new relationships.

Write a Cypher query to return all nodes connected to the movie, Forrest Gump, along with their relationships.


```python
execute_query("""match (p:Person)-[rel]->(m:Movie)
                 where m.title = 'Forrest Gump'
                 return p.name, rel, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
      <th>rel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Robert Zemeckis</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Forrest Gump</td>
      <td>Robin Wright</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Forrest Gump</td>
      <td>Gary Sinise</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Forrest Gump</td>
      <td>Tom Hanks</td>
      <td>{}</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.5: Add properties to relationships.

Add the roles property to the three ACTED_IN relationships that you just created to the movie, Forrest Gump using this information: Tom Hanks played the role, Forrest Gump. Robin Wright played the role, Jenny Curran. Gary Sinise played the role, Lieutenant Dan Taylor.


```python
execute_query("""match (p:Person)-[rel:ACTED_IN]->(m:Movie)
                 where m.title = 'Forrest Gump'
                 set rel.roles =
                 case p.name
                   when 'Tom Hanks' then ['Forrest Gump']
                   when 'Robin Wright' then ['Jenny Curran']
                   when 'Gary Sinise' then ['Lieutenant Dan Taylor']
                 end
                 return p.name, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Robin Wright</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Forrest Gump</td>
      <td>Gary Sinise</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Forrest Gump</td>
      <td>Tom Hanks</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.6: Add a property to the HELPED relationship.

Add a new property, research to the HELPED relationship between Tom Hanks and Gary Sinise and set this property’s value to war history.


```python
execute_query("""match (p1:Person)-[rel:HELPED]->(p2:Person)
                 where p1.name = 'Tom Hanks' and p2.name = 'Gary Sinise'
                 set rel.research = 'war history'
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



#### Exercise 9.7: View the current list of property keys in the graph


```python
execute_query("""call db.propertyKeys
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>propertyKey</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tagline</td>
    </tr>
    <tr>
      <th>1</th>
      <td>title</td>
    </tr>
    <tr>
      <th>2</th>
      <td>released</td>
    </tr>
    <tr>
      <th>3</th>
      <td>born</td>
    </tr>
    <tr>
      <th>4</th>
      <td>name</td>
    </tr>
    <tr>
      <th>5</th>
      <td>roles</td>
    </tr>
    <tr>
      <th>6</th>
      <td>summary</td>
    </tr>
    <tr>
      <th>7</th>
      <td>rating</td>
    </tr>
    <tr>
      <th>8</th>
      <td>lengthInMinutes</td>
    </tr>
    <tr>
      <th>9</th>
      <td>birthPlace</td>
    </tr>
    <tr>
      <th>10</th>
      <td>research</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.8: View the current schema of the graph.


```python
execute_query("""call db.schema
              """).values
```




    array([[list([(_-19:Movie {constraints: [], indexes: [], name: 'Movie'}), (_-21:olderMovie {constraints: [], indexes: [], name: 'olderMovie'}), (_-20:Person {constraints: [], indexes: [], name: 'Person'})]),
            list([(Person)-[:ACTED_IN {}]->(Movie), (Person)-[:ACTED_IN {}]->(olderMovie), (Person)-[:REVIEWED {}]->(olderMovie), (Person)-[:REVIEWED {}]->(Movie), (Person)-[:PRODUCED {}]->(Movie), (Person)-[:PRODUCED {}]->(olderMovie), (Person)-[:WROTE {}]->(Movie), (Person)-[:WROTE {}]->(olderMovie), (Person)-[:FOLLOWS {}]->(Person), (Person)-[:DIRECTED {}]->(Movie), (Person)-[:DIRECTED {}]->(olderMovie), (Person)-[:HELPED {}]->(Person)])]],
          dtype=object)



#### Exercise 9.9: Retrieve the names and roles for actors.

Query the graph to return the names and roles of actors in the movie, Forrest Gump.


```python
execute_query("""match (p:Person)-[rel:ACTED_IN]->(m:Movie)
                 where m.title = 'Forrest Gump'
                 return p.name, rel.roles
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p.name</th>
      <th>rel.roles</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Robin Wright</td>
      <td>[Jenny Curran]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Gary Sinise</td>
      <td>[Lieutenant Dan Taylor]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Tom Hanks</td>
      <td>[Forrest Gump]</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.10: Retrieve information about any specific relationships

Query the graph to retrieve information about any HELPED relationships.


```python
execute_query("""match (p1:Person)-[rel:HELPED]->(p2:Person)
                 return p1.name, rel.roles, p2.name
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>p1.name</th>
      <th>p2.name</th>
      <th>rel.roles</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Tom Hanks</td>
      <td>Gary Sinise</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 9.11: Modify a property of a relationship.

Modify the role that Gary Sinise played in the movie, Forrest Gump from Lieutenant Dan Taylor to Lt. Dan Taylor.


```python
execute_query("""match (p:Person)-[rel:ACTED_IN]->(m:Movie)
                 where m.title = 'Forrest Gump' and p.name = 'Lieutenant Dan Taylor'
                 set rel.roles = ['Lt. Dan Taylor']
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



#### Exercise 9.12: Remove a property from a relationship

Remove the research property from the HELPED relationship from Tom Hanks to Gary Sinise.


```python
execute_query("""match (p1:Person)-[rel:HELPED]->(p2:Person)
                 where p1.name = 'Tom Hanks' and p2.name = 'Gary Sinise' 
                 remove rel.research
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



#### Exercise 9.13: Confirm that your modifications were made to the graph


```python
execute_query("""match (p:Person)-[rel:ACTED_IN]->(m:Movie)
                 where m.title = 'Forrest Gump'
                 return p.name, rel, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
      <th>rel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Robin Wright</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Forrest Gump</td>
      <td>Gary Sinise</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Forrest Gump</td>
      <td>Tom Hanks</td>
      <td>{}</td>
    </tr>
  </tbody>
</table>
</div>



## Exercício 10 – Deleting nodes and relationships

#### Exercise 10.1: Delete a relationship.

Delete the HELPED relationship from the graph.


```python
execute_query("""match (:Person)-[rel:HELPED]->(:Person)
                 delete rel
              """)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



#### Exercise 10.2: Confirm that the relationship has been deleted


```python
execute_query("""match (:Person)-[rel:HELPED]->(:Person)
                 return rel
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



### Exercise 10.3: Retrieve a movie and all of its relationships

Query the graph to display Forrest Gump and all of its relationships.


```python
execute_query("""match (p:Person)-[rel]->(m:Movie)
                 where m.title = 'Forrest Gump'
                 return p.name, rel, m.title
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>m.title</th>
      <th>p.name</th>
      <th>rel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Forrest Gump</td>
      <td>Robert Zemeckis</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Forrest Gump</td>
      <td>Robin Wright</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Forrest Gump</td>
      <td>Gary Sinise</td>
      <td>{}</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Forrest Gump</td>
      <td>Tom Hanks</td>
      <td>{}</td>
    </tr>
  </tbody>
</table>
</div>



#### Exercise 10.4: Try deleting a node without detaching its relationships.

Try deleting the Forrest Gump node without detaching its relationships.


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 delete m
              """)
```


    ---------------------------------------------------------------------------

    ClientError                               Traceback (most recent call last)

    <ipython-input-289-fce138580520> in <module>
          2                  where m.title = 'Forrest Gump'
          3                  delete m
    ----> 4               """)
    

    <ipython-input-6-7e3fe836d1a6> in execute_query(query)
          1 def execute_query(query):
          2 
    ----> 3     df = graph.run(query).to_data_frame()
          4 
          5     return df
    

    ~\Anaconda3\lib\site-packages\py2neo\database.py in run(self, cypher, parameters, **kwparameters)
        531         :return:
        532         """
    --> 533         return self.begin(autocommit=True).run(cypher, parameters, **kwparameters)
        534 
        535     def separate(self, subgraph):
    

    ~\Anaconda3\lib\site-packages\py2neo\database.py in run(self, cypher, parameters, **kwparameters)
        826                                              graph=self.graph,
        827                                              keys=[],
    --> 828                                              entities=entities))
        829         except CypherError as error:
        830             raise GraphError.hydrate({"code": error.code, "message": error.message})
    

    ~\Anaconda3\lib\site-packages\py2neo\internal\connectors.py in run(self, statement, parameters, tx, graph, keys, entities)
        290     def run(self, statement, parameters=None, tx=None, graph=None, keys=None, entities=None):
        291         if tx is None:
    --> 292             return self._run_1(statement, parameters, graph, keys, entities)
        293         else:
        294             return self._run_in_tx(statement, parameters, tx, graph, keys, entities)
    

    ~\Anaconda3\lib\site-packages\py2neo\internal\connectors.py in _run_1(self, statement, parameters, graph, keys, entities)
        253                     on_success=result.update_metadata, on_failure=self._fail, on_summary=result.done)
        254         cx.send()
    --> 255         cx.fetch()
        256         return result
        257 
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in fetch(self)
        417     def fetch(self):
        418         try:
    --> 419             return self._fetch()
        420         except self.error_handler.known_errors as error:
        421             self.error_handler.handle(error, self.unresolved_address)
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in _fetch(self)
        453         if summary_signature == b"\x70":
        454             log_debug("[#%04X]  S: SUCCESS %r", self.local_port, summary_metadata)
    --> 455             response.on_success(summary_metadata or {})
        456         elif summary_signature == b"\x7E":
        457             log_debug("[#%04X]  S: IGNORED", self.local_port)
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in on_success(self, metadata)
        738         handler = self.handlers.get("on_success")
        739         if callable(handler):
    --> 740             handler(metadata)
        741         handler = self.handlers.get("on_summary")
        742         if callable(handler):
    

    ~\Anaconda3\lib\site-packages\py2neo\internal\connectors.py in update_metadata_with_keys(metadata)
        247         def update_metadata_with_keys(metadata):
        248             result.update_metadata(metadata)
    --> 249             hydrator.keys = result.keys()
        250 
        251         cx.run(statement, dehydrated_parameters or {}, on_success=update_metadata_with_keys, on_failure=self._fail)
    

    ~\Anaconda3\lib\site-packages\py2neo\internal\hydration\__init__.py in keys(self)
         75     def keys(self):
         76         while not self._keys and not self._done and callable(self._on_more):
    ---> 77             self._on_more()
         78         return self._keys
         79 
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in fetch(self)
        417     def fetch(self):
        418         try:
    --> 419             return self._fetch()
        420         except self.error_handler.known_errors as error:
        421             self.error_handler.handle(error, self.unresolved_address)
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in _fetch(self)
        459         elif summary_signature == b"\x7F":
        460             log_debug("[#%04X]  S: FAILURE %r", self.local_port, summary_metadata)
    --> 461             response.on_failure(summary_metadata or {})
        462         else:
        463             raise ProtocolError("Unexpected response message with signature %02X" % summary_signature)
    

    ~\Anaconda3\lib\site-packages\neobolt\direct.py in on_failure(self, metadata)
        749         handler = self.handlers.get("on_failure")
        750         if callable(handler):
    --> 751             handler(metadata)
        752         handler = self.handlers.get("on_summary")
        753         if callable(handler):
    

    ~\Anaconda3\lib\site-packages\py2neo\internal\connectors.py in _fail(cls, metadata)
        286     def _fail(cls, metadata):
        287         from py2neo.database import GraphError
    --> 288         raise GraphError.hydrate(metadata)
        289 
        290     def run(self, statement, parameters=None, tx=None, graph=None, keys=None, entities=None):
    

    ClientError: ConstraintValidationFailed: Cannot delete node<171>, because it still has relationships. To delete this node, you must first delete its relationships.


#### Exercise 10.5: Delete a Movie node, along with its relationships

Delete Forrest Gump, along with its relationships in the graph.


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 detach delete m
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



#### Exercise 10.6: Confirm that the Movie node has been deleted.


```python
execute_query("""match (m:Movie)
                 where m.title = 'Forrest Gump'
                 return m
              """)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>


