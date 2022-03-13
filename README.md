
      
  <div id="readme" class="Box-body readme blob js-code-block-container p-5 p-xl-6 gist-border-0">
    <article class="markdown-body entry-content container-lg" itemprop="text"><h2><a id="user-content-xcode" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#xcode"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Xcode</h2>
<p>Install xcode, it's required for other programs</p>
<div class="highlight highlight-source-shell"><pre>xcode-select --install</pre></div>
<h2><a id="user-content-homebrew" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#homebrew"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Homebrew</h2>
<p>Install Homebrew</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 /bin/bash -c <span class="pl-s"><span class="pl-pds">"</span><span class="pl-s"><span class="pl-pds">$(</span>curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh<span class="pl-pds">)</span></span><span class="pl-pds">"</span></span></pre></div>

<p>Check if Homebrew is correctly installed</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 brew doctor</pre></div>
<p>Install usefull packages</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 brew install redis sqlite wget </pre></div>
<p>Start redis service</p>
<pre><code>arch -x86_64 brew services start redis
</code></pre>
<p>To prevent "permission denied" with brew</p>
<div class="highlight highlight-source-shell"><pre>sudo chown -R "$USER":admin /usr/local</pre></div>   

          
# <h2>Cocoapods</h2>      
<p>Install Cocoapods</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 sudo gem install cocoapods -n /usr/local/bin</pre></div>
<p>Install ffi</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 sudo gem install ffi</pre></div>

          # <h2>Install zsh</h2>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 brew install zsh</pre></div>
<p>Install Oh My Zsh, type "Y" to confirm to change the defaukt shell to zsh</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 sh -c <span class="pl-s"><span class="pl-pds">"</span><span class="pl-s"><span class="pl-pds">$(</span>curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh<span class="pl-pds">)</span></span><span class="pl-pds">"</span></span></pre></div>
<p>Tell the system to use programs installed by Hombrew (in /usr/local/bin) rather than the OS default if it exists.</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>export PATH="/usr/local/bin:$PATH"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h3><a id="user-content-packages" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#packages"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Packages</h3>
<h4><a id="user-content-zsh-syntax-highlighting" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#zsh-syntax-highlighting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>zsh-syntax-highlighting</h4>
<p>Install zsh-syntax-highlighting</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 brew install zsh-syntax-highlighting </pre></div>
<p>To activate the syntax highlighting, enter this command to update the .zshrc file:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<p>You will also need to force reload of your .zshrc:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">source</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h4><a id="user-content-zsh-autosuggestions" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#zsh-autosuggestions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>zsh-autosuggestions</h4>
<p>Install zsh-autosuggestions</p>
<div class="highlight highlight-source-shell"><pre>arch -x86_64 brew install zsh-autosuggestions </pre></div>
<p>To activate the autosuggestions, enter this command to update the .zshrc file:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<p>You will also need to force reload of your .zshrc:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">source</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h4><a id="user-content-themes" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#themes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Themes</h4>
<p>Edit your <code>.zshrc</code>, find the key <code>ZSH_THEME</code>. By default it is "robbyrussell", change with :</p>
<pre><code>ZSH_THEME="ys"
</code></pre>
          To disable strange warning, 
          <pre><code>nano ~/.zshrc</code></pre>
          Set this line at top of file:
          <pre><code>ZSH_DISABLE_COMPFIX=true</code></pre>
          Save and relaunch terminal
          
