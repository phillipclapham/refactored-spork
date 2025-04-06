# Open Questions

## Technical Questions

1. **API Selection**
   - Which AI providers should we use for each role?
   - Should we use the same provider for all AIs or mix providers?
   - What are the cost implications of different choices?

2. **Performance Concerns**
   - How to handle potential API latency?
   - Should we implement concurrent API requests?
   - How to maintain responsiveness with multiple sequential AI responses?

3. **Context Management**
   - What's the optimal way to manage context windows for each AI?
   - How much history should be included for each participant?
   - Should different context strategies be used for regular AIs vs. moderator?

## Design Questions

1. **AI Personalities**
   - How distinct should each AI's personality be?
   - Should personalities be configurable or hard-coded?
   - What traits make for engaging conversation?

2. **Moderator Behavior**
   - How active should the moderator be?
   - What triggers moderator intervention?
   - How to balance human control vs. autonomous moderation?

3. **User Experience**
   - What commands should be available to the human?
   - How to make the "whisper" functionality intuitive?
   - Should there be a way to adjust conversation parameters mid-session?