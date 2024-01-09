# android_development_roadmap


# Gradle environment variables for Android Studio to install gradle from local file directory, instead of downloading gradle from the internet

press <b>windows key</b> + <b>r -> </b> click <b>Advanced</b> tab -> click <b>Environment variables</b>
<br>
-> view under <b>User variables</b> -> click <b>New</b> -> for <b>Variable name</b>: type:
<pre><code>JAVA_HOME</code></pre>

-> for <b>Variable value</b>: type: (in this case, Android Studio installed in <b>Program Files</b>)
<pre><code>C:\Program Files\Android Studio\jbr</code></pre>


-> click <b>Ok</b>

<br>

-> view under <b>System variables</b> -> click <b>New</b> -> for <b>Variable name</b>: type:
<pre><code>JAVA_HOME</code></pre>

-> for <b>Variable value</b>: type: (in this case, Android Studio installed in <b>Program Files</b>)
<pre><code>C:\Program Files\Android Studio\jbr</code></pre>

-> click <b>Ok</b>

<br>

-> view under <b>System variables</b> -> view under <b>OS</b> -> click/select <b>Path</b> -> click <b>Edit</b> -> click <b>New</b> 

-> paste this:
<pre><code>%JAVA_HOME%\bin</code></pre>

-> click <b>New</b> -> paste this: (depends on where you installed <b>gradle</b>) after going to <b>https://gradle.org/install/</b> -> then scroll and click on <b>Binary-install</b>, hint: look for the <b>dists</b> folder)
<pre><code>C:\Program Files\.gradle\wrapper\dists\gradle-8.4-bin</code></pre>

-> click <b>Ok</b>

-> open <b>Android Studio</b> -> go to <b>SDK Manager</b> -> click <b>edit</b> for <b>Android SDK Location</b>

-> select the Sdk folder or paste this(depends on where you installed your Android SDK files(<b>AppData</b>), in this case, it's in the root directory of the <b>C</b> drive, ): 
<pre><code>C:\AppData\Local\Android\Sdk</code></pre>

-> click <b>Ok</b>

## now you be able to create a project that doesn't download gradle files from the internet, but instead, "download" gradle files from your local hard drive or flash/thumb drive
-> click <b>New Project</b>

<b></b>
