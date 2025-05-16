# Automated X Posting Terminal
An automated posting workflow for X. Takes the most recent posts from select X channels using an RSS feed and utilizes multiple GPT-4o steps and advanced prompting rules to translate them into new posts relevant to your brand identity.

## About This Repository
This Automated Posting Terminal for X is primarily available for educational and portfolio purposes only. This documentation represents an implementation of a common business process tool. A deployment-ready version would require further iteration and testing. Please feel free to make those updates yourself, or for developmental inquiries regarding the interface, please contact edan@analyticintelligencesolutions.com.

# Technical Architecture
### RSS Feed
The terminal pulls a minimum of the 15 most recent posts from each X channel RSS feed. It has a minimum of 5 X channel RSS feeds to choose from. These should have a good amount of overlap, and your brand identity should be clearly and directly defined for best results.

### RSS Feed Translation
The RSS feed should be parsed and aggregated. An AI step should be added with a similar developer/system prompt: "You are a viral post extractor. You will receive a  posts from a source on X, and your job is to output that post only. Output ONLY the text content, no links, quotes, or unrelated elements. Output in JSON format. Do not wrap your output in any other text, not even backticks." The AI is expected to respond with a JSON output.

### Topic Selection
To make the overall post feed more natural, it would be wise to add a middle step with relevent post topics defined by a human. This should have at least 40-50 topics to rotate through for best results. A randomizer should select one topic from the list every time to use as the main post content. For my implementation, I add an idea every time I have one for a post I can't write immediately. Since it is mixing the topic with a source post, using the same topic twice will not produce a negative or repetitve effect.

### X Post Creator
An AI step should be added with a similar developer/system prompt: "You are to take an input post from a twitter source account, and repurpose it to highlight the one proposed AI chatbot solution, for high quality engaging posts on X (formerly Twitter). Take the input post and merge it with the recommended AI chatbot benefit. Choose to either mirror the input post's exact sentence structure while swapping in the selected AI benefit, or counter the input post's pain point by showing how AI solves it. Prioritize following the meme format of the input post while ensuring the new post flows naturally and makes logical sense. Use the same amount of emojis as the original input post. Only output lowercase letters." Make sure you provide the AI step with both the input post and the post topic. This is specific to one specialized industry use case and should be adapted accordingly. At some point, we will probably be able to remove 'formerly Twitter'.

### Post Additions
The post pipeline can end here, and two branching pathways are recommended so it does end here, sometimes, to add to the natural randomization factor of your X feed. For the ones that continue, adding a generated image is a viable next step. For best results, an AI prompt similar to this one is recommended: "You are to take two Twitter posts and generate a simple image prompt. Your output should be one clear, descriptive sentence focused on a single main object or scene. Create a photorealistic, memorable visual that captures the post's essence without using text or human figures. The image should feel natural and polished, not AI-generated. Output only the prompt with no additional text." With that in mind, you should provide both the intial source post and your generated post for content reference. There are several kinds of paid follow up AI image improvement API steps you can add to improve the final post content.

The more branching flow types you add, the more natural your X feed will feel. You can do multiple kinds of content flows, different post lengths and structures, AI generated videos, and randomized link additions. The more specific you are with your process steps, the better your end result will be.

## Development and Legal
To actually test the tool, reach out to edan@analyticintelligencesolutions,com. Feel free to inquire further as to how it works, use it as inspiration, or adapt elements for your own projects. As with any code sample, it's always best to understand the concepts and implement your own solution rather than using it directly in production. If you're inspired by this approach, I encourage you to develop your own unique solution with much needed modifications to both design and implementation.
