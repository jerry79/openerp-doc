.. i18n: .. _bazaar-faq-link:
.. i18n: 
.. i18n: F.A.Q on Bazaar version control system
.. i18n: --------------------------------------
..

.. _bazaar-faq-link:

Bazaar 版本控制的常见问题(F.A.Q)
--------------------------------------

.. i18n: .. contents::
..

.. 目录::

.. i18n: How to install bazaar ?
.. i18n: +++++++++++++++++++++++
..

Bazaar安装
+++++++++++++++++++++++

.. i18n: To install bazaar on any ubuntu distribution, you can use::
.. i18n: 
.. i18n:   apt-get install bzr
..

在Ubuntu系统上使用下面命令安装 Bazaar::

  apt-get install bzr

.. i18n: To work correctly, bzr version must be at least 1.3. Check it with the command::
.. i18n: 
.. i18n:   bzr --version
..

最好安装Bazaar版本>=1.3。下面的命令可以查看当前Bazaar的版本::

  bzr --version

.. i18n: If you have an older version check this url: http://bazaar-vcs.org/Download
..

如果Bazaar版本过低， 请到 http://bazaar-vcs.org/Download 下载最新版本

.. i18n: On debian, in any distribution, the 1.5 version is working, you can get it on
.. i18n: this url: http://backports.org/debian/pool/main/b/bzr/bzr_1.5-1~bpo40+1_i386.deb
..

Debian分发的系统可以使用1.5版本的Bazaar，下载地址为: http://backports.org/debian/pool/main/b/bzr/bzr_1.5-1~bpo40+1_i386.deb

.. i18n: How to create a login on launchpad ?
.. i18n: ++++++++++++++++++++++++++++++++++++
..

Launchpad 帐号
++++++++++++++++++++++++++++++++++++

.. i18n: Before you can commit on launchpad, you need to create a login.
..

要在Launchpad上提交代码，你肯定是需要去注册一下的。

.. i18n: Go to: https://launchpad.net --> log in / register on top right.
..

在 https://launchpad.net 首页的右上方的 Login/Register 就是咱注册的地儿了。

.. i18n: Enter your e-mail address and wait for an e-mail which will guide you through the process needed to create your login.
..

Enter your e-mail address and wait for an e-mail which will guide you through the process needed to create your login.

.. i18n: This login is only needed if you intend to commit on bazaar on openerp-commiter or on your own branch.
..

This login is only needed if you intend to commit on bazaar on openerp-commiter or on your own branch.

.. i18n: How to commit ?
.. i18n: +++++++++++++++
..

代码提交
+++++++++++++++

.. i18n: Once your login is created, you need to create some ssh keys and insert them on
.. i18n: your login page (see create ssh keys on the left). These ssh keys are needed to
.. i18n: commit.
..

Once your login is created, you need to create some ssh keys and insert them on
your login page (see create ssh keys on the left). These ssh keys are needed to
commit.

.. i18n: I advise you to follow these instructions to complete the creation of your
.. i18n: ssh keys: https://help.launchpad.net/YourAccount/CreatingAnSSHKeyPair
..

I advise you to follow these instructions to complete the creation of your
ssh keys: https://help.launchpad.net/YourAccount/CreatingAnSSHKeyPair

.. i18n: How to use Bazaar ?
.. i18n: +++++++++++++++++++
..

Bazaar使用指导
+++++++++++++++++++

.. i18n: There are two ways to work on bzr. Either you make a checkout or create a local branch.
..

There are two ways to work on bzr. Either you make a checkout or create a local branch.

.. i18n: Checkout method::
.. i18n: 
.. i18n:   bzr co lp:~openerp/openobject-addons/trunk -- to make a checkout
.. i18n:   bzr up                                     -- to make an update
.. i18n:   bzr ci                                     -- to commit
..

Checkout method::

  bzr co lp:~openerp/openobject-addons/trunk -- to make a checkout
  bzr up                                     -- to make an update
  bzr ci                                     -- to commit

.. i18n: Creating a branch::
.. i18n: 
.. i18n:   bzr branch lp:~<url> <local dir>             -- to create a branch locally
.. i18n:   bzr pull                                     -- to update the branch
.. i18n:   bzr push lp:~<url>                           -- to include your changes in the remote branch
..

Creating a branch::

  bzr branch lp:~<url> <local dir>             -- to create a branch locally
  bzr pull                                     -- to update the branch
  bzr push lp:~<url>                           -- to include your changes in the remote branch

.. i18n: In any case, when you experience some problems, you can do::
.. i18n: 
.. i18n:   bzr help
..

In any case, when you experience some problems, you can do::

  bzr help

.. i18n: or ``bzr help <command>``. e.g.::
.. i18n: 
.. i18n:   bzr help branch
..

or ``bzr help <command>``. e.g.::

  bzr help branch

.. i18n: Some problems
.. i18n: +++++++++++++
..

常见问题
+++++++++++++

.. i18n: Checkout does not work, I have this message error::
.. i18n: 
.. i18n:   bzr lp:~<url> 
.. i18n:   bzr: ERROR: Repository KnitPackRepository is not compatible with repository RemoteRepository
..

Checkout does not work, I have this message error::

  bzr lp:~<url> 
  bzr: ERROR: Repository KnitPackRepository is not compatible with repository RemoteRepository

.. i18n: There are two ways to correct it.
..

There are two ways to correct it.

.. i18n: Instead of using ``bzr co lp:~<url>``, use ``bzr co bzr+ssh://<yourlaunchpad login>@bazaar.launchpad.net/~<url>``
..

Instead of using ``bzr co lp:~<url>``, use ``bzr co bzr+ssh://<yourlaunchpad login>@bazaar.launchpad.net/~<url>``

.. i18n: check this url: https://bugs.launchpad.net/bzr/+bug/205579. Generally, you do::
.. i18n: 
.. i18n:  bzr branch lp:~<url> 
.. i18n:  bzr reconfigure --checkout
..

check this url: https://bugs.launchpad.net/bzr/+bug/205579. Generally, you do::

 bzr branch lp:~<url> 
 bzr reconfigure --checkout
