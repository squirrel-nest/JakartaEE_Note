# JakartaEE Development Note

<details open>
    <summary>
        <i><b>✨ JakartaEE Development RoadMap - 开发 的 路线图</b></i>
    </summary>
    <a id="jakartaee-development-note"></a>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ <a href="https://jakartaee.github.io/jakartaee-documentation/jakartaee-tutorial/current/index.html">Jakarta EE Tutorial</a> - 作为 脉络</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 知识点 结合 例子</b></i>
                            </summary>
                            <ul type="disc">
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 最新 Jakarta EE Tutorial 在线文档</b></i>
                            </summary>
                            <ul type="disc">
                                👉  ➡️  <a href="https://jakartaee.github.io/jakartaee-documentation/jakartaee-tutorial/current/index.html">Jakarta EE Tutorial</a>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ - </b></i>
                </summary>
                <ul type="disc">
                    <li>参考文档：<a href="https://dev.mysql.com/doc/refman/8.3/en/macos-installation.html">2.4 Installing MySQL on macOS</a></li>
                    <li>安装需要关注的一般注意事项，请 参阅：<a href="https://dev.mysql.com/doc/refman/8.3/en/macos-installation-notes.html">2.4.1 General Notes on Installing MySQL on macOS</a><br>
                        <ul>
                            <li>可以先按照 <a href="#mysql-install-on-macos-using-native-packages">2.4.2 Installing MySQL on macOS Using Native Packages</a> 的步骤 进行 安装，后续，再 看看 注意事项</li>
                            <li>如果要用 其它的 方式 按照，则 需要 先 看看 这个 一般性注意事项</li>
                        </ul>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ brew 的 安装方式</b></i>
                            </summary>
                            <a id="mysql-install-by-brew-mode" ></a>
                            <ul type="disc">
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ brew 安装 说明</b></i>
                                        </summary>
                                        <a id="explanation-for-mysql-install-by-brew-mode" ></a>
                                        <ul type="disc">
                                            <li>brew 安装 不是 最新 版</li>
                                            <li>因 与 mariadb 及 percona-server 同时 安装 会有 冲突
                                                <pre><code> Conflicts with:
mariadb (because mysql, mariadb, and percona install the same binaries)
percona-server (because mysql, mariadb, and percona install the same binaries)</code></pre>
                                            </li>
                                            <li>
                                                <details open>
                                                    <summary>
                                                        <i><b>✨ brew 安装 注意事项：</b></i>
                                                    </summary>
                                                    <a id="mysql-install-with-brew-note" ></a>
                                                    <ul type="disc">
                                                        <li>We've installed your MySQL database without a root password. To secure it run:
                                                            <pre><code>mysql_secure_installation</code></pre>
                                                        </li>
                                                        <li>MySQL is configured to only allow connections from localhost by default</li>
                                                        <li>To connect run:
                                                            <pre><code>mysql -uroot</code></pre>
                                                        </li>
                                                        <li>To restart mysql after an upgrade:
                                                            <pre><code>brew services restart mysql</code></pre>
                                                        </li>
                                                        <li>Or, if you don't want/need a background service you can just run:
                                                            <pre><code>/opt/homebrew/opt/mysql/bin/mysqld_safe --datadir=/opt/homebrew/var/mysql</code></pre>
                                                        </li>
                                                    </ul>
                                                </details>
                                            </li>
                                        </ul>
                                    </details>
                                </li>
