clash科学上网：clash for windows 详细教程

1. 简介
Clash 是一个使用 Go 语言编写，基于规则的跨平台代理软件核心程序。
Clash for Windows 是目前在 Windows 上唯一可用的图形化 Clash 分支。通过 Clash API 来配置和控制 Clash 核心程序，便于用户可视化操作和使用。
支持的协议： Vmess, Shadowsocks, Snell , SOCKS5 , ShadowsocksR（在0.11.2版本加入）
【注】：ClashR for Windows 是第三方修改版本，已汉化。支持SSR协议，使用方法与原版相同。下载地址请看第3节。
ClashR(for Windows)（Whojave）项目地址：https://github.com/WhoJave/clash/releases

2. 整理教程时的系统环境
Windows 10 1903
Clash for Windows 0.8.0

此教程针对手持 Clash 订阅链接的用户，

V2ray订阅链接需先转换成Clash 订阅链接才能使用。查看 订阅链接转换教程。

没有V2ray订阅链接？请移步 👉 https://sesegu.github.io/ivpn 免费获取。

3. 下载和安装 Clash for Windows
原版CFW的Github发布地址：https://github.com/Fndroid/clash_for_windows_pkg/releases

由于 Clash for Windows 没有任何有效的数字签名，因此 SmartScreen 可能会弹出提示，请点击「更多信息」，然后选择「仍要运行」。

4. 如何汉化 Clash for Windows？
汉化版CFW的Github发布地址：https://github.com/ender-zhao/Clash-for-Windows_Chinese

对于部分新用户来说，纯英文的界面确实有一些不太友好，但是我们可以通过很简单的操作来自行汉化Clash for Windows。以下操作需要在Clash未在运行的前提下进行：

如果是安装版的Clash，那么可以对着桌面图标单击右键，选择打开文件所在位置，即可找到clash主程序所在的Clash for Windows文件夹。然后双击进入resources文件夹，找到app.asar这个文件。

将Clash for Windows汉化文件，替换掉原来的app.asar文件。

5. 快速配置 Clash for Windows
打开 Clash for Windows 应用程序，在左侧的标签页中选择「Profiles」， 在顶部输入您的 Clash 订阅链接 ，然后点击「Download」按钮。

