tmp
===

禁ping

.. code:: shell

    iptables -A INPUT -p icmp --icmp-type 8 -s 0/0 -j DROP
