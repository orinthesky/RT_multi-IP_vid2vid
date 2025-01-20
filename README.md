# RT_multi-IP_vid2vid
A real time diffusion workflow for vid2vid style transfer using multiple image prompts

Created by FungAI - @orinthesky

This workflow allows for multiple image prompts to stylize a real time camera input.  This is achieved using a Canny ControlNet as well as saved embeddings of the image prompts.
The IPadapter Plus node pack is necessary for this. If you want to run this in ComfyStream, as of now there can only be one "load image" node input in the workflow, so all image prompts must be saved as embeddings and reloaded as such in the workflow.
I've encluded a worklfow called "IP_embedding_saver" which has everything turned off except a group ready to save your concatenated embeddings. Use this to save your embeds and then move the saved .ipadapter files to the /inputs folder in your ComfyUI folder so the "load IPadapter embeds" node can find them.
