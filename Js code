import { useState } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";

export default function MessageGenerator() {
  const [prompt, setPrompt] = useState("");
  const [message, setMessage] = useState("");

  const generateMessage = () => {
    // Simple predefined generator
    if (prompt.toLowerCase().includes("diwali")) {
      setMessage("Hello {name}, Diwali greetings! We wish you the best holiday. Namaste!");
    } else if (prompt.toLowerCase().includes("new year")) {
      setMessage("Hello {name}, Wishing you a Happy New Year! May this year bring joy and success.");
    } else {
      setMessage(`Hello {name}, ${prompt} ✨`);
    }
  };

  return (
    <div className="p-6 max-w-lg mx-auto">
      <Card className="shadow-lg rounded-2xl">
        <CardContent className="space-y-4">
          <h2 className="text-xl font-bold">Message Generator</h2>

          {/* Prompt Input */}
          <Input
            placeholder="Enter your prompt (e.g., Diwali wish)"
            value={prompt}
            onChange={(e) => setPrompt(e.target.value)}
          />

          <Button onClick={generateMessage}>Generate Message</Button>

          {/* Generated Message */}
          {message && (
            <Textarea
              className="mt-4"
              value={message}
              onChange={(e) => setMessage(e.target.value)}
            />
          )}
        </CardContent>
      </Card>
    </div>
  );
}
