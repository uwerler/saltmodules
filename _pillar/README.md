### file_tree_ng.py

This module is an enhanced version of file_tree.py with the ability to create
hostgroups out if graines or pillars. For now I renamed it to file_tree_ng and
hope to submit it after more testing upstream.

Simply place the module unter salt/_pillar and configure it like file_tree in
master config with additionally adding grains or pillars which match later on
hostgroups:

```
        ext_pillar:
          - file_tree:
            root_dir: /path/to/root/directory
            pillar_name: some:pillar
            grains_name: 
              - some:grain
              - some:other:grain
```

Testers welcome!

