# 💬 Unity Dialogue System

This project is a simple yet functional **dialogue system** designed for Unity. It allows characters in your game to display conversations on screen with names, portraits, and animated text transitions. Players can advance the dialogue by pressing a key.

## 🎯 Features

- Shows actor name, portrait, and message
- Advance dialogue with the `E` key
- Automatically splits long messages into smaller parts
- Text fade-in animation
- Smooth open/close animations for the dialogue box
- Easily expandable with new characters and messages

## 🛠️ Setup

1. Clone or download this repository:
   ```bash
   git clone https://github.com/yourusername/Unity-Dialogue-System.git

Open your Unity project and add the files to the Assets/Scripts folder.

Create a UI Canvas in your scene and add the following UI elements:

Image → for actor portrait

TextMeshPro - Text → for actor name

TextMeshPro - Text → for dialogue message

Panel or RectTransform → for background box

Drag and drop the relevant UI references to the DialogueManager component in the Inspector.

Create a GameObject with the DialogueTrigger script and assign:

An array of messages (text + actor ID)

An array of actors (name + sprite)

▶️ How It Works
When DialogueTrigger.StartDialogue() is called, the DialogueManager opens the dialogue UI and shows the first message.

Press E to display the next message.

Once all messages have been shown, the dialogue UI closes.

🧩 Example Usage
csharp
Kopyala
Düzenle
public class DialogueStart : MonoBehaviour
{
    public DialogueTrigger trigger;

    private void OnTriggerEnter(Collider other)
    {
        if (other.CompareTag("Player"))
        {
            trigger.StartDialogue();
        }
    }
}
📌 Requirements
Unity 2021 or newer

TextMeshPro package (comes built-in)

LeanTween (for animations – optional but recommended)

🤝 Contributing
Pull requests and suggestions are welcome! For major changes, please open an issue first to discuss what you'd like to change.

📜 License
This project is licensed under the MIT License. Feel free to use, modify, and distribute it in your own projects.

🧠 Note: This is a basic system and can be extended into a more complex narrative system depending on your game’s needs.
