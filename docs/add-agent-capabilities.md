---
title: Capabilities for Agents in Microsoft 365 Copilot
description: Learn about capabilities that you can add to your declarative agent and how to enable them.
author: lauragra
ms.author: lauragra
ms.topic: concept-article
ms.date: 11/15/2024
---

# Add capabilities to your declarative agent

You can enhance the user experience of your declarative agent by adding capabilities. The **capabilities** element in the manifest reference and the **Capabilities** section in the Copilot Studio agent builder provide several options for you to unlock features for your users. This article describes the user capabilities that you can add to your agents.

## Image generator

The image generator capability enables declarative agents to generate images based on user prompts. Image generator uses the existing [Designer](https://designer.microsoft.com/) functionality to create visually appealing and contextually relevant graphics, and includes the following features:

- **Multiple image generation**: For each user prompt, the agent generates four images.
- **Interactive image options**: Users can click on each generated image to view it in full size. They can download, copy, or view content credentials for the full-size image. They can also click the side arrow to scroll through the four images.
- **Image modification**: Users can follow up with subsequent prompts to modify the original images without losing context. For example, first prompt: "Create a photo of a happy puppy running around in a yard." Second prompt: "Include a tennis ball."
- **Feedback mechanism**: Users can provide feedback on the generated images by giving a thumbs up or thumbs down. This helps improve the quality of future image generations.
- **Clipboard and sharing**: Users can copy the generated images to their clipboard to paste into other applications, or they can share the generated images directly from the interface.
 
### Image generation examples

The following examples show what users can do with the image generation capability in your agent.

**User prompt**: Create an image of a serene beach at sunset with palm trees and gentle waves.

The following image shows the result.

:::image type="content" source="assets/images/image-gen-beach-prompt.png" alt-text="Beach image response to the user prompt":::

**User prompt**: Design a flyer for a summer music festival and add a date for May 15, 2024.

The following image shows the result.

:::image type="content" source="assets/images/image-gen-flier-prompt.png" alt-text="Festival flyer image response to the user prompt":::

### Enable image generator

If you're using [Teams Toolkit and Visual Studio Code](build-declarative-agents.yml) to create your agent, to enable image generator in your agent, add the `GraphicArt` value to the **capabilities** property in your manifest reference, as shown in the following example.

```json
{
  "capabilities": [
    {
      "name": "GraphicArt"
    }
  ]
}
```

If you're using [Copilot Studio agent builder](copilot-studio-agent-builder.md) to create your agent, on the **Configure** tab, under **Capabilities**, choose the toggle next to **Image generator**.

:::image type="content" source="assets/images/capabilities-toggle.png" alt-text="Screenshot of the Capabilities section of the agent builder":::

> [!NOTE]
> The image generator doesn't currently work in the test pane in Copilot Studio agent builder.

## Related content

- [Declarative agents overview](overview-declarative-agent.md)
- [Declarative agent manifest reference](declarative-agent-manifest.md)