# Awesome AI Camera App



**Curated List of Commercial Apps & Open-Source Projects**

*Focused on Computational Photography, AI Enhancement, LUT Color Grading & Manual Controls*

**Last updated: October 2026**



This repository tracks notable **commercial AI camera apps** and **open-source projects** that bring computational photography, AI-driven enhancement, and professional-grade controls to mobile devices.



**Examples** include Microsoft Pix, Google Camera, Lensa AI, Prisma, Halide, Focos, Spectre Camera, VSCO, Camera+, and ProCam (the category leaders).



**Open-source emphasis**: The AI camera app space is **dominated by proprietary apps**, but a **growing open-source ecosystem** is emerging—particularly on Android. **Photon Camera** (Apache-2.0) is the standout, providing advanced LUT support, motion photos, AI-driven bokeh, and multi-frame synthesis . **LutinLens** (Sky Hackathon 2025) combines AI composition suggestions with GPU-accelerated LUT rendering . **Open Camera** remains the classic open-source Android camera with manual controls . **Camataca** offers granular control over every camera parameter Android exposes . For **Linux webcam effects**, **OpenEffects** and **webcam-filters** bring portrait blur and background replacement to any PipeWire-compatible app . This section documents these production-grade solutions.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [Commercial Apps](#commercial-apps)

- [Open-Source Projects](#open-source-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Commercial Apps



- **[Halide](https://halide.cam/)**  

  **High-end manual camera app for iPhone.** Provides gesture-based exposure and focus control, focus peaking, detailed histogram, adaptive level grid, and RAW support. The gold standard for iPhone manual photography .



- **[Google Camera](https://play.google.com/store/apps/details?id=com.google.android.GoogleCamera)**  

  **Google's flagship camera app with computational photography.** Features HDR+, Night Sight, Portrait Mode, and Astrophotography. Pixel-exclusive features leverage Google's ML models for best-in-class image quality.



- **[Lensa AI](https://prisma-ai.com/lensa)**  

  **AI photo editor with Magic Avatars.** Upload selfies and generate avatars in multiple artistic styles (comic, watercolor, cyberpunk, etc.). Popularized AI avatar generation on mobile .



- **[Prisma](https://prisma-ai.com/)**  

  **AI art filter app.** Applies artistic styles to photos using neural style transfer. One of the earliest mainstream AI photo apps.



- **[Focos](https://focos.app/)**  

  **Depth-based bokeh and portrait effects for iPhone.** Uses depth data from dual-camera iPhones to simulate large-aperture bokeh with adjustable focus points.



- **[Spectre Camera](https://spectre.cam/)**  

  **AI-powered long exposure for iPhone.** Uses computational photography to capture light trails and motion blur without a tripod.



- **[VSCO](https://vsco.co/)**  

  **Photo editing and community app with film-inspired presets.** Known for its distinctive color grading and LUT-style filters.



- **[Camera+](https://camera.plus/)**  

  **Feature-rich iPhone camera replacement.** Provides manual controls, multiple shooting modes, and advanced editing tools .



- **[ProCam](https://procamapp.com/)**  

  **Professional camera app for iPhone.** Offers manual controls, RAW capture, and advanced shooting modes.



## Open-Source Projects



### Android Camera Apps with AI



- **[Photon Camera](https://github.com/bjzhou/PhotonCamera)**  

  **The most advanced open-source Android camera app for static photography.** **Apache-2.0 licensed** . **Key features**: **Full LUT support** (`.cube`, `.png`, `.xmp`) with real-time preview ; **Motion Photos** with multi-vendor adaptation (Xiaomi, Samsung, Pixel)—the only open-source project to do so ; **AI-driven bokeh** using **midas-v2** depth detection optimized for Qualcomm chips ; **Multi-frame synthesis** for noise reduction and super-resolution ; **Phantom Mode** bypasses third-party camera API limitations by using the system camera with LUT processing ; **AI Color Simulation** using Google Nano Banana 2 to extract color profiles from reference photos . **Tech stack**: Jetpack Compose, Camera2 API, Android 11+ . **Best for**: Android photographers wanting mirrorless-like control and AI-enhanced quality.



- **[LutinLens](https://github.com/m0cal/LutinLens)**  

  **AI-powered smart camera app from Sky Hackathon 2025.** Built on **LibreCamera** with **Flutter** frontend . **Key features**: **NVIDIA NeMo Agent Toolkit + MCP protocol** for real-time AI composition analysis and LUT recommendations ; **GPU-accelerated LUT rendering** via GLSL (YUV to ARGB conversion with trilinear interpolation) achieving ~30 FPS on Snapdragon 8 Gen 2 ; scene recognition, composition suggestions, and real-time feedback (green checkmark for optimal timing) . **Tech stack**: Flutter 3.16+, Dart 3.2+, GLSL shaders, NVIDIA NeMo, Qwen LLM, Alibaba Cloud . **Best for**: Android users wanting AI-assisted composition with professional LUT grading.



- **[Open Camera](https://opencamera.org.uk/)**  

  **The classic open-source Android camera app.** Free, no ads, no in-app purchases . **Key features**: Auto-stabilization, manual controls (exposure, focus, ISO), HDR, focus modes, time-lapse, customizable resolution and file format . **Tradeoffs**: Complex interface for new users; limited post-processing . **Best for**: Android users wanting a free, feature-rich camera with manual controls and community-driven development.



- **[Camataca](https://github.com/Particlo/camataca)**  

  **Android camera app that exposes nearly every camera parameter.** **Key features**: Shows all cameras and microphones; supports **HDR, RAW, JPG, PNG, WebP, DNG, AVIF, JXL**; displays all available video/audio encoders (H.264, H.265, VP8/9, AV1); supports **BT2020, Display P3, scRGB, 8/10/16-bit, linear, HLG, PQ**; adjustable resolution, exposure, focus, white balance, sensitivity, FPS, color correction, flash, tonemap, effects . **Tradeoffs**: 1 MB base app (45 MB with AVIF/JXL codecs); requires APK sideload . **Best for**: Power users wanting maximum control over Android camera hardware.



### Linux Webcam Effects



- **[OpenEffects](https://github.com/funinkina/openeffects)**  

  **Linux-native webcam effects engine powered by ONNX Runtime.** **Key features**: **Portrait Mode** (AI background blur with feathered edges), **Center Stage** (intelligent face/body tracking for auto-cropping), **Background Replacement** (solid color or custom image), **Studio Light** (face-region-aware tone mapping), **Reactions** (hand-gesture-triggered overlays) . Works with **any PipeWire camera node**—Zoom, OBS, WebRTC, etc. . **Architecture**: `openeffectsd` (headless GStreamer daemon), `openeffects` (GTK4 GUI), `openeffectsctl` (CLI for scripting) . **ML inference runs on CPU** (2-5 ms per frame on modern x86_64) . **Best for**: Linux users wanting AI webcam effects without cloud dependency.



- **[webcam-filters](https://github.com/jashandeep-sohi/webcam-filters)**  

  **Add filters (background blur, etc.) to your webcam on Linux.** **540 GitHub stars** . Python-based. **Best for**: Simple background blur on Linux without a full effects engine.



### Image Enhancement & AI Toolkit



- **[SnapOtter-Vespera](https://github.com/Marcus-torchline/SnapOtter-Vespera)**  

  **Comprehensive open-source image toolkit with 50+ tools.** **AGPLv3 / Commercial dual-license** . **Key features**: **Local AI**—background removal, upscaling, photo restoration and colorization, object erasure, face blur/enhance, OCR, canvas expansion ; **Image editor** with layers, brushes, curves, filters ; **Pipelines** for chaining tools into reusable workflows ; **REST API** for every tool ; supports 55+ input formats including 23 RAW formats . **Deployment**: Single Docker container, no external services . **Best for**: Teams wanting a self-hosted, privacy-first alternative to cloud image services.



- **[local-upscaler](https://pypi.org/project/local-upscaler/)**  

  **Offline image and video upscaler with additional AI tools.** **Key features**: Image/video upscaling (2x, 4x, 60fps interpolation) ; **Colorize (DDColor)** and **Inpaint/object removal (LaMa)** tabs ; **Non-AI adjustments**—exposure, contrast, highlights/shadows, temperature, tint, vibrance, saturation, B&W conversion ; **Recipes** for batch processing with saved edit chains ; **PDF tools** (build/extract) . **Best for**: Users wanting local AI upscaling and restoration without cloud services.



### AI Avatar Generation



- **[302 Avatar Maker](https://github.com/302ai/302_avatar_maker)**  

  **Open-source AI avatar creation from selfies.** **Key features**: 17+ preset artistic styles (comic, watercolor, cyberpunk, steampunk, etc.); custom style descriptions; multiple output sizes (960×1280, 1024×1024, 1280×960) . **Tech stack**: Next.js 14, Tailwind CSS, Shadcn UI . **Deployment**: Docker . **Best for**: Creating unique social media avatars and artistic portraits.



- **[Enliven](https://huggingface.co/spaces/Coconut626/lyvo-photo-to-videoAi)**  

  **Open-source AI avatar animation with real expression transfer.** **MIT/Apache-2.0 licensed** . **Key features**: Transfers real human expressions and head movements from a driving video onto a static avatar photo; uses **LivePortrait** for expression/pose transfer and optional **GFPGAN** for face enhancement ; natural head rotation, nods, blinks . **Requirements**: Python 3.10+, 8GB RAM minimum, GPU recommended (CPU takes 13-20+ hours per 10-second video) . **Best for**: Creating expressive talking-head avatars from photos.



### Additional Strong Open-Source Options



- **Android AI Camera**: **Photon Camera** (Apache-2.0, LUTs, AI bokeh, motion photos), **LutinLens** (AI composition, GPU LUTs), **Open Camera** (classic, manual controls), **Camataca** (full parameter control) .

- **Linux Webcam**: **OpenEffects** (ONNX-based, portrait/background), **webcam-filters** (simple blur) .

- **Image Toolkit**: **SnapOtter-Vespera** (50+ tools, local AI), **local-upscaler** (upscaling, colorize, inpaint) .

- **AI Avatars**: **302 Avatar Maker** (17+ styles), **Enliven** (expression transfer) .



**Frameworks for building custom systems**: Combine **Photon Camera** for Android photography with LUTs and AI bokeh, **OpenEffects** for Linux webcam effects, **SnapOtter-Vespera** for comprehensive local image processing, and **302 Avatar Maker** or **Enliven** for AI avatar generation. Add **ONNX Runtime** for on-device ML inference and **FFmpeg** for video processing.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's commercial or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- AI camera apps handle photos and potentially biometric data (selfies, faces); ensure compliance with privacy regulations and obtain proper consent for face processing.

- **Open-source reality**: The open-source ecosystem for AI camera apps is **developing but production-capable** on **Android** (**Photon Camera**, **Open Camera**, **Camataca**) and **Linux** (**OpenEffects**, **webcam-filters**) . **Photon Camera** provides the most advanced feature set—LUTs, motion photos, AI bokeh, multi-frame synthesis—and is actively maintained . **OpenEffects** brings AI webcam effects to any Linux app . **SnapOtter-Vespera** offers a comprehensive self-hosted image toolkit . However, **commercial apps** (Halide, Google Camera, Lensa) still lead in **computational photography quality** and **AI model sophistication**, particularly for iPhone . The open-source path is **genuinely viable** for Android users and privacy-conscious Linux users seeking full control over their photography workflow.



---



**Made for mobile photographers, Android power users, Linux enthusiasts, and AI image tool developers.**

Let's make AI camera apps more open, transparent, and privacy-respecting.
# Awesome-AI-Camera-App

Awesome AI Camera AppCurated List of Commercial Apps & Open-Source ProjectsFocused on Computational Photography, AI Enhancement, LUT Color Grading & Manual ControlsLast updated: October 2026This repository tracks notable commercial AI camera apps and open-source projects that bring computational photography, AI-driven enhancement, and professional-grade controls to mobile devices.Examples include Microsoft Pix, Google Camera, Lensa AI, Prisma, Halide, Focos, Spectre Camera, VSCO, Camera+, and ProCam (the category leaders).Open-source emphasis: The AI camera app space is dominated by proprietary apps, but a growing open-source ecosystem is emerging—particularly on Android. Photon Camera (Apache-2.0) is the standout, providing advanced LUT support, motion photos, AI-driven bokeh, and multi-frame synthesis . LutinLens (Sky Hackathon 2025) combines AI composition suggestions with GPU-accelerated LUT rendering . Open Camera remains the classic open-source Android camera with manual controls . Camataca offers granular control over every camera parameter Android exposes . For Linux webcam effects, OpenEffects and webcam-filters bring portrait blur and background replacement to any PipeWire-compatible app . This section documents these production-grade solutions.Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.Table of ContentsCommercial AppsOpen-Source ProjectsHow to ContributeDisclaimerCommercial AppsHalideHigh-end manual camera app for iPhone. Provides gesture-based exposure and focus control, focus peaking, detailed histogram, adaptive level grid, and RAW support. The gold standard for iPhone manual photography .Google CameraGoogle's flagship camera app with computational photography. Features HDR+, Night Sight, Portrait Mode, and Astrophotography. Pixel-exclusive features leverage Google's ML models for best-in-class image quality.Lensa AIAI photo editor with Magic Avatars. Upload selfies and generate avatars in multiple artistic styles (comic, watercolor, cyberpunk, etc.). Popularized AI avatar generation on mobile .PrismaAI art filter app. Applies artistic styles to photos using neural style transfer. One of the earliest mainstream AI photo apps.FocosDepth-based bokeh and portrait effects for iPhone. Uses depth data from dual-camera iPhones to simulate large-aperture bokeh with adjustable focus points.Spectre CameraAI-powered long exposure for iPhone. Uses computational photography to capture light trails and motion blur without a tripod.VSCOPhoto editing and community app with film-inspired presets. Known for its distinctive color grading and LUT-style filters.Camera+Feature-rich iPhone camera replacement. Provides manual controls, multiple shooting modes, and advanced editing tools .ProCamProfessional camera app for iPhone. Offers manual controls, RAW capture, and advanced shooting modes.Open-Source ProjectsAndroid Camera Apps with AIPhoton CameraThe most advanced open-source Android camera app for static photography. Apache-2.0 licensed . Key features: Full LUT support (.cube, .png, .xmp) with real-time preview ; Motion Photos with multi-vendor adaptation (Xiaomi, Samsung, Pixel)—the only open-source project to do so ; AI-driven bokeh using midas-v2 depth detection optimized for Qualcomm chips ; Multi-frame synthesis for noise reduction and super-resolution ; Phantom Mode bypasses third-party camera API limitations by using the system camera with LUT processing ; AI Color Simulation using Google Nano Banana 2 to extract color profiles from reference photos . Tech stack: Jetpack Compose, Camera2 API, Android 11+ . Best for: Android photographers wanting mirrorless-like control and AI-enhanced quality.LutinLensAI-powered smart camera app from Sky Hackathon 2025. Built on LibreCamera with Flutter frontend . Key features: NVIDIA NeMo Agent Toolkit + MCP protocol for real-time AI composition analysis and LUT recommendations ; GPU-accelerated LUT rendering via GLSL (YUV to ARGB conversion with trilinear interpolation) achieving ~30 FPS on Snapdragon 8 Gen 2 ; scene recognition, composition suggestions, and real-time feedback (green checkmark for optimal timing) . Tech stack: Flutter 3.16+, Dart 3.2+, GLSL shaders, NVIDIA NeMo, Qwen LLM, Alibaba Cloud . Best for: Android users wanting AI-assisted composition with professional LUT grading.Open CameraThe classic open-source Android camera app. Free, no ads, no in-app purchases . Key features: Auto-stabilization, manual controls (exposure, focus, ISO), HDR, focus modes, time-lapse, customizable resolution and file format . Tradeoffs: Complex interface for new users; limited post-processing . Best for: Android users wanting a free, feature-rich camera with manual controls and community-driven development.CamatacaAndroid camera app that exposes nearly every camera parameter. Key features: Shows all cameras and microphones; supports HDR, RAW, JPG, PNG, WebP, DNG, AVIF, JXL; displays all available video/audio encoders (H.264, H.265, VP8/9, AV1); supports BT2020, Display P3, scRGB, 8/10/16-bit, linear, HLG, PQ; adjustable resolution, exposure, focus, white balance, sensitivity, FPS, color correction, flash, tonemap, effects . Tradeoffs: 1 MB base app (45 MB with AVIF/JXL codecs); requires APK sideload . Best for: Power users wanting maximum control over Android camera hardware.Linux Webcam EffectsOpenEffectsLinux-native webcam effects engine powered by ONNX Runtime. Key features: Portrait Mode (AI background blur with feathered edges), Center Stage (intelligent face/body tracking for auto-cropping), Background Replacement (solid color or custom image), Studio Light (face-region-aware tone mapping), Reactions (hand-gesture-triggered overlays) . Works with any PipeWire camera node—Zoom, OBS, WebRTC, etc. . Architecture: openeffectsd (headless GStreamer daemon), openeffects (GTK4 GUI), openeffectsctl (CLI for scripting) . ML inference runs on CPU (2-5 ms per frame on modern x86_64) . Best for: Linux users wanting AI webcam effects without cloud dependency.webcam-filtersAdd filters (background blur, etc.) to your webcam on Linux. 540 GitHub stars . Python-based. Best for: Simple background blur on Linux without a full effects engine.Image Enhancement & AI ToolkitSnapOtter-VesperaComprehensive open-source image toolkit with 50+ tools. AGPLv3 / Commercial dual-license . Key features: Local AI—background removal, upscaling, photo restoration and colorization, object erasure, face blur/enhance, OCR, canvas expansion ; Image editor with layers, brushes, curves, filters ; Pipelines for chaining tools into reusable workflows ; REST API for every tool ; supports 55+ input formats including 23 RAW formats . Deployment: Single Docker container, no external services . Best for: Teams wanting a self-hosted, privacy-first alternative to cloud image services.local-upscalerOffline image and video upscaler with additional AI tools. Key features: Image/video upscaling (2x, 4x, 60fps interpolation) ; Colorize (DDColor) and Inpaint/object removal (LaMa) tabs ; Non-AI adjustments—exposure, contrast, highlights/shadows, temperature, tint, vibrance, saturation, B&W conversion ; Recipes for batch processing with saved edit chains ; PDF tools (build/extract) . Best for: Users wanting local AI upscaling and restoration without cloud services.AI Avatar Generation302 Avatar MakerOpen-source AI avatar creation from selfies. Key features: 17+ preset artistic styles (comic, watercolor, cyberpunk, steampunk, etc.); custom style descriptions; multiple output sizes (960×1280, 1024×1024, 1280×960) . Tech stack: Next.js 14, Tailwind CSS, Shadcn UI . Deployment: Docker . Best for: Creating unique social media avatars and artistic portraits.EnlivenOpen-source AI avatar animation with real expression transfer. MIT/Apache-2.0 licensed . Key features: Transfers real human expressions and head movements from a driving video onto a static avatar photo; uses LivePortrait for expression/pose transfer and optional GFPGAN for face enhancement ; natural head rotation, nods, blinks . Requirements: Python 3.10+, 8GB RAM minimum, GPU recommended (CPU takes 13-20+ hours per 10-second video) . Best for: Creating expressive talking-head avatars from photos.Additional Strong Open-Source OptionsAndroid AI Camera: Photon Camera (Apache-2.0, LUTs, AI bokeh, motion photos), LutinLens (AI composition, GPU LUTs), Open Camera (classic, manual controls), Camataca (full parameter control) .Linux Webcam: OpenEffects (ONNX-based, portrait/background), webcam-filters (simple blur) .Image Toolkit: SnapOtter-Vespera (50+ tools, local AI), local-upscaler (upscaling, colorize, inpaint) .AI Avatars: 302 Avatar Maker (17+ styles), Enliven (expression transfer) .Frameworks for building custom systems: Combine Photon Camera for Android photography with LUTs and AI bokeh, OpenEffects for Linux webcam effects, SnapOtter-Vespera for comprehensive local image processing, and 302 Avatar Maker or Enliven for AI avatar generation. Add ONNX Runtime for on-device ML inference and FFmpeg for video processing.How to ContributeFork the repo.Add/edit entries in README.md (follow existing format).Include: name, link, 1–2 sentence description, and whether it's commercial or open-source.Submit PR with a short explanation.Star the repo if you find it useful!DisclaimerThis is a community-curated list — not exhaustive and not an endorsement.AI camera apps handle photos and potentially biometric data (selfies, faces); ensure compliance with privacy regulations and obtain proper consent for face processing.Open-source reality: The open-source ecosystem for AI camera apps is developing but production-capable on Android (Photon Camera, Open Camera, Camataca) and Linux (OpenEffects, webcam-filters) . Photon Camera provides the most advanced feature set—LUTs, motion photos, AI bokeh, multi-frame synthesis—and is actively maintained . OpenEffects brings AI webcam effects to any Linux app . SnapOtter-Vespera offers a comprehensive self-hosted image toolkit . However, commercial apps (Halide, Google Camera, Lensa) still lead in computational photography quality and AI model sophistication, particularly for iPhone . The open-source path is genuinely viable for Android users and privacy-conscious Linux users seeking full control over their photography workflow.Made for mobile photographers, Android power users, Linux enthusiasts, and AI image tool developers.Let's make AI camera apps more open, transparent, and privacy-respecting.
