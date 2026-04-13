The question or message to send to the AI. Can be:
- A string: Plain text question
- An array: Multipart content with text and binary data (images, PDFs, audio, etc.)
Array elements can be:
* String: Text content or file path (if path exists, file is read automatically)
* Binary: File content as binary
* Struct: Part object with content and metadata
Examples:
- Simple: "What is the capital of France?"
- Multipart: ["Analyze this image", imageBytes]
- With paths: ["Summarize this PDF", "/path/to/document.pdf"]
- Mixed: ["Compare these", image1Bytes, "/path/to/image2.jpg"]
- Struct: ["do you like these", {"contenttype":"audio/mpeg","path":"/path/to/music.mp3"}]
- Struct: ["do you like these", {"contenttype":"audio/mpeg","binary":bin,"metadata":metadata}]
The question becomes part of the conversation history and provides context for future interactions within the same session.