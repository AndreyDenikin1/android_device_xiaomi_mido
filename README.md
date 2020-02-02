# Update all packages

<pre><code>sudo apt update && sudo apt upgrade -y</code></pre>


<p>use a script for download all requare require packages:</p>

<pre><code>cd ~ && sudo apt install git -y && git clone https://github.com/akhilnarang/scripts && cd scripts && sudo bash setup/android_build_env.sh && sudo bash setup/install_android_sdk.bash</code></pre>

# Sync and Build manually

<p>To initialize a shallow clone (recommend), which will save even more space, use a command like this:</p>

<pre><code>repo init --depth=1 -u https://gitlab.com/OrangeFox/Manifest.git -b fox_9.0</code></pre>

<p>Then to sync up:</p>

<pre><code>repo sync -j8 --force-sync</code></pre>



<p>To initialize a shallow clone use a command like this:</p>

<pre><code>git clone https://github.com/AndreyDenikin1/android_device_xiaomi_mido.git</code></pre>



<p>Then to build:</p>
<pre><code>. build/envsetup.sh && export ALLOW_MISSING_DEPENDENCIES=true 
lunch omni_mido-eng && mka recoveryimage</code></pre>
