# Gen Vision 🎃 - Multimodal Chatbot with Text, Image, and Video Processing


Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference

| Option                               | Repository URL                                       | File Name                                      | Alias        |
|--------------------------------------|------------------------------------------------------|------------------------------------------------|--------------|
| Realism (face/character) 👦🏻          | `prithivMLmods/Canopus-Realism-LoRA`                 | `Canopus-Realism-LoRA.safetensors`             | `rlms`       |
| Pixar (art/toons) 🙀                 | `prithivMLmods/Canopus-Pixar-Art`                    | `Canopus-Pixar-Art.safetensors`                | `pixar`      |
| Photoshoot (camera/film) 📸          | `prithivMLmods/Canopus-Photo-Shoot-Mini-LoRA`        | `Canopus-Photo-Shoot-Mini-LoRA.safetensors`    | `photo`      |
| Clothing (hoodies/pants/shirts) 👔   | `prithivMLmods/Canopus-Clothing-Adp-LoRA`            | `Canopus-Dress-Clothing-LoRA.safetensors`      | `clth`       |
| Interior Architecture (house/hotel) 🏠 | `prithivMLmods/Canopus-Interior-Architecture-0.1`    | `Canopus-Interior-Architecture-0.1δ.safetensors` | `arch`       |
| Fashion Product (wearing/usable) 👜  | `prithivMLmods/Canopus-Fashion-Product-Dilation`     | `Canopus-Fashion-Product-Dilation.safetensors` | `fashion`    |
| Minimalistic Image (minimal/detailed) 🏞️ | `prithivMLmods/Pegasi-Minimalist-Image-Style`        | `Pegasi-Minimalist-Image-Style.safetensors`    | `minimalist` |
| Modern Clothing (trend/new) 👕       | `prithivMLmods/Canopus-Modern-Clothing-Design`       | `Canopus-Modern-Clothing-Design.safetensors`   | `mdrnclth`   |
| Animaliea (farm/wild) 🫎             | `prithivMLmods/Canopus-Animaliea-Artism`             | `Canopus-Animaliea-Artism.safetensors`         | `Animaliea`  |
| Liquid Wallpaper (minimal/illustration) 🖼️ | `prithivMLmods/Canopus-Liquid-Wallpaper-Art`         | `Canopus-Liquid-Wallpaper-Minimalize-LoRA.safetensors` | `liquid`     |
| Canes Cars (realistic/future cars) 🚘 | `prithivMLmods/Canes-Cars-Model-LoRA`                | `Canes-Cars-Model-LoRA.safetensors`            | `car`        |
| Pencil Art (characteristic/creative) ✏️ | `prithivMLmods/Canopus-Pencil-Art-LoRA`               | `Canopus-Pencil-Art-LoRA.safetensors`          | `Pencil Art` |
| Art Minimalistic (paint/semireal) 🎨 | `prithivMLmods/Canopus-Art-Medium-LoRA`              | `Canopus-Art-Medium-LoRA.safetensors`          | `mdm`        |

**Gen Vision** is a powerful multimodal chatbot that integrates text generation, image generation, and text-to-speech (TTS) capabilities. It leverages state-of-the-art models like **FastThink**, **Qwen2VL**, and **Stable Diffusion XL** to provide a seamless experience for users. The chatbot supports various art styles for image generation, text-to-speech functionality, and multimodal input processing.

---

## Features

1. **Text Generation**:
   - Powered by the `FastThink-0.5B-Tiny` model for efficient text generation.
   - Supports conversational history and context-aware responses.

2. **Image Generation**:
   - Uses **Stable Diffusion XL** with **LoRA (Low-Rank Adaptation)** for high-quality image generation.
   - Supports multiple art styles, including Realism, Pixar, Photoshoot, Clothing, Interior, Fashion, Minimalistic, Modern, Animaliea, Wallpaper, Cars, Pencil Art, and Art Minimalistic.

3. **Text-to-Speech (TTS)**:
   - Supports two TTS voices (`en-US-JennyNeural` and `en-US-GuyNeural`).
   - Converts generated text into speech for an interactive experience.

4. **Multimodal Input**:
   - Accepts text and images as input.
   - Processes multimodal inputs seamlessly using **Qwen2VL**.

5. **Gradio Interface**:
   - Provides an intuitive and interactive web interface for users.
   - Supports queuing, progress tracking, and example-based interactions.

---

## Installation

To set up the project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/Gen-Vision.git
   cd Gen-Vision
   ```

2. **Install Dependencies**:
   Ensure you have Python 3.8+ installed. Then, install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   Start the Gradio interface:
   ```bash
   python app.py
   ```
   The application will launch locally, and you can access it via the provided URL.

---

## Usage

### 1. **Text Generation**
   - Enter text in the input box and press `Enter`.
   - The chatbot will generate a response based on the input.

### 2. **Image Generation**
   - Use the `@<lora_command>` tag followed by a prompt to generate images in specific styles.
   - Example: `@realism A futuristic cityscape with neon lights`.

### 3. **Text-to-Speech (TTS)**
   - Use the `@tts1` or `@tts2` command followed by text to generate speech.
   - Example: `@tts1 Who is Nikola Tesla?`.

### 4. **Multimodal Input**
   - Upload images along with text queries for combined processing.
   - Example: `Summarize the letter` + upload an image.

---

## Examples

Here are some example inputs you can try:

1. **Text Generation**:
   - `Python Program for Array Rotation`

2. **Image Generation**:
   - `@realism Chocolate dripping from a donut against a yellow background`
   - `@pixar A young man with light brown wavy hair and light brown eyes sitting in an armchair`

3. **Text-to-Speech**:
   - `@tts2 What causes rainbows to form?`

4. **Multimodal Input**:
   - `Summarize the letter` + upload an image.

---

## Models Used

1. **FastThink-0.5B-Tiny**:
   - A lightweight text generation model for efficient conversational AI.

2. **Qwen2VL-OCR2-2B-Instruct**:
   - A multimodal model for text and image processing.

3. **Stable Diffusion XL**:
   - A state-of-the-art image generation model with LoRA support for various art styles.

4. **Edge TTS**:
   - A text-to-speech engine for generating speech from text.

---

## Configuration

You can customize the following parameters in the code:

- **LoRA Models**:
  - Add or modify LoRA models in the `LORA_OPTIONS` dictionary.
  - Example:
    ```python
    LORA_OPTIONS = {
        "Realism": ("prithivMLmods/Canopus-Realism-LoRA", "Canopus-Realism-LoRA.safetensors", "rlms"),
        "Pixar": ("prithivMLmods/Canopus-Pixar-Art", "Canopus-Pixar-Art.safetensors", "pixar"),
    }
    ```

- **Text Generation Parameters**:
  - Adjust `max_new_tokens`, `temperature`, `top_p`, `top_k`, and `repetition_penalty` in the `generate` function.
