# AI Cultural Arts UnitedS
*** BYOM Readme *** 

This example demonstrates the optimization, deployment, and inference process of the BYOM (Bring Your Own Model) model. Three models are included:

1) GAN Model: This GAN model has been trained using images of famous painters to learn their painting styles. The training has been completed and a .ckpt (or .pt) file has been output.

2) Diffusion Model (W): This diffusion_word model has been trained using works of famous calligraphers (such as Wang Xizhi) to learn the diffusion generation of entire glyphs. The training has been completed and a .ckpt (or .pt) file has been output.

3) Diffusion Model (S): This diffusion_stroke model has been trained using works of famous calligraphers (such as Wang Xizhi) to learn the stroke order of each font. The training has been completed and a .ckpt (or .pt) file has been output.

Therefore, in this example, we provide three pre-trained models (*.pt format). In the code section, we provide code to convert these three .pt model files into standard onnx files. This demonstrates how to convert these pre-trained .pt models locally to standard onnxfiles, allowing you to clearly observe the format of the model's input and output data.

Next, we enter the crucial stage of "Compiling and Optimizing with AI Hub." Please utilize AI Hub's services to perform the key task: submit the three onnxfiles to AI Hub to generate Qnn_onnx format files (containing model.onnx and model.data or model.bin), storing them in the following three folders:

C:/ox_model_roro_gan/

C:/ox_model_roro_word/

C:/ox_model_roro_stroke/

 

 

After compiling, optimizing, and deploying (profiling) to achieve satisfactory performance, you can then run the EdgeAI app on a real machine to perform inference. This example provides two apps:

App_01: It first calls a GAN model (Qnn_onnxformat) to generate the calligraphy base (background), then calls a Diffusion_word model (Qnn_innx format) to write the entire Chinese character.

App_02: It first calls a GAN model (Qnn_onnxformat) to generate the calligraphy base (background), then calls a Diffusion_stroke model (Qnn_innx format) to write the Chinese character stroke by stroke.

 

~~ END ~~