<h2><a id="user-content-git-and-github" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#git-and-github"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Git and Github</h2>
          
        
<p>Install git</p>
<div class="highlight highlight-source-shell"><pre>brew install git</pre></div>
<p>Define your Git user (should be the same name and email you use for GitHub)</p>
<div class="highlight highlight-source-shell"><pre>git config --global user.name <span class="pl-s"><span class="pl-pds">"</span>FirstName LastName<span class="pl-pds">"</span></span>
git config --global user.email <span class="pl-s"><span class="pl-pds">"</span>your.email@cegelem.fr<span class="pl-pds">"</span></span></pre></div>
<h2><a id="user-content-mysql" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#mysql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>MySQL</h2>
<p>Install MySQL 8.0</p>
<div class="highlight highlight-source-shell"><pre>brew install mysql@8.0</pre></div>
<p>To have MySQL started now and auto restarted at login</p>
<div class="highlight highlight-source-shell"><pre>brew services start mysql@8.0</pre></div>
<p>Setup MySQL</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c"><span class="pl-c">#</span> 0 - mysql_secure_installation</span>
<span class="pl-c"><span class="pl-c">#</span> 1 - n</span>
<span class="pl-c"><span class="pl-c">#</span> 2 - toor</span>
<span class="pl-c"><span class="pl-c">#</span> 3 - toor</span>
<span class="pl-c"><span class="pl-c">#</span> 4 - y</span>
<span class="pl-c"><span class="pl-c">#</span> 5 - y</span>
<span class="pl-c"><span class="pl-c">#</span> 6 - y</span>
<span class="pl-c"><span class="pl-c">#</span> 7 - y</span>
mysql_secure_installation</pre></div>
<h2><a id="user-content-node" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#node"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Node</h2>
<p>Install Node LTS</p>
<div class="highlight highlight-source-shell"><pre>brew install node@12</pre></div>
<p>Tell the system where npm is installed</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>export PATH="/usr/local/opt/node@12/bin:$PATH"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<p>You will also need to force reload of your .zshrc:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">source</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<p>Install Font Awesome Pro</p>
<div class="highlight highlight-source-shell"><pre>npm config <span class="pl-c1">set</span> <span class="pl-s"><span class="pl-pds">"</span>@fortawesome:registry<span class="pl-pds">"</span></span> https://npm.fontawesome.com/ <span class="pl-k">&amp;&amp;</span> npm config <span class="pl-c1">set</span> <span class="pl-s"><span class="pl-pds">"</span>//npm.fontawesome.com/:_authToken<span class="pl-pds">"</span></span> 70FD2A39-6862-4A64-8284-82FB1564B4DE</pre></div>
<h2><a id="user-content-php" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#php"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>PHP</h2>
<h4><a id="user-content-php-74" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#php-74"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>PHP 7.4</h4>
<p>Install PHP 7.4</p>
<div class="highlight highlight-source-shell"><pre>brew install php@7.4</pre></div>
<p>To have PHP started now and auto restarted at login</p>
<div class="highlight highlight-source-shell"><pre>brew services start php@7.4</pre></div>
<p>Check PHP version</p>
<div class="highlight highlight-source-shell"><pre>php -v</pre></div>
<div class="highlight highlight-source-shell"><pre>PHP 7.4.4 (cli) (built: Mar 19 2020 20:12:27) ( NTS )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
    with Zend OPcache v7.4.4, Copyright (c), by Zend Technologies</pre></div>
<p>The php.ini and php-fpm.ini file can be found in <code>/usr/local/etc/php/7.4/</code></p>
<h4><a id="user-content-update-default-php-fpm" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#update-default-php-fpm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Update default PHP-FPM</h4>
<p>Update default PHP-FPM configuration via <code>/usr/local/etc/php/7.4/php-fpm.d/www.conf</code></p>
<div class="highlight highlight-source-shell"><pre>pm = dynamic
pm.max_children = 200
pm.start_servers = 20
pm.min_spare_servers = 10
pm.max_spare_servers = 20
pm.process_idle_timeout = 10s
pm.max_requests = 500</pre></div>
<h4><a id="user-content-xdebug-29" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#xdebug-29"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Xdebug 2.9</h4>
<p>Install Xdebug 2.9</p>
<div class="highlight highlight-source-shell"><pre>pecl install xdebug-2.9.4</pre></div>
<p>Check PHP version with Xdebug installed</p>
<div class="highlight highlight-source-shell"><pre>php -v</pre></div>
<div class="highlight highlight-source-shell"><pre>PHP 7.4.4 (cli) (built: Mar 19 2020 20:12:27) ( NTS )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
    with Xdebug v2.9.4, Copyright (c) 2002-2020, by Derick Rethans
    with Zend OPcache v7.4.4, Copyright (c), by Zend Technologies</pre></div>
