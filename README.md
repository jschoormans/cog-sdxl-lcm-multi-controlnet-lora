# cog-sdxl-lcm-multi-controlnet-lora

https://replicate.com/fofr/sdxl-lcm-multi-controlnet-lora

[![Replicate demo and cloud API](https://replicate.com/fofr/sdxl-lcm-multi-controlnet-lora/badge)](https://replicate.com/fofr/sdxl-lcm-multi-controlnet-lora)

SDXL with:

- LCM lora for massive speed increase
- img2img
- inpainting
- custom Replicate lora loading
- up to 3 simultaneous controlnets with different images
  - canny
  - midas depth
  - leres depth
  - soft edge hed
  - soft edge pidi
  - openpose
  - QR Monster (illusions)
  - lineart
  - lineart anime
- img2img plus controlnet
- inpainting plus controlnet
- controlnet conditioning strengths
- controlnet start and end controls
- SDXL refiner
- Image resizing based on width/height, input image or a control image
- Disable safety checker via API

Based on https://github.com/fofr/cog-sdxl-multi-controlnet-lora


sudo cog predict -i controlnet_1=openpose 

sudo cog predict -i image=@brandon.png -i mask=@brandon-mask.png -i prompt="a bald man wearing a TOK sweater, in Milan, fashion photography, 4k photo" -i negative_prompt="low quality, bad quality, dress, unsharp, hair" -i controlnet_1="openpose" -i sizing_strategy="input_image" -i controlnet_1_image=@brandon.png -i lora_weights="https://pbxt.replicate.delivery/z3i4F3x0rwLDGV9JRQ1JvoNGqtBrwKlhWwI0BGghHIB9ySZE/trained_model.tar" 