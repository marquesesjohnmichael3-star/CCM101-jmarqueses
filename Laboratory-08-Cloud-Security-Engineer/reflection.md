# Mission 8 Reflection

## The Cloud Security Engineer

Before studying cloud security, I mostly thought about whether a server was running correctly and whether users could access its applications. This laboratory introduced another important responsibility: controlling who can communicate with the server and which services should be accessible.

One lesson I gained is that a host-based firewall provides protection directly on an individual machine. Even when the security of a larger network fails, the server can still apply its own rules to incoming connections. This additional protection is valuable because organizations should not depend on only one security measure.

I also understood why administrators must pay attention to open ports. A port may be necessary for a particular service, but leaving unused ports exposed can create opportunities for unauthorized access. Inspecting network connections and limiting permitted traffic are practical ways to reduce these risks.

Another important concern is database security. For example, exposing MySQL port 3306 to everyone on the internet can attract attempts to guess credentials or exploit weaknesses in database software. Sensitive information should be protected by restricting database connections to trusted systems and authorized users.

While performing the firewall procedures, I realized that a small configuration mistake could affect both security and accessibility. Allowing SSH before enabling UFW is a good example because the wrong order could disconnect an administrator from a remote server. I also learned that a successful local application request does not automatically prove that external traffic is securely filtered.

As I continue building my GitHub cloud computing portfolio, Mission 8 adds another area of learning to my previous laboratory activities. I want my portfolio to show not only completed commands but also my understanding of their purpose and limitations. This experience encourages me to become more careful when deploying and managing cloud services.