<h4><a id="user-content-toggle-xdebug-29" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#toggle-xdebug-29"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Toggle Xdebug 2.9</h4>
<p>Toggle x-debug extension : <code>vim /usr/local/etc/php/7.4/php.ini</code> and comment / uncomment <code>zend_extension="xdebug.so"</code> line.</p>
<h4><a id="user-content-phpredis" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#phpredis"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>PHPRedis</h4>
<p>Install PHPRedis</p>
<div class="highlight highlight-source-shell"><pre>pecl install redis
<span class="pl-c"><span class="pl-c">#</span> ...</span>
<span class="pl-c"><span class="pl-c">#</span> enable igbinary serializer support? [no] : no</span>
<span class="pl-c"><span class="pl-c">#</span> enable lzf compression support? [no] : no</span>
<span class="pl-c"><span class="pl-c">#</span> ...</span></pre></div>
<p>Check if extension is enabled</p>
<div class="highlight highlight-source-shell"><pre>cat /usr/local/etc/php/7.4/php.ini <span class="pl-k">|</span> grep redis
<span class="pl-c"><span class="pl-c">#</span> extension="redis.so"</span></pre></div>
<h2><a id="user-content-composer" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#composer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Composer</h2>
<p>Install latest composer version</p>
<div class="highlight highlight-source-shell"><pre>brew install composer</pre></div>
<p>Tell the system where composer is installed by replacing your system user name.</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>export PATH="/Users/YOUR_SYSTEM_USER_NAME/.composer/vendor/bin:$PATH"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<p>You will also need to force reload of your .zshrc:</p>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">source</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h3><a id="user-content-packages-1" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#packages-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Packages</h3>
<p>Install useful packages</p>
<div class="highlight highlight-source-shell"><pre>composer global require laravel/valet tightenco/lambo phpunit/phpunit laravel/installer</pre></div>
<p>Install valet</p>
<div class="highlight highlight-source-shell"><pre>valet install</pre></div>
<p>Add sudoers files for Brew and Valet to make Valet commands run without passwords</p>
<div class="highlight highlight-source-shell"><pre>valet trust</pre></div>
<h2><a id="user-content-git-repositories" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#git-repositories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Git repositories</h2>
<h3><a id="user-content-ad-old" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#ad-old"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>ad-old</h3>
<p>Setup valet :</p>
<ul>
<li>need laravel/valet to be installed first</li>
<li>cd /to/ad-old/git/repository</li>
<li>enter the command below</li>
</ul>
<div class="highlight highlight-source-shell"><pre>valet link ad-old <span class="pl-k">&amp;&amp;</span> valet secure ad-old</pre></div>
<h2><a id="user-content-alias" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#alias"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Alias</h2>
<p>These aliases only work with ZSH terminal.</p>
<h3><a id="user-content-laravel" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#laravel"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Laravel</h3>
<div class="highlight highlight-source-shell"><pre><span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias art="php artisan"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h3><a id="user-content-repositories" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#repositories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Repositories</h3>
<div class="highlight highlight-source-shell"><pre><span class="pl-c"><span class="pl-c">#</span> ad-old</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias adold="cd ~/Codes/Cegelem/ad-old"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h3><a id="user-content-ssh" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#ssh"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SSH</h3>
<p>If you need to access to servers, you will find below a usefull set of aliases.</p>
<h4><a id="user-content-for-production" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#for-production"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>For production</h4>
<div class="highlight highlight-source-shell"><pre><span class="pl-c"><span class="pl-c">#</span> ad-old</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias adold-production="ssh forge@35.180.132.237 -i ~/.ssh/laravel_forge_cegelem"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h4><a id="user-content-for-staging" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#for-staging"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>For staging</h4>
<div class="highlight highlight-source-shell"><pre><span class="pl-c"><span class="pl-c">#</span> ad-old</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias adold-staging="ssh forge@52.47.189.116 -i ~/.ssh/laravel_forge_cegelem"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
<h3><a id="user-content-misc" class="anchor" aria-hidden="true" href="https://github.com/cegelem-sas/docs/blob/master/macOS/setup.md#misc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Misc</h3>
<div class="highlight highlight-source-shell"><pre><span class="pl-c"><span class="pl-c">#</span> composer i</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias ci="composer i"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc

<span class="pl-c"><span class="pl-c">#</span> composer i &amp;&amp; npm i &amp;&amp; npm run dev</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias cinidev="composer i &amp;&amp; npm i &amp;&amp; npm run dev"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc

<span class="pl-c"><span class="pl-c">#</span> composer i &amp;&amp; npm i &amp;&amp; npm run prod</span>
<span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>alias ciniprod="composer i &amp;&amp; npm i &amp;&amp; npm run prod"<span class="pl-pds">'</span></span> <span class="pl-k">&gt;&gt;</span> <span class="pl-k">~</span>/.zshrc</pre></div>
</article>
  </div>

    </div>
