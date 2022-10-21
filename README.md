# PortSIP integration

## Steps to reproduce error:

1. Put framework in directory at path `third-party/PortSIP/Frameworks/`
2. Run `generate_project.sh` shell script to generate .xcodeproj
3. Run application on any simulator

## Info

PortSIP framework includes symbols for webrtc, libyuv, boringssl those conflicts with same libraries placed in `third-party/` directory
