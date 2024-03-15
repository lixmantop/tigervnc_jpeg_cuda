# **Introducing Tiger VNC + jpeg + CUDA(NVIDIA)**

## Validate the suitability of the solution :)
 + Outsource Jpeg encoding from VNC
 + Reduce encoding load at CPU level
 + GPU level encoding (Opencl/CUDA)
 + No adhesion/dependency between TigerVnc <=> CUDA encoding


## Installing/Testing TigerVNC

 + Clone the TigerVnc project (https://github.com/TigerVNC/tigervnc.git)
 + Patching in tigervnc/common/rfb with JpegCompressor.cxx and JpegCompressor.h
 + Compiling/installing Xvnc
 + Installing/compiling nvJPEG

## Testing

+ launch nvJPEG (https://github.com/lixmantop/nvJPEG.git)
+ start the tigervn server (systemctl start vncserver@:1 or vncserver)


## Plan:

-------------        -------------------------------          ----------
  Tigervnc     <==>  socket = /tmp/vnc_jpeg_cuda    <==>    nvJPEG 
 -------------        -------------------------------          ----------
