{
  "log": {
    "level": "warn",
    "output": "box.log",
    "timestamp": true
  },
  "dns": {
    "servers": [
      {
        "tag": "dns-remote",
        "address": "udp://1.1.1.1",
        "address_resolver": "dns-direct"
      },
      {
        "tag": "dns-trick-direct",
        "address": "https://sky.rethinkdns.com/",
        "detour": "direct-fragment"
      },
      {
        "tag": "dns-direct",
        "address": "1.1.1.1",
        "address_resolver": "dns-local",
        "detour": "direct"
      },
      {
        "tag": "dns-local",
        "address": "local",
        "detour": "direct"
      },
      {
        "tag": "dns-block",
        "address": "rcode://success"
      }
    ],
    "rules": [
      {
        "domain": [
          "prox-se.pointtoserver.com",
          "prox-gr.pointtoserver.com",
          "prox-hu.pointtoserver.com",
          "prox-ky.pointtoserver.com",
          "prox-tr.pointtoserver.com",
          "prox-is.pointtoserver.com",
          "prox-ae.pointtoserver.com",
          "prox-at.pointtoserver.com",
          "prox-mc.pointtoserver.com",
          "prox-bb.pointtoserver.com",
          "prox-ee.pointtoserver.com",
          "prox-ro.pointtoserver.com",
          "prox-es.pointtoserver.com",
          "prox-br.pointtoserver.com",
          "prox-ie.pointtoserver.com",
          "prox-rs.pointtoserver.com",
          "prox-al.pointtoserver.com",
          "prox-in.pointtoserver.com",
          "prox-bg.pointtoserver.com",
          "prox-bh.pointtoserver.com",
          "prox-lt.pointtoserver.com",
          "prox-au.pointtoserver.com",
          "prox-dk.pointtoserver.com",
          "prox-bo.pointtoserver.com",
          "[::ffff:426f:3de9]",
          "prox-vn.pointtoserver.com",
          "prox-ca.pointtoserver.com",
          "prox-af.pointtoserver.com",
          "prox-om.pointtoserver.com",
          "prox-bs.pointtoserver.com"
        ],
        "server": "dns-direct"
      },
      {
        "domain": "connectivitycheck.gstatic.com",
        "server": "dns-remote",
        "rewrite_ttl": 3000
      },
      {
        "domain_suffix": ".ir",
        "server": "dns-direct"
      },
      {
        "rule_set": [
          "geoip-ir",
          "geosite-ir"
        ],
        "server": "dns-direct"
      }
    ],
    "final": "dns-remote",
    "static_ips": {
      "sky.rethinkdns.com": [
        "104.17.147.22",
        "104.17.148.22",
        "188.114.97.3",
        "188.114.96.3",
        "2a06:98c1:3120::3",
        "2a06:98c1:3121::3"
      ]
    },
    "independent_cache": true
  },
  "inbounds": [
    {
      "type": "tun",
      "tag": "tun-in",
      "mtu": 9000,
      "inet4_address": "172.19.0.1/28",
      "auto_route": true,
      "strict_route": true,
      "endpoint_independent_nat": true,
      "stack": "mixed",
      "sniff": true,
      "sniff_override_destination": true
    },
    {
      "type": "mixed",
      "tag": "mixed-in",
      "listen": "127.0.0.1",
      "listen_port": 12334,
      "sniff": true,
      "sniff_override_destination": true
    },
    {
      "type": "direct",
      "tag": "dns-in",
      "listen": "127.0.0.1",
      "listen_port": 16450
    }
  ],
  "outbounds": [
    {
      "type": "selector",
      "tag": "select",
      "outbounds": [
        "auto",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇷🇴",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇫🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇿",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇬",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇦",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇭",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇱",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇲🇩",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇭🇳",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇺🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇾",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇿",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇰",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇺🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇰",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇬",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇧",
        "🇩🇰@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
        "🇫🇷@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇮🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇳🇱",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇩",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇭",
        "t.me/SiNAVM-US-4",
        "t.me/SiNAVM-US-5",
        "t.me/SiNAVM-US-6"
      ],
      "default": "auto"
    },
    {
      "type": "urltest",
      "tag": "auto",
      "outbounds": [
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇷🇴",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇫🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇿",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇬",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇦",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇭",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇱",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇲🇩",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇭🇳",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇺🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇾",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇿",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇰",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇺🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇸",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇪",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇷",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇰",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇺",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇬",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇧",
        "🇩🇰@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
        "🇫🇷@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇮🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇹",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇳🇱",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇩",
        "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇭",
        "t.me/SiNAVM-US-4",
        "t.me/SiNAVM-US-5",
        "t.me/SiNAVM-US-6"
      ],
      "url": "http://connectivitycheck.gstatic.com/generate_204",
      "interval": "10m0s",
      "tolerance": 1,
      "idle_timeout": "30m0s"
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇷🇴",
      "server": "prox-ro.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇫🇷",
      "server": "prox-es.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇪",
      "server": "prox-se.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇪",
      "server": "prox-ae.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇿",
      "server": "prox-al.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇹",
      "server": "prox-at.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇦🇺",
      "server": "prox-au.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇪",
      "server": "prox-in.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇬",
      "server": "prox-bg.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇷",
      "server": "prox-br.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇦",
      "server": "prox-ca.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇭",
      "server": "prox-mc.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇱",
      "server": "prox-dk.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇲🇩",
      "server": "prox-bo.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇭🇳",
      "server": "193.9.32.3",
      "server_port": 90,
      "username": "79QQqCPBLgrFzen5tP9kzLVX",
      "password": "NDbeMN6pQE5f3cuHmmmJrAfz",
      "tls": {
        "enabled": true,
        "server_name": "ieee.org",
        "insecure": true,
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🇺🇸",
      "server": "[::ffff:426f:3de9]",
      "server_port": 89,
      "username": "79QQqCPBLgrFzen5tP9kzLVX",
      "password": "NDbeMN6pQE5f3cuHmmmJrAfz",
      "tls": {
        "enabled": true,
        "server_name": "ieee.org",
        "insecure": true,
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "vless",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇾",
      "server": "92.112.126.34",
      "server_port": 11002,
      "uuid": "82af21a9-6a98-4da6-b951-72347b8e40d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "gallery.sourceforge.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "onYhi7WJAagIg9liEjsjDDdgpJQ5h-T8Z_lanR-kakQ",
          "short_id": "f57645e2"
        }
      },
      "transport": {
        "type": "httpupgrade",
        "host": "gallery.sourceforge.net",
        "path": "/ws",
        "headers": {
          "Host": "gallery.sourceforge.net",
          "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
        }
      }
    },
    {
      "type": "vless",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇨🇿",
      "server": "85.93.8.142",
      "server_port": 11002,
      "uuid": "82af21a9-6a98-4da6-b951-72347b8e40d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "gallery.sourceforge.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "cT2LpCh0dCr4jmoG6N2pDi8Pf8wxZZ4MFU-yDiVT_zI",
          "short_id": "b535db"
        }
      },
      "transport": {
        "type": "httpupgrade",
        "host": "gallery.sourceforge.net",
        "path": "/ws",
        "headers": {
          "Host": "gallery.sourceforge.net",
          "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
        }
      }
    },
    {
      "type": "vless",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇪",
      "server": "104.234.74.23",
      "server_port": 11002,
      "uuid": "3185f90f-f8eb-499b-b76c-6a27afaf970d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "gallery.sourceforge.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "R_zZS27sEP3wbCa7qX7jV0CcLiv1sAL_i_snquX-MAA",
          "short_id": "4f"
        }
      },
      "transport": {
        "type": "httpupgrade",
        "host": "gallery.sourceforge.net",
        "path": "/ws",
        "headers": {
          "Host": "gallery.sourceforge.net",
          "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
        }
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇩🇰",
      "server": "prox-om.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇺🇸",
      "server": "prox-bb.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇪",
      "server": "prox-ee.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇪🇸",
      "server": "prox-es.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇺",
      "server": "prox-vn.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇷",
      "server": "prox-tr.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇪",
      "server": "prox-af.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇷",
      "server": "prox-gr.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇰",
      "server": "prox-ro.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇭🇺",
      "server": "prox-hu.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇸🇬",
      "server": "prox-bh.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇬🇧",
      "server": "prox-is.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "🇩🇰@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
      "server": "85.190.238.27",
      "server_port": 89,
      "username": "79QQqCPBLgrFzen5tP9kzLVX",
      "password": "NDbeMN6pQE5f3cuHmmmJrAfz",
      "tls": {
        "enabled": true,
        "server_name": "ieee.org",
        "insecure": true,
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "🇫🇷@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻🟡",
      "server": "185.81.125.67",
      "server_port": 89,
      "username": "79QQqCPBLgrFzen5tP9kzLVX",
      "password": "NDbeMN6pQE5f3cuHmmmJrAfz",
      "tls": {
        "enabled": true,
        "server_name": "ieee.org",
        "insecure": true,
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇮🇹",
      "server": "prox-lt.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇱🇹",
      "server": "prox-bs.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇳🇱",
      "server": "prox-ie.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇹🇩",
      "server": "prox-rs.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "@𝗦𝗶𝗡𝗔𝗩𝗠👈🏻تلگرام🇧🇭",
      "server": "prox-ky.pointtoserver.com",
      "server_port": 10799,
      "username": "purevpn0s12300644",
      "password": "ioqn613v",
      "tls": {
        "server_name": "ieee.org",
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "t.me/SiNAVM-US-4",
      "server": "85.190.232.156",
      "server_port": 89,
      "username": "79QQqCPBLgrFzen5tP9kzLVX",
      "password": "NDbeMN6pQE5f3cuHmmmJrAfz",
      "tls": {
        "enabled": true,
        "server_name": "ieee.org",
        "insecure": true,
        "alpn": "h2,http/1.1"
      },
      "headers": {
        "Host": "stream.meet.google.com"
      }
    },
    {
      "type": "http",
      "tag": "t.me/SiNAVM-US-5",
      "server": "50.114.206.151",
      "server_port": 11001,
      "username": "Babak-US-2",
      "password": "q44tiTaJyf",
      "headers": {
        "Host": "google.com",
        "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
      }
    },
    {
      "type": "http",
      "tag": "t.me/SiNAVM-US-6",
      "server": "50.114.206.150",
      "server_port": 11001,
      "username": "Babak-US-1",
      "password": "yHFqYPbYgs",
      "headers": {
        "Host": "google.com",
        "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36"
      }
    },
    {
      "type": "dns",
      "tag": "dns-out"
    },
    {
      "type": "direct",
      "tag": "direct"
    },
    {
      "type": "direct",
      "tag": "direct-fragment",
      "tls_fragment": {
        "enabled": true,
        "size": "10-30",
        "sleep": "2-8"
      }
    },
    {
      "type": "direct",
      "tag": "bypass"
    },
    {
      "type": "block",
      "tag": "block"
    }
  ],
  "route": {
    "rules": [
      {
        "inbound": "dns-in",
        "outbound": "dns-out"
      },
      {
        "port": 53,
        "outbound": "dns-out"
      },
      {
        "process_name": [
          "Hiddify",
          "Hiddify.exe",
          "HiddifyCli",
          "HiddifyCli.exe"
        ],
        "outbound": "bypass"
      },
      {
        "domain_suffix": ".ir",
        "outbound": "direct"
      },
      {
        "rule_set": [
          "geoip-ir",
          "geosite-ir"
        ],
        "outbound": "direct"
      }
    ],
    "rule_set": [
      {
        "type": "remote",
        "tag": "geoip-ir",
        "format": "binary",
        "url": "https://raw.githubusercontent.com/hiddify/hiddify-geo/rule-set/country/geoip-ir.srs",
        "update_interval": "120h0m0s"
      },
      {
        "type": "remote",
        "tag": "geosite-ir",
        "format": "binary",
        "url": "https://raw.githubusercontent.com/hiddify/hiddify-geo/rule-set/country/geosite-ir.srs",
        "update_interval": "120h0m0s"
      }
    ],
    "final": "select",
    "auto_detect_interface": true,
    "override_android_vpn": true
  },
  "experimental": {
    "cache_file": {
      "enabled": true,
      "path": "clash.db"
    },
    "clash_api": {
      "external_controller": "127.0.0.1:16756",
      "secret": "iKKKeLnSA9rcztyB"
    }
  }
}