<figure data-type="image" tabindex="1"><img src="img/1.png" alt="1-订阅.png" loading="lazy"></figure>
<p>Clash for Windows 会自动拉取配置文件进行更新，如果一切顺利，你应当可以看到绿色提示信息「Success!」，并且可以看到一个新增的配置文件：</p>
<figure data-type="image" tabindex="2"><img src="img/2.png" alt="2-订阅成功.png" loading="lazy"></figure>
<p>点击新增的配置文件来切换到该配置，然后点击「Proxies」标签页来切换接入点，将顶部的出站模式选择为「Rule」。<br>
此模式下你的网络访问请求将通过 Clash for Winows 进行<strong>分流处理</strong>。</p>
<p>展开此折叠框以了解“分流”</p>
<figure data-type="image" tabindex="3"><img src="img/3.png" alt="3-选择模式.png" loading="lazy"></figure>
<p>在「Proxy」策略组中选择所想要使用的接入点。Proxy 策略组是用于访问国际网络的默认策略，在不进行其他修改的情况下，所有国际网络的访问都通过 Proxy 策略组中选择的接入点进行。</p>
<p>图中所示的其它策略组为本人出于自身实际需求自行配置的，请以自己的实际配置为准。</p>
<h2 id="6-启动-clash-for-windows">6. 启动 Clash for Windows</h2>
<p>请务必确保开关是启用状态。<br>
经博客聊天窗口统计，大量新手用户因未打开开关，导致连不上代理。</p>
<p>返回到「General」部分，将「System Proxy」的开关更改为<strong>绿色</strong>状态即可开始使用。此外，建议将「Start with Windows」也更改为<strong>绿色</strong>来让 Clash for Windows 在开机时自动启动。</p>
<figure data-type="image" tabindex="4"><img src="img/4.png" alt="4-打开代理.png" loading="lazy"></figure>
<hr>
<h4 id="本地拖拽yaml文件">本地拖拽YAML文件</h4>
<p>在无法直接从软件里更新自己的订阅时，可以复制你的链接，直接粘贴到浏览器打开，然后复制全部的文本，在桌面新建一个文本文档（TXT格式），然后粘贴到文档里，保存后将文件的扩展名更改为 YAML 。然后直接拖拽到软件的 Proflies 界面。</p>
<p>这是一种曲线救国的方法。此方法导入的配置无法进行更新，需要更新时请重新来一遍。</p>
<p>简单的使用教程到这里就结束了 ，当前已经可以进行正常的科学上网。<br>
有兴趣的话可以接着了解下边的内容。</p>
<hr>
<p>请注意<br>
当配置文件存在错误时，无法在「Profiles」界面切换，请根据提示进行修改<br>
若出现如图所示的情况，说明您未点击刚才新增的配置文件，请返回「Profiles」点击选择对应的配置文件。</p>
<figure data-type="image" tabindex="5"><img src="img/5.png" alt="9-配置错误示例.png" loading="lazy"></figure>
<h2 id="7-其它知识">7. 其它知识</h2>
<h3 id="71-clash-for-windows-界面简介">7.1 Clash for Windows 界面简介</h3>
<figure data-type="image" tabindex="6"><img src="img/6.png" alt="8-界面简介.png" loading="lazy"></figure>
<ul>
<li><code>General（常规）</code>：
<ul>
<li><code>Port</code>、<code>Socks Port</code>；分别为 HTTP、SOCKS 代理端口，点击终端图案可以打开一个配置了代理的命令行窗口，点击端口数字可以复制该命令；</li>
<li><code>Allow LAN</code>：启用局域网共享代理功能；‘</li>
<li><code>Log Level</code>：日志等级；</li>
<li><code>Home Directory</code>：点击下方路径直达 <code>C:\Users\用户名\.config\clash</code> 文件夹；</li>
<li><code>GeoIP Database</code>：点击下方日期可更新 GeoIP 数据库；</li>
<li><code>UWP Loopback</code> ：可以用来使 UWP 应用解除回环代理限制；</li>
<li><code>Tap Device</code> ：安装 cfw-tap 网卡，可用于处理不遵循系统代理的软件（实际启动 tap 模式需要更改配置文件）；</li>
<li><code>General YML</code>：编辑 <code>config.yml</code> 文件，可用于配置部分 <strong>General</strong> 页面内容；</li>
<li><code>Dark Theme</code>：控制暗色模式；</li>
<li><code>System Proxy</code>：启用系统代理；</li>
<li><code>Start with Windows</code>：设置开机自启；</li>
</ul>
</li>
<li><code>Proxies（代理）</code>：选择代理方式（Global - 全局、Rule - 规则、Direct - 直连）及策略组节点选择；</li>
<li><code>Profiles（配置管理）</code>：
<ul>
<li>用来下载远端配置文件和创建本地副本，且可在多个配置文件间切换；</li>
<li>对配置进行节点、策略组和规则的管理（添加节点、策略组和规则在各自编辑界面选择 <code>Add</code>, 调整策略组顺序、节点顺序及策略组节点使用拖拽的方式）；</li>
</ul>
</li>
<li><code>Logs（日志）</code>：显示当前请求命中规则类型和策略；</li>
<li><code>Connections (连接)</code>: 显示当前的 TCP 连接，可对某个具体连接执行关闭操作；</li>
<li><code>Feedback（反馈）</code>：显示软件、作者相关信息，内含捐赠码，欢迎打赏 <a href="https://github.com/Fndroid">Fndroid</a> 大佬以感谢和支持开发。</li>
</ul>
<h3 id="72-uwp-应用">7.2 UWP 应用</h3>
<p>如需使用 UWP 应用，还需要点击「EnableLoopback」来为 UWP 应用启用本地回环代理。在 Windows 10 中，微软出于安全性考虑，不允许 UWP 应用访问本地回环地址，这导致 UWP 应用无法直接使用代理，需要其他工具来破除这一限制。</p>
<p>Clash for Windows 集成了 EnableLoopback 程序，只需要点击「UWP Loopback」就可以使用。</p>
<figure data-type="image" tabindex="7"><img src="img/7.png" alt="5-UWP应用.png" loading="lazy"></figure>
<p>打开后一般直接点击 Exempt All 勾选所有 UWP 应用，然后点击 Save Changes 即可。请注意安装新的 UWP 应用后需要重新设置。</p>
<h3 id="73-更新-geoip-数据库">7.3 更新 GeoIP 数据库</h3>
<p>在「General」界面点击「GeoIP Database」来更新 MaxMind 的 GeoIP2 Lite 数据库。此数据库用于 Geo 规则和 DNS 判断，在更新软件时，GeoIP 库会同步更新，一般不需要频繁刷新。</p>
<figure data-type="image" tabindex="8"><img src="img/8.png" alt="7-更新IP库.png" loading="lazy"></figure>
<h3 id="74-tap-设备">7.4 TAP 设备</h3>
<h4 id="741-介绍">7.4.1 介绍</h4>
<p>Clash for Windows 中提供了一个新的 TAP 模式。对于不遵循系统代理的软件，TAP 模式可以接管其流量并交由 CFW 处理。</p>
<h4 id="742-cfw090及以后版本">7.4.2 CFW0.9.0及以后版本</h4>
<h5 id="安装tap网卡">安装TAP网卡</h5>
<p>点击 <code>General</code>页面下的 <code>TAP Device</code>以安装 TAP 网卡，此网卡将用于接管系统流量，安装完成可在系统网络连接中看到一张新的虚拟网卡 <code>cfw-tap</code>。</p>
<h5 id="启动tap模式">启动TAP模式</h5>
<p>在配置文件中，添加以下字段(包含fake-ip)：</p>
<pre><code class="language-yaml">dns:
   enable: true
   enhanced-mode: fake-ip # 或 redir-host
   listen: 127.0.0.1:53
   nameserver:
      - 223.5.5.5
