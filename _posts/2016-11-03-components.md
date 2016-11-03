 <div class="nine columns">
                 
          

<p>In Angular 2, Components are the main way we build and specify elements and logic on the page.</p>

<p>In Angular 1, we achieved this through directives, controllers, and scope. In Angular 2, all those concepts
are combined into Components.</p>

<h3 id="a-simple-component">A simple component</h3>

<p>Here’s a simple <a href="https://angular.io/docs/ts/latest/api/core/index/Component-decorator.html">Component</a> that renders our name, and a button that triggers a method to print our name to the console:</p>

<div class="language-javascript highlighter-rouge"><pre class="highlight"><code>
<span class="kr">import</span> <span class="p">{</span> <span class="nx">Component</span> <span class="p">}</span> <span class="nx">from</span> <span class="s1">'@angular/core'</span><span class="p">;</span>

<span class="err">@</span><span class="nx">Component</span><span class="p">({</span>
  <span class="na">selector</span><span class="p">:</span> <span class="s1">'my-component'</span><span class="p">,</span>
  <span class="na">template</span><span class="p">:</span> <span class="s1">'&lt;div&gt;Hello my name is {{name}}. &lt;button (click)="sayMyName()"&gt;Say my name&lt;/button&gt;&lt;/div&gt;'</span>
<span class="p">})</span>
<span class="kr">export</span> <span class="kr">class</span> <span class="nx">MyComponent</span> <span class="p">{</span>
  <span class="nx">constructor</span><span class="p">()</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">name</span> <span class="o">=</span> <span class="s1">'Max'</span>
  <span class="p">}</span>
  <span class="nx">sayMyName</span><span class="p">()</span> <span class="p">{</span>
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s1">'My name is'</span><span class="p">,</span> <span class="k">this</span><span class="p">.</span><span class="nx">name</span><span class="p">)</span>
  <span class="p">}</span>
<span class="p">}</span>

</code></pre>
</div>

<p>When we use the <code class="highlighter-rouge">&lt;my-component&gt;&lt;/my-component&gt;</code> tag in our HTML, this component will be created,
our constructor called, and rendered.</p>
