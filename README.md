![output](https://github.com/user-attachments/assets/1c47fd97-a96b-40d9-9b40-f06105db5a47)
<!-- 

check ffmpg

AE render Quick Time, RGB-Alpha save --- video.mov

# step 1 — generate palette (better colours, smaller file)
ffmpeg -i "video.mov" -vf "fps=15,scale=480:-1:flags=lanczos,palettegen" palette.png

# step 2 — create gif using palette, and ask the GIF to loop forever
ffmpeg -i "video.mov" -i palette.png -filter_complex "fps=15,scale=480:-1:flags=lanczos[x];[x][1:v]paletteuse" -loop 0 output.gif


-->
