# Simple realtime search engine with Twitter Streaming API support in 140 lines.

## Usage

    gem install msgpack-rpc   # MessagePack-RPC library
    gem install sytem_timer
    gem install memcache-client
    
    memcached -p 11211 &
    ./rrse-manager 5000 127.0.0.1:11211 &
    ./rsse-indexer  127.0.0.1:5000 127.0.0.1:6001 &
    ./rsse-indexer  127.0.0.1:5000 127.0.0.1:6002 &
    
    ./rsse-crawler  127.0.0.1:5000 twitter-user-name password
    
    ./rrse-searcher 127.0.0.1:5000 keyword

