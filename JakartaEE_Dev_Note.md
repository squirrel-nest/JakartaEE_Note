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
                        所有的笔记，都要以官网 的 原始文档 为主，因为 官网的 文档 能 保持 最新，不会 过时。 -- 要养成看原始 文档 的 习惯。
                    </li>
                    <li>
                        需要的先学，不需要的暂时不用花时间学，先了解即可。（知道有这一回事，就可以）
                    </li>
                    <li>
                        穿插着学（不同的知识也很要这样，比如：数据库（以 MySQL 或 PostgreSQL，选一个 作为 优先级 学习），语言（Python 或 C 或 C++ 或 Java，容易上手就可以），还有比如 游戏引擎，排好 优先级），互相印证，不同部分的 关联点。
                    </li>
                    <li>
                        一定要 遵循 的 原则：学的过程用，用的过程学，知行合一，贯穿始终。 ---- 也就是 从实践到理论，再从理论到实践，实践与理论相结合的 原则。。。
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ MySQL Reference Manual 文档的下载</b></i>
                </summary>
                <a id="mysql-reference-download-note" ></a>
                <ul type="disc">
                    <li>如果网络通畅，则查看在线文档，更方便，并且，是：<br>
                        ➡️ 👉 👉 最新版本：<a href="https://dev.mysql.com/doc/refman/8.3/en/">MySQL 8.3 Reference Manual</a>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 下载 位置（网址）</b></i>
                            </summary>
                            <a id="source-for-mysql-reference-download" ></a>
                            <ul type="disc">
                                <li>当前位置（网址）：<a href="https://docs.oracle.com/en-us/iaas/mysql-database/doc/supporting-documentation.html">Supporting Documentation</a>  -> <br><a href="https://dev.mysql.com/doc/refman/en/">MySQL Reference Manual</a></li>
                                <li><a href="https://dev.mysql.com/doc/refman/en/">MySQL Documentation HomePage</a></li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 下载步骤</b></i>
                            </summary>
                            <a id="mysql-reference-download-step-by-step" ></a>
                            <ol type="i">
                                <li>打开 <a href="https://dev.mysql.com/doc/">MySQL Documentation HomePage</a></li>
                                <li>下拉到 Browse MySQL Documentation by: Product</li>
                                <li>找到 MySQL Server & MySQL Cluster</li>
                                <li>点击 ➕</li>
                                <li>选择要下载的版本，点击右边的 下载 符号</li>
                                <li>文档打开后，右键菜单，选择，另存为</li>
                                <li>选择保存位置，即可</li>
                            </ol>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 注意事项 及 问题处理</b></i>
                            </summary>
                            <a id="note-and-troubleshooting-for-mysql-reference-download" ></a>
                            <ol type="i">
                                <li>需要登陆 oracle 账号</li>
                                <li>关闭 VPN，否则会提示无权限</li>
                            </ol>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ 安装</b></i>
                </summary>
                <a id="mysql-install-by-mode"></a>
                <ul type="disc">
                    <li>
                        <a href="#mysql-install-and-config-for-mac-note">回到开头</a>
                    </li>
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
                                <i><b>✨ brew 的 安装方式</b></i> 👈 ✨ 不推荐，目前 推荐 <a href="#mysql-install-on-macos-using-native-packages">Native Packages 的 安装方式</a>，方便、快捷 ✨
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
