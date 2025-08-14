# watchetawan
watchetawan.org

ffmpeg -i source.mov -an -vf "scale=1280:-1,fps=24" \
  -c:v libx264 -preset veryfast -crf 23 -profile:v high -pix_fmt yuv420p \
  -tune fastdecode \
  -g 12 -keyint_min 12 -sc_threshold 0 \
  -movflags +faststart \
  output.mp4

  ffmpeg -i source.mov -an -vf "scale=1280:-1,fps=24" \
  -c:v libvpx-vp9 -crf 32 -b:v 0 -row-mt 1 \
  -g 12 -movflags +faststart \
  output.webm

  ffmpeg -i source.mov -an -vf "scale=1280:-1,fps=24" \
  -c:v libx264 -preset veryfast -crf 23 -profile:v high -pix_fmt yuv420p \
  -tune fastdecode -g 8 -keyint_min 8 -sc_threshold 0 \
  -movflags +faststart output.mp4