experimental:
  interface-name: WLAN # WLAN 为物理网卡名
</code></pre>
<h5 id="工作原理">工作原理</h5>
<p>此版本可以使用interface-name属性避免回环，所以可以不使用fake-ip模式，并且支持了UDP及IP类请求</p>
<h4 id="743-cfw0811及以前版本">7.4.3 CFW0.8.11及以前版本</h4>
<h5 id="安装tap网卡-2">安装TAP网卡</h5>
<p>点击 <code>General</code>页面下的 <code>TAP Device</code>以安装 TAP 网卡，此网卡将用于接管系统流量，安装完成可在系统网络连接中看到一张新的虚拟网卡 <code>cfw-tap</code>。</p>
<h5 id="启动tap模式-2">启动TAP模式</h5>
<p>在配置文件中，添加以下字段(包含fake-ip)：</p>
<pre><code class="language-yaml">dns:
   enable: true
   enhanced-mode: fake-ip
   listen: 127.0.0.1:53
   nameserver:
      - 223.5.5.5
</code></pre>
<h5 id="工作原理-2">工作原理</h5>
<p>为避免循环，Clash for Windows 只会将Fake IP段的请求发往TAP，所以必须要在配置文件中指定 <code>enhanced-mode: fake-ip</code>。<br>
Clash for Windows 会将系统 DNS 修改为 Clash 本地 DNS 服务器，获取到 Fake IP 的请求再发送至 TAP 网卡，这样设置可以让大部分软件能够正常工作，但如果请求直接使用IP地址而非域名，则不会被发往 TAP ，例如 Telegram 。</p>
<h4 id="744-cfw096版本">7.4.4 CFW0.9.6版本</h4>
<p>此版本调整了TAP逻辑，DNS在此版本要求监听在0.0.0.0:53<br>
同时，此版本已经将TAP安装DNS改为10.0.0.1了，Office不能联网的问题可以参考这个修改配置文件解决：<br>
https://github.com/Fndroid/clash_for_windows_pkg/issues/466#issuecomment-614716133</p>
<h3 id="75-url-scheme">7.5 URL Scheme</h3>
<p>CFW支持使用URL Scheme快速导入配置文件：</p>
<pre><code class="language-yaml">clash://install-config?url=&lt;encoded URI&gt;
</code></pre>
<h3 id="76-便携模式">7.6 便携模式</h3>
<p><strong>版本要求：</strong><br>
从0.4.0开始，Clash for Windows提供简单的便携支持</p>
<p><strong>使用方法：</strong><br>
进入Release页面下载最新后缀为 <code>.zip或.7z</code>的免安装包并解压至希望安装的目录下（如移动硬盘、U盘等）</p>
<p><strong>配置文件：</strong><br>
进入 <code>安装目录/resources/static/files/</code>目录中进行如下操作：</p>
<ol>
<li>新建config.yml（文件可以为空，但一定要创建）</li>
<li>重新启动Clash for Windows<br>
此时文件夹目录中还有其他文件及文件夹，请勿对其修改</li>
</ol>
<p><strong>启动及更新：</strong><br>
安装目录下Clash for Windows.exe即为软件入口，点击启动即可<br>
如需更新Clash for Windows，只需下载对应zip安装包，解压并覆盖至软件目录即可</p>
<h2 id="8-常见问题">8. 常见问题</h2>
<h3 id="81-界面显示不全无法操作">8.1 界面显示不全，无法操作</h3>
<p>删除 Home Directory 下 config.yml 文件并重启软件 如错误依旧，打开 logs 文件夹，选取最新日志文件分析</p>
<h3 id="82-升级后提示-xxx-not-found">8.2 升级后提示 xxx not found</h3>
<p>0.6.0 版本升级后，Clash 核心增加对规则部分的校验，如果策略不存在，则不再忽略而提示错误，根据错误信息检查配置文件并进行排除即可</p>
<h3 id="83-系统代理自动关闭或打开">8.3 系统代理自动关闭或打开</h3>
<p>清除系统代理设置 如无法解决，则检查是否有其他安全/代理软件修改代理设置</p>
<p><strong>如果装有QQ输入法或者QQ音乐等腾讯系软件，建议卸载或者禁止开机自动启动，此类毒瘤软件会更改系统代理设置。</strong><br>
<strong>浏览器里有代理类插件的话（包括Switch Omgega、各种VPN、集装箱等），请尝试删除代理插件，然后重启电脑。</strong></p>
<p>详见：https://github.com/Fndroid/clash_for_windows_pkg/issues/312</p>
<h3 id="84-无法访问网页">8.4 无法访问网页</h3>
<p>0.6.0 版本升级后，Clash 核心使用自定义 DNS 设置进行服务器及直连域名的解析，所以当日志中出现大量 All DNS Failed! 日志时，请重新设置合适的 DNS</p>
<p>如果不使用 TAP ，建议将 DNS 关闭</p>
<h3 id="85-tap-无法安装">8.5 TAP 无法安装</h3>
<p>检查是否已经安装其他 TAP 设备，若是，可以先在设备管理器中将其删除后重试</p>
<h3 id="86-安装074-之后版本首次使用时不显示接入点">8.6 安装0.7.4 之后版本首次使用时不显示接入点</h3>
<p>新版 Clash for Windows 在下载配置文件后并不会默认切换到新的配置文件（与旧版本不同），否则仍然使用的是默认配置文件。</p>
<h3 id="87-替换配置文件后不显示接入点">8.7 替换配置文件后不显示接入点</h3>
<p>这可能是因为 <code>Clash for Windows</code> 的基础配置文件 <code>config.yml</code> 被修改。要解决此问题，点击 <code>Clash for Windows General</code> 标签页上的 <code>Home Directory</code> 进入 <code>Clash for Windows</code> 配置目录，然后删除 <code>config.yml</code> 文件（不是 <code>config.yaml</code>），退出并重启打开 <code>Clash for Windows</code>，重新进行配置步骤。</p>
<h3 id="88-系统代理异常关闭">8.8 系统代理异常关闭</h3>
<p><strong>解决办法：</strong></p>
<p>① 打开注册表编辑器（可以自行百度如何打开）</p>
<p>② 进入HKEY_CURRENT_USERSoftwareMicrosoftWindowsCurrentVersionInternet SettingsConnections</p>
<p>③ 选择文件 - 导出，输入文件名备份当前分支</p>
<p>④ 删除所有条目</p>
<p>⑤ 重新开关System Proxy</p>
<p>⑥ 刷新注册表编辑器，查看条目是否重新出现，若否，选择文件 - 导入恢复设置</p>
<p><strong>如果装有QQ输入法或者QQ音乐等腾讯系软件，建议卸载或者禁止开机自动启动，此类毒瘤软件会更改系统代理设置。</strong><br>
<strong>浏览器里有代理类插件的话（包括Switch Omgega、各种VPN、集装箱等），请尝试删除代理插件，然后重启电脑。</strong></p>
<p>详见：https://github.com/Fndroid/clash_for_windows_pkg/issues/312</p>
<h3 id="89-tap无法正常工作">8.9 TAP无法正常工作</h3>
<p>首先，重新启动CFW，且勿使用管理员权限启动。<br>
然后重新在 <code>General</code>中点击 <code>Install TAP Device</code>。</p>
<h2 id="9-geoip相关问题">9. GeoIP相关问题</h2>
<p>若遇到首页和log中有类似于下边这样的提示：</p>
<pre><code class="language-yaml">time=&quot;2020-01-08T03:23:08Z&quot; level=fatal 
msg=&quot;Can't load mmdb: error opening database: invalid MaxMind DB file&quot;
</code></pre>
<p>则说明 country.mmdb 文件有问题，请下载正常的 country.mmdb 文件，然后移动到 <code>.config\clash</code> 文件夹进行替换。</p>
<p>如果找不到该文件夹，可以在 CFW 首页点击 <code>Open Folder</code> 直达。</p>
<p>点击右边按钮下载country.mmdb 文件（下载后请自行解压）</p>
<h2 id="10-常见的订阅错误报告">10. 常见的订阅错误报告</h2>
<p>① 如果遇到以下提示：</p>
<pre><code class="language-yaml">Invalid Config:yaml:
unmarshal errors:line 1:cannot unmarshal !!str c3M6Ly9...
</code></pre>
<p>说明用错了订阅链接，请检查自己是不是复制错了或者多了空格之类的。</p>
<p>没有 Clash 订阅链接的可以使用<a href="https://bianyuan.xyz/">订阅转换API</a>来转换订阅链接。</p>
<p>② 如果遇到此类提示：</p>
<pre><code class="language-yaml">Invalid Config:
Value for 'Proxy' is invalid:Unexpected null or empty
</code></pre>
<p>说明你还没买套餐，或者订阅为空。请联系你所在机场的管理员。</p>
<p>③ 如果遇到此提示：</p>
<pre><code class="language-yaml">...cipher not supported
</code></pre>
<p>说明你使用的加密算法不被Clash支持。请更换加密算法。推荐：<code>ChaCha20-ietf-poly1305</code></p>