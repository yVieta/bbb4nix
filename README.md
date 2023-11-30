# BBB4Nix

## Contribution to Nix Community Packages
This Modul will be contributed to the [official nixpkgs](https://github.com/NixOS/nixpkgs) when it gets rewritten and finished. 

## Extras
That includes [packages](packages/README.md) and [modules](modules/README.md) for all relevant components.

## Todos
- Rewriting the modules for
- Testing on "standalone"

### Comments from Helsinki
#### Notes
We deploy this together with our deployment/configuration management/whatever project.
Some stub modules are included for compatibility, but we don't test this

##### Known issues from Helsinki 
When not using helsinki, you need to enable AES256-GCM-SHA384 or another cipher compatible with node.js 8.x (used by bbb html5) in your nginx.
Also some ports need to be opened for WebRTC etc.

Recording and Playback does not work. This is due to the fact that it is:
1) most likely not GDPR compliant (https://docs.bigbluebutton.org/admin/privacy.html)
2) implemented very interestingly (there is a branch which mostly gets it working, look at that to see what I mean)
3) will work differently in bbb 2.3
