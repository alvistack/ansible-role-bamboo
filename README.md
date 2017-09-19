Ansible Role for Bamboo
=====================

[![Build Status](https://travis-ci.org/alvistack/ansible-role-bamboo.svg?branch=master)](https://travis-ci.org/alvistack/ansible-role-bamboo)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/ansible-role-bamboo.svg)](https://github.com/alvistack/ansible-role-bamboo)
[![GitHub license](https://img.shields.io/github/license/alvistack/ansible-role-bamboo.svg)](https://github.com/alvistack/ansible-role-bamboo/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/galaxy-alvistack.bamboo-blue.svg)](https://galaxy.ansible.com/alvistack/bamboo)

Ansible Role for Atlassian Bamboo Installation.

Requirements
------------

This role require Ansible 2.4 or higher.

This role was designed for Ubuntu 16.04/14.04 or CentOS 6/7.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>bamboo_catalina</td>
<td>no</td>
<td><code>/opt/atlassian/bamboo</code></td>
<td></td>
<td>Location for the Bamboo installation directory</td>
</tr>
<tr class="even">
<td>bamboo_connector_port</td>
<td>no</td>
<td><code>8085</code></td>
<td></td>
<td>Bamboo Apache Tomcat connector port</td>
</tr>
<tr class="odd">
<td>bamboo_context_path</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Context path for Bamboo installation</td>
</tr>
<tr class="even">
<td>bamboo_group</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the group that should own the file</td>
</tr>
<tr class="odd">
<td>bamboo_home</td>
<td>no</td>
<td><code>/var/atlassian/application-data/bamboo</code></td>
<td></td>
<td>Location for the Bamboo home directory</td>
</tr>
<tr class="even">
<td>bamboo_jvm_maximum_memory</td>
<td>no</td>
<td><code>768m</code></td>
<td></td>
<td>Bamboo JVM maximum memory usage</td>
</tr>
<tr class="odd">
<td>bamboo_jvm_minimum_memory</td>
<td>no</td>
<td><code>384m</code></td>
<td></td>
<td>Bamboo JVM minimum memory usage</td>
</tr>
<tr class="even">
<td>bamboo_jvm_support_recommended_args</td>
<td>no</td>
<td><code>-Datlassian.plugins.enable.wait=300</code></td>
<td></td>
<td>Atlassian Support recommended JVM arguments</td>
</tr>
<tr class="odd">
<td>bamboo_owner</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the user that should own the file</td>
</tr>
<tr class="even">
<td>bamboo_proxy_name</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Domain name for working with reverse proxy</td>
</tr>
<tr class="odd">
<td>bamboo_scheme</td>
<td>no</td>
<td><code>~</code></td>
<td><ul>
<li><code>http</code></li>
<li><code>https</code></li>
</ul></td>
<td>Scheme for working with reverse proxy</td>
</tr>
<tr class="even">
<td>bamboo_server_port</td>
<td>no</td>
<td><code>8007</code></td>
<td></td>
<td>Bamboo Apache Tomcat server port</td>
</tr>
<tr class="odd">
<td>bamboo_url</td>
<td>no</td>
<td><code>https://downloads.atlassian.com/software/bamboo/downloads/atlassian-bamboo-6.1.1.tar.gz</code></td>
<td></td>
<td>URL for download archive</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: bamboo
          bamboo_proxy_name: "bamboo.example.com"
          bamboo_scheme: "http"
          bamboo_owner: "bamboo"
          bamboo_group: "bamboo"

License
-------

-   Code released under [Apache License 2.0](https://github.com/alvistack/ansible-role-bamboo/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

