<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.2.253">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>promo_testing_linear_regression</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1.6em;
  vertical-align: middle;
}
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { display: inline-block; line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
    color: #aaaaaa;
  }
pre.numberSource { margin-left: 3em; border-left: 1px solid #aaaaaa;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
code span.al { color: #ff0000; font-weight: bold; } /* Alert */
code span.an { color: #60a0b0; font-weight: bold; font-style: italic; } /* Annotation */
code span.at { color: #7d9029; } /* Attribute */
code span.bn { color: #40a070; } /* BaseN */
code span.bu { color: #008000; } /* BuiltIn */
code span.cf { color: #007020; font-weight: bold; } /* ControlFlow */
code span.ch { color: #4070a0; } /* Char */
code span.cn { color: #880000; } /* Constant */
code span.co { color: #60a0b0; font-style: italic; } /* Comment */
code span.cv { color: #60a0b0; font-weight: bold; font-style: italic; } /* CommentVar */
code span.do { color: #ba2121; font-style: italic; } /* Documentation */
code span.dt { color: #902000; } /* DataType */
code span.dv { color: #40a070; } /* DecVal */
code span.er { color: #ff0000; font-weight: bold; } /* Error */
code span.ex { } /* Extension */
code span.fl { color: #40a070; } /* Float */
code span.fu { color: #06287e; } /* Function */
code span.im { color: #008000; font-weight: bold; } /* Import */
code span.in { color: #60a0b0; font-weight: bold; font-style: italic; } /* Information */
code span.kw { color: #007020; font-weight: bold; } /* Keyword */
code span.op { color: #666666; } /* Operator */
code span.ot { color: #007020; } /* Other */
code span.pp { color: #bc7a00; } /* Preprocessor */
code span.sc { color: #4070a0; } /* SpecialChar */
code span.ss { color: #bb6688; } /* SpecialString */
code span.st { color: #4070a0; } /* String */
code span.va { color: #19177c; } /* Variable */
code span.vs { color: #4070a0; } /* VerbatimString */
code span.wa { color: #60a0b0; font-weight: bold; font-style: italic; } /* Warning */
</style>


<script src="Promo_testing_linear_regression_files/libs/clipboard/clipboard.min.js"></script>
<script src="Promo_testing_linear_regression_files/libs/quarto-html/quarto.js"></script>
<script src="Promo_testing_linear_regression_files/libs/quarto-html/popper.min.js"></script>
<script src="Promo_testing_linear_regression_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="Promo_testing_linear_regression_files/libs/quarto-html/anchor.min.js"></script>
<link href="Promo_testing_linear_regression_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="Promo_testing_linear_regression_files/libs/quarto-html/quarto-syntax-highlighting.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="Promo_testing_linear_regression_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="Promo_testing_linear_regression_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="Promo_testing_linear_regression_files/libs/bootstrap/bootstrap.min.css" rel="stylesheet" id="quarto-bootstrap" data-mode="light">
<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.3.6/require.min.js" integrity="sha512-c3Nl8+7g4LMSTdrm621y7kf9v3SDPnhxLNhcjFJbKECVnmZHTdo+IRO05sNLTH/D3vA6u1X32ehoLC7WFVdheg==" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js" integrity="sha512-bLT0Qm9VnAYZDflyKcBaQ2gg0hSYNQrJ8RilYldYQ1FxQYoCLtUjuuRuZo+fjqhx/qtq/1itJ0C2ejDxltZVFg==" crossorigin="anonymous"></script>
<script type="application/javascript">define('jquery', [],function() {return window.jQuery;})</script>

  <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml-full.js" type="text/javascript"></script>

</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">



<div class="cell" data-execution_count="2">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> numpy <span class="im">as</span> np</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> pandas <span class="im">as</span> pd</span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> seaborn <span class="im">as</span> sns</span>
<span id="cb1-4"><a href="#cb1-4" aria-hidden="true" tabindex="-1"></a><span class="im">from</span> sklearn.preprocessing <span class="im">import</span> OneHotEncoder <span class="im">as</span> SklearnOneHotEncoder</span>
<span id="cb1-5"><a href="#cb1-5" aria-hidden="true" tabindex="-1"></a><span class="im">from</span> statsmodels.regression.linear_model <span class="im">import</span> OLS</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<section id="using-linear-regression-with-dummy-variables-for-promo-testing" class="level3">
<h3 class="anchored" data-anchor-id="using-linear-regression-with-dummy-variables-for-promo-testing">Using linear regression with dummy variables for promo testing</h3>
<p>Dependent variable - <span class="math inline">\(Y\)</span> - our target for prediction - final check value</p>
<p>Independet Variable - <span class="math inline">\(X\)</span> - the feature - (our promo)</p>
<p>Promo is a categorical variable which we will transform into a dummy variable.</p>
<p><span class="math inline">\({\alpha}\)</span> will represent a change (delta) in the average check.</p>
<p><span class="math inline">\({\beta}\)</span> is just the average bill for all orders without promo.</p>
<p>The main formula for linear regrission will be: <span class="math display">\[
Y = {\alpha} * X + {\beta}
\]</span></p>
<p>With dummy variable we need to re-write linear regression, because we want it to represent the expected value of Y at some value of X.</p>
<p><span class="math display">\[
E[Y | X] = {\alpha} * X + {\beta}
\]</span></p>
<p>Also when using dummay variable for the promo, a purchase with a promo will be binary (with promo = 1, and without = 0).</p>
<p>So when we bought something with a promo, X=1, and we multiply 1 by the check value. When X=0, our increase in check value <span class="math inline">\({\alpha}\)</span> is multiplied by 0, and at the end we have only <span class="math inline">\({\beta}\)</span>.</p>
<p>So in these cases the forimula from above will look like this:</p>
<p><span class="math display">\[
E[Y | X=1] = {\alpha} + {\beta}
\]</span></p>
<p><span class="math display">\[
E[Y | X=0] = {\beta}
\]</span></p>
<p><span class="math inline">\({\beta}\)</span> will essentially be the average of all checks without a promo.</p>
<div class="cell" data-pycharm="{&quot;name&quot;:&quot;#%%\n&quot;}" data-execution_count="56">
<div class="sourceCode cell-code" id="cb2"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="co">#Entire class to transform categorical feature into a dummy (binary) variable. </span></span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a><span class="co">#There is a standard OneHotEncoder in the sklearn.preprocessing but it will leave new columns without names,</span></span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a><span class="co">#so we have to make a new one </span></span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a><span class="kw">class</span> OneHotEncoder(SklearnOneHotEncoder):</span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a>    <span class="kw">def</span> <span class="fu">__init__</span>(<span class="va">self</span>, <span class="op">**</span>kwargs):</span>
<span id="cb2-6"><a href="#cb2-6" aria-hidden="true" tabindex="-1"></a>        <span class="bu">super</span>(OneHotEncoder, <span class="va">self</span>).<span class="fu">__init__</span>(<span class="op">**</span>kwargs)</span>
<span id="cb2-7"><a href="#cb2-7" aria-hidden="true" tabindex="-1"></a>        <span class="va">self</span>.fit_flag <span class="op">=</span> <span class="va">False</span></span>
<span id="cb2-8"><a href="#cb2-8" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-9"><a href="#cb2-9" aria-hidden="true" tabindex="-1"></a>    <span class="kw">def</span> fit(<span class="va">self</span>, X, <span class="op">**</span>kwargs):</span>
<span id="cb2-10"><a href="#cb2-10" aria-hidden="true" tabindex="-1"></a>        out <span class="op">=</span> <span class="bu">super</span>().fit(X)</span>
<span id="cb2-11"><a href="#cb2-11" aria-hidden="true" tabindex="-1"></a>        <span class="va">self</span>.fit_flag <span class="op">=</span> <span class="va">True</span></span>
<span id="cb2-12"><a href="#cb2-12" aria-hidden="true" tabindex="-1"></a>        <span class="cf">return</span> out</span>
<span id="cb2-13"><a href="#cb2-13" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-14"><a href="#cb2-14" aria-hidden="true" tabindex="-1"></a>    <span class="kw">def</span> transform(<span class="va">self</span>, X, <span class="op">**</span>kwargs):</span>
<span id="cb2-15"><a href="#cb2-15" aria-hidden="true" tabindex="-1"></a>        sparse_matrix <span class="op">=</span> <span class="bu">super</span>(OneHotEncoder, <span class="va">self</span>).transform(X)</span>
<span id="cb2-16"><a href="#cb2-16" aria-hidden="true" tabindex="-1"></a>        new_columns <span class="op">=</span> <span class="va">self</span>.get_new_columns(X<span class="op">=</span>X)</span>
<span id="cb2-17"><a href="#cb2-17" aria-hidden="true" tabindex="-1"></a>        d_out <span class="op">=</span> pd.DataFrame(sparse_matrix.toarray(), columns<span class="op">=</span>new_columns, index<span class="op">=</span>X.index)</span>
<span id="cb2-18"><a href="#cb2-18" aria-hidden="true" tabindex="-1"></a>        <span class="cf">return</span> d_out</span>
<span id="cb2-19"><a href="#cb2-19" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-20"><a href="#cb2-20" aria-hidden="true" tabindex="-1"></a>    <span class="kw">def</span> fit_transform(<span class="va">self</span>, X, <span class="op">**</span>kwargs):</span>
<span id="cb2-21"><a href="#cb2-21" aria-hidden="true" tabindex="-1"></a>        <span class="va">self</span>.fit(X)</span>
<span id="cb2-22"><a href="#cb2-22" aria-hidden="true" tabindex="-1"></a>        <span class="cf">return</span> <span class="va">self</span>.transform(X)</span>
<span id="cb2-23"><a href="#cb2-23" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb2-24"><a href="#cb2-24" aria-hidden="true" tabindex="-1"></a>    <span class="kw">def</span> get_new_columns(<span class="va">self</span>, X):</span>
<span id="cb2-25"><a href="#cb2-25" aria-hidden="true" tabindex="-1"></a>        new_columns <span class="op">=</span> []</span>
<span id="cb2-26"><a href="#cb2-26" aria-hidden="true" tabindex="-1"></a>        <span class="cf">for</span> i, column <span class="kw">in</span> <span class="bu">enumerate</span>(X.columns):</span>
<span id="cb2-27"><a href="#cb2-27" aria-hidden="true" tabindex="-1"></a>            j <span class="op">=</span> <span class="dv">0</span></span>
<span id="cb2-28"><a href="#cb2-28" aria-hidden="true" tabindex="-1"></a>            <span class="cf">while</span> j <span class="op">&lt;</span> <span class="bu">len</span>(<span class="va">self</span>.categories_[i]):</span>
<span id="cb2-29"><a href="#cb2-29" aria-hidden="true" tabindex="-1"></a>                new_columns.append(<span class="ss">f'</span><span class="sc">{</span>column<span class="sc">}</span><span class="ss">_&lt;</span><span class="sc">{</span><span class="va">self</span><span class="sc">.</span>categories_[i][j]<span class="sc">}</span><span class="ss">&gt;'</span>)</span>
<span id="cb2-30"><a href="#cb2-30" aria-hidden="true" tabindex="-1"></a>                j <span class="op">+=</span> <span class="dv">1</span></span>
<span id="cb2-31"><a href="#cb2-31" aria-hidden="true" tabindex="-1"></a>        <span class="cf">return</span> new_columns</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell" data-execution_count="57">
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>df <span class="op">=</span> pd.read_csv(<span class="st">'one_promo_df.csv'</span>, index_col<span class="op">=</span>[<span class="dv">0</span>])</span>
<span id="cb3-2"><a href="#cb3-2" aria-hidden="true" tabindex="-1"></a>df.head(<span class="dv">20</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="57">

<div>

<table class="dataframe table table-sm table-striped">
  <thead>
    <tr>
      <th></th>
      <th>order_id</th>
      <th>order_value</th>
      <th>promo_type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>89014417</td>
      <td>22</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>1</th>
      <td>89027235</td>
      <td>37</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>2</th>
      <td>88979766</td>
      <td>27</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>3</th>
      <td>89065392</td>
      <td>30</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>4</th>
      <td>88992397</td>
      <td>32</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>5</th>
      <td>89054226</td>
      <td>25</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>6</th>
      <td>89019462</td>
      <td>30</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>7</th>
      <td>89004871</td>
      <td>25</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>8</th>
      <td>89040172</td>
      <td>21</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>9</th>
      <td>89040144</td>
      <td>31</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>10</th>
      <td>89011586</td>
      <td>27</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>11</th>
      <td>89010120</td>
      <td>12</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>12</th>
      <td>89062426</td>
      <td>12</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>13</th>
      <td>89072723</td>
      <td>19</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>14</th>
      <td>88981465</td>
      <td>35</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>15</th>
      <td>89052139</td>
      <td>34</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>16</th>
      <td>89007805</td>
      <td>32</td>
      <td>SALE15</td>
    </tr>
    <tr>
      <th>17</th>
      <td>89043442</td>
      <td>29</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>18</th>
      <td>89060951</td>
      <td>30</td>
      <td>no_promo</td>
    </tr>
    <tr>
      <th>19</th>
      <td>89069655</td>
      <td>23</td>
      <td>no_promo</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
<div class="cell" data-execution_count="58">
<div class="sourceCode cell-code" id="cb4"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb4-1"><a href="#cb4-1" aria-hidden="true" tabindex="-1"></a>df.promo_type.unique()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="58">
<pre><code>array(['no_promo', 'SALE15'], dtype=object)</code></pre>
</div>
</div>
<div class="cell" data-pycharm="{&quot;name&quot;:&quot;#%%\n&quot;}" data-execution_count="59">
<div class="sourceCode cell-code" id="cb6"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb6-1"><a href="#cb6-1" aria-hidden="true" tabindex="-1"></a>encoder <span class="op">=</span> OneHotEncoder()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell" data-execution_count="60">
<div class="sourceCode cell-code" id="cb7"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb7-1"><a href="#cb7-1" aria-hidden="true" tabindex="-1"></a>encoder.fit_transform(df[[<span class="st">'promo_type'</span>]]) <span class="co">#getting new columns from the original promo_type column unique values</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="60">

<div>

<table class="dataframe table table-sm table-striped">
  <thead>
    <tr>
      <th></th>
      <th>promo_type_&lt;SALE15&gt;</th>
      <th>promo_type_&lt;no_promo&gt;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>99995</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>99996</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>99997</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>99998</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>99999</th>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
<p>99969 rows × 2 columns</p>
</div>
</div>
</div>
<p>We should drop promo_type_<no_promo> column because we’ll a 3d coeficient (3d feature which won’t give us anything new). If we keep it we will get alpha, beta (which is a free member) and a 3d unkown which will drag our linear regression.</no_promo></p>
<div class="cell" data-execution_count="61">
<div class="sourceCode cell-code" id="cb8"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb8-1"><a href="#cb8-1" aria-hidden="true" tabindex="-1"></a><span class="co">#now we can assign our variables and drop no_promo column</span></span>
<span id="cb8-2"><a href="#cb8-2" aria-hidden="true" tabindex="-1"></a>X <span class="op">=</span> encoder.fit_transform(</span>
<span id="cb8-3"><a href="#cb8-3" aria-hidden="true" tabindex="-1"></a>    df[[<span class="st">'promo_type'</span>]])<span class="op">\</span></span>
<span id="cb8-4"><a href="#cb8-4" aria-hidden="true" tabindex="-1"></a>    .drop(<span class="st">'promo_type_&lt;no_promo&gt;'</span>, axis<span class="op">=</span><span class="dv">1</span>)<span class="op">\</span></span>
<span id="cb8-5"><a href="#cb8-5" aria-hidden="true" tabindex="-1"></a>    .assign(aov<span class="op">=</span><span class="dv">1</span>)  <span class="co">#aov adds a free member coeficient of 1 into regression. OLS can't evaluate intercept if it's not added </span></span>
<span id="cb8-6"><a href="#cb8-6" aria-hidden="true" tabindex="-1"></a>                    <span class="co">#(in sklearn fit intercept). So when aov = 1 </span></span>
<span id="cb8-7"><a href="#cb8-7" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb8-8"><a href="#cb8-8" aria-hidden="true" tabindex="-1"></a>Y <span class="op">=</span> df[<span class="st">'order_value'</span>]</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell" data-execution_count="62">
<div class="sourceCode cell-code" id="cb9"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb9-1"><a href="#cb9-1" aria-hidden="true" tabindex="-1"></a>estimator <span class="op">=</span> OLS(Y, X).fit()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>In linear regression we are testing the following:</p>
<p>H0: that coeficient is equal to 0</p>
<p>H1: coeficient is not = 0</p>
<div class="cell" data-pycharm="{&quot;name&quot;:&quot;#%%\n&quot;}" data-execution_count="63">
<div class="sourceCode cell-code" id="cb10"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb10-1"><a href="#cb10-1" aria-hidden="true" tabindex="-1"></a><span class="bu">print</span>(estimator.summary())</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>                            OLS Regression Results                            
==============================================================================
Dep. Variable:            order_value   R-squared:                       0.000
Model:                            OLS   Adj. R-squared:                  0.000
Method:                 Least Squares   F-statistic:                     1.166
Date:                Sun, 02 Oct 2022   Prob (F-statistic):              0.280
Time:                        13:46:47   Log-Likelihood:            -3.5255e+05
No. Observations:               99969   AIC:                         7.051e+05
Df Residuals:                   99967   BIC:                         7.051e+05
Df Model:                           1                                         
Covariance Type:            nonrobust                                         
=======================================================================================
                          coef    std err          t      P&gt;|t|      [0.025      0.975]
---------------------------------------------------------------------------------------
promo_type_&lt;SALE15&gt;    -0.0938      0.087     -1.080      0.280      -0.264       0.076
aov                    29.4996      0.027   1075.409      0.000      29.446      29.553
==============================================================================
Omnibus:                       15.216   Durbin-Watson:                   2.006
Prob(Omnibus):                  0.000   Jarque-Bera (JB):               15.630
Skew:                           0.018   Prob(JB):                     0.000404
Kurtosis:                       3.050   Cond. No.                         3.37
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.</code></pre>
</div>
</div>
<p>Good thing about this linear regression is we don’t need to look at MAPE, and don’t need to maximize R^2. We only need to look at statistical significance of our coefficients:</p>
<p>promo_type_SALE15 p-values is 0.28 which is much higher than our significance level, meaning we can’t reject H0. So this coefficient is essentially = 0. Our dispersion is somewhat high and confidence interval includes 0 (-0.264 to 0.076). This means that promo has very low effect on the mean check value (which is good for us!). If we see an increase in in number of orders in total when we are offering this promo, we can say that this is a good promo because it increases number of orders but doesn’t decrease (has very low effect) our mean order value. However, it is also possible that our promo is just used on a small amount of orders.</p>
<p>aov P-values is statistically significant meaning it is not a random feature.</p>
<hr>
</section>
<section id="what-if-we-have-multiple-promos" class="level3">
<h3 class="anchored" data-anchor-id="what-if-we-have-multiple-promos">What if we have multiple promos?</h3>
<p>Now let’s see an example with several promotions to understand which ones work best for our business.</p>
<div class="cell" data-pycharm="{&quot;name&quot;:&quot;#%%\n&quot;}" data-execution_count="64">
<div class="sourceCode cell-code" id="cb12"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb12-1"><a href="#cb12-1" aria-hidden="true" tabindex="-1"></a>df_multi <span class="op">=</span> pd.read_csv(<span class="st">'multiple_promo_df.csv'</span>, index_col<span class="op">=</span>[<span class="dv">0</span>])</span>
<span id="cb12-2"><a href="#cb12-2" aria-hidden="true" tabindex="-1"></a>df_multi.head()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="64">

<div>

<table class="dataframe table table-sm table-striped">
  <thead>
    <tr>
      <th></th>
      <th>gmv</th>
      <th>title</th>
      <th>delivery_discount</th>
      <th>surge_increment</th>
      <th>order_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>22</td>
      <td>SALE15</td>
      <td>0</td>
      <td>0</td>
      <td>768977643</td>
    </tr>
    <tr>
      <th>1</th>
      <td>44</td>
      <td>LUCKY</td>
      <td>1</td>
      <td>0</td>
      <td>768977644</td>
    </tr>
    <tr>
      <th>2</th>
      <td>26</td>
      <td>SUMMER</td>
      <td>0</td>
      <td>0</td>
      <td>768977645</td>
    </tr>
    <tr>
      <th>3</th>
      <td>26</td>
      <td>no_promo</td>
      <td>0</td>
      <td>0</td>
      <td>768977646</td>
    </tr>
    <tr>
      <th>4</th>
      <td>39</td>
      <td>no_promo</td>
      <td>0</td>
      <td>0</td>
      <td>768977647</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
<p>gmv - order value</p>
<p>title - promo code</p>
<p>delivery_discount - wheather ther is or no discount on delivery</p>
<p>surge_increment - this is when our delivery cost increased</p>
<p>order_id - self-explanatory</p>
<div class="cell" data-pycharm="{&quot;name&quot;:&quot;#%%\n&quot;}" data-execution_count="65">
<div class="sourceCode cell-code" id="cb13"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb13-1"><a href="#cb13-1" aria-hidden="true" tabindex="-1"></a>df_multi.query(<span class="st">'title == "no_promo"'</span>).shape[<span class="dv">0</span>] <span class="op">/</span> df_multi.shape[<span class="dv">0</span>]</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="65">
<pre><code>0.5904545516019529</code></pre>
</div>
</div>
<p>59% of orders have no promotions, and therefore 41% with</p>
<div class="cell" data-execution_count="66">
<div class="sourceCode cell-code" id="cb15"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a>encoder.fit_transform(df_multi[[<span class="st">'title'</span>]]).head(<span class="dv">3</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="66">

<div>

<table class="dataframe table table-sm table-striped">
  <thead>
    <tr>
      <th></th>
      <th>title_&lt;LUCKY&gt;</th>
      <th>title_&lt;SALE15&gt;</th>
      <th>title_&lt;SORRY&gt;</th>
      <th>title_&lt;SUMMER&gt;</th>
      <th>title_&lt;TAKE30&gt;</th>
      <th>title_&lt;WINTER&gt;</th>
      <th>title_&lt;no_promo&gt;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
<p>again we don’t need the title_<no_promo> column because it doesn’t add anything new (you can derive it from all other columns)</no_promo></p>
<div class="cell" data-execution_count="68">
<div class="sourceCode cell-code" id="cb16"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb16-1"><a href="#cb16-1" aria-hidden="true" tabindex="-1"></a>Ym <span class="op">=</span> df_multi[<span class="st">'gmv'</span>]</span>
<span id="cb16-2"><a href="#cb16-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb16-3"><a href="#cb16-3" aria-hidden="true" tabindex="-1"></a>Xm <span class="op">=</span> encoder.fit_transform(df_multi[[<span class="st">'title'</span>]])<span class="op">\</span></span>
<span id="cb16-4"><a href="#cb16-4" aria-hidden="true" tabindex="-1"></a>    .drop(<span class="st">'title_&lt;no_promo&gt;'</span>, axis<span class="op">=</span><span class="dv">1</span>)<span class="op">\</span></span>
<span id="cb16-5"><a href="#cb16-5" aria-hidden="true" tabindex="-1"></a>    .assign(aov<span class="op">=</span><span class="dv">1</span>)</span>
<span id="cb16-6"><a href="#cb16-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb16-7"><a href="#cb16-7" aria-hidden="true" tabindex="-1"></a>Xm[<span class="st">'delivery_discount'</span>] <span class="op">=</span> df_multi[<span class="st">'delivery_discount'</span>]</span>
<span id="cb16-8"><a href="#cb16-8" aria-hidden="true" tabindex="-1"></a>Xm[<span class="st">'surge_increment'</span>] <span class="op">=</span> df_multi[<span class="st">'surge_increment'</span>]</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell" data-execution_count="69">
<div class="sourceCode cell-code" id="cb17"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb17-1"><a href="#cb17-1" aria-hidden="true" tabindex="-1"></a>Xm.head(<span class="dv">5</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="69">

<div>

<table class="dataframe table table-sm table-striped">
  <thead>
    <tr>
      <th></th>
      <th>title_&lt;LUCKY&gt;</th>
      <th>title_&lt;SALE15&gt;</th>
      <th>title_&lt;SORRY&gt;</th>
      <th>title_&lt;SUMMER&gt;</th>
      <th>title_&lt;TAKE30&gt;</th>
      <th>title_&lt;WINTER&gt;</th>
      <th>aov</th>
      <th>delivery_discount</th>
      <th>surge_increment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
<div class="cell" data-execution_count="70">
<div class="sourceCode cell-code" id="cb18"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb18-1"><a href="#cb18-1" aria-hidden="true" tabindex="-1"></a>Ym.head(<span class="dv">5</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="70">
<pre><code>0    22
1    44
2    26
3    26
4    39
Name: gmv, dtype: int64</code></pre>
</div>
</div>
<div class="cell" data-execution_count="71">
<div class="sourceCode cell-code" id="cb20"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a>estimator_multi <span class="op">=</span> OLS(Ym, Xm).fit()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell" data-execution_count="72">
<div class="sourceCode cell-code" id="cb21"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb21-1"><a href="#cb21-1" aria-hidden="true" tabindex="-1"></a><span class="bu">print</span>(estimator_multi.summary())</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>                            OLS Regression Results                            
==============================================================================
Dep. Variable:                    gmv   R-squared:                       0.058
Model:                            OLS   Adj. R-squared:                  0.058
Method:                 Least Squares   F-statistic:                     2844.
Date:                Sun, 02 Oct 2022   Prob (F-statistic):               0.00
Time:                        13:46:58   Log-Likelihood:            -1.3137e+06
No. Observations:              369705   AIC:                         2.627e+06
Df Residuals:                  369696   BIC:                         2.628e+06
Df Model:                           8                                         
Covariance Type:            nonrobust                                         
=====================================================================================
                        coef    std err          t      P&gt;|t|      [0.025      0.975]
-------------------------------------------------------------------------------------
title_&lt;LUCKY&gt;        -4.7214      0.055    -86.588      0.000      -4.828      -4.615
title_&lt;SALE15&gt;       -3.3930      0.042    -80.113      0.000      -3.476      -3.310
title_&lt;SORRY&gt;        -2.2311      0.130    -17.203      0.000      -2.485      -1.977
title_&lt;SUMMER&gt;       -2.6650      0.044    -61.168      0.000      -2.750      -2.580
title_&lt;TAKE30&gt;       -6.8097      0.088    -77.495      0.000      -6.982      -6.638
title_&lt;WINTER&gt;       -4.7933      0.069    -69.641      0.000      -4.928      -4.658
aov                  31.5263      0.019   1661.272      0.000      31.489      31.564
delivery_discount    -2.0326      0.043    -47.626      0.000      -2.116      -1.949
surge_increment       0.8302      0.082     10.149      0.000       0.670       0.991
==============================================================================
Omnibus:                       42.868   Durbin-Watson:                   1.998
Prob(Omnibus):                  0.000   Jarque-Bera (JB):               42.878
Skew:                           0.026   Prob(JB):                     4.89e-10
Kurtosis:                       3.002   Cond. No.                         9.62
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.</code></pre>
</div>
</div>
<p>Here we see that for all features p-value is 0.00 and is statistically significant.</p>
<p>We can see that all promos lower the average check value. Sometimes it’s ok. We can see that for example for SALE15 code our average order value dropped by USD3.39 which is less than expected USD4.465 (see below). So it’s a decent promo. Meaning we a gaining USD1.075 from this promo on each order. On average we also give USD2 discount for delivery, and our delivery price surges by USD0.83.</p>
<section id="our-average-15-discount-should-be-around-4.46-see-below." class="level4">
<h4 class="anchored" data-anchor-id="our-average-15-discount-should-be-around-4.46-see-below.">Our average 15% discount should be around $4.46 (see below).</h4>
<p>If we a below this number means this promotion is earning us</p>
<div class="cell" data-execution_count="76">
<div class="sourceCode cell-code" id="cb23"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb23-1"><a href="#cb23-1" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb23-2"><a href="#cb23-2" aria-hidden="true" tabindex="-1"></a>Ym.mean() <span class="op">*</span> <span class="fl">0.15</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="76">
<pre><code>4.465749178398994</code></pre>
</div>
</div>
</section>
</section>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const clipboard = new window.ClipboardJS('.code-copy-button', {
    target: function(trigger) {
      return trigger.previousElementSibling;
    }
  });
  clipboard.on('success', function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  });
  function tippyHover(el, contentFn) {
    const config = {
      allowHTML: true,
      content: contentFn,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start'
    };
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      return note.innerHTML;
    });
  }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->



</body></html>
