# Voice Capture Integration Guide

How to capture thoughts by voice and route them into your Personal Stack.

---

## Why Voice Capture?

- Capture ideas while walking, driving, commuting
- Faster than typing for brain dumps
- Lower friction means more capture
- Good for processing thoughts out loud

**The goal**: Voice → Text → Inbox → Processed into system

---

## The Voice Capture Workflow

```
[Speak into device]
        ↓
[Transcription service]
        ↓
[Text file or note]
        ↓
[Into 00_Inbox/]
        ↓
[Process within 48h]
```

You have options at each stage. Pick what fits your setup.

---

## Option 1: Apple Dictation (Simplest)

**Works on**: Mac, iPhone, iPad
**Cost**: Free
**Quality**: Good for short captures

### Setup
1. Enable: System Settings → Keyboard → Dictation → On
2. Set shortcut (default: press Fn twice)

### Workflow
1. Open Obsidian, create new note in `00_Inbox/`
2. Press Fn twice, speak
3. Dictation appears as text
4. Save and process later

### Pros/Cons
- ✅ No extra apps, built-in
- ✅ Works offline (on-device)
- ❌ No automatic file creation
- ❌ Must have Obsidian open

---

## Option 2: Whisper (Best Quality)

**Works on**: Any device (via API or local)
**Cost**: Free (local) or API costs
**Quality**: Excellent, handles accents well

### Option 2A: Whisper via MacWhisper (Mac)

1. Download [MacWhisper](https://goodsnooze.gumroad.com/l/macwhisper)
2. Record or import audio
3. Transcribe locally
4. Copy text to Inbox

### Option 2B: Whisper via API

For automated pipelines:

```python
import openai

audio_file = open("recording.m4a", "rb")
transcript = openai.Audio.transcribe("whisper-1", audio_file)
print(transcript["text"])
```

### Option 2C: Whisper Local (Free, Private)

```bash
# Install
pip install openai-whisper

# Transcribe
whisper recording.m4a --model base --output_format txt
```

### Pros/Cons
- ✅ Best accuracy
- ✅ Handles long recordings
- ✅ Can be fully local/private
- ❌ Requires extra step to get into vault

---

## Option 3: Voice Memos + Automation (iPhone)

**Works on**: iPhone
**Cost**: Free (with Shortcuts)
**Quality**: Good

### Setup
1. Record with Voice Memos app
2. Create Shortcut to transcribe and save

### Basic Shortcut
1. Open Shortcuts app
2. Create new shortcut:
   - Get latest Voice Memo
   - Transcribe audio
   - Save to Files (your vault's Inbox folder)

### Pros/Cons
- ✅ Native apps, reliable
- ✅ Can automate
- ❌ Requires iCloud sync to vault
- ❌ Shortcut setup takes time

---

## Option 4: Otter.ai (Best for Meetings)

**Works on**: Web, iOS, Android
**Cost**: Free tier available, paid for more
**Quality**: Excellent, especially for conversations

### Setup
1. Sign up at otter.ai
2. Install mobile app
3. Record conversations or upload audio

### Getting into Vault
- Export transcript as text
- Copy to `00_Inbox/`
- Or use Otter's integrations (Zapier, etc.)

### Pros/Cons
- ✅ Great for meetings, multiple speakers
- ✅ Auto-identifies speakers
- ✅ Searchable archive
- ❌ Cloud-based (privacy consideration)
- ❌ Manual export to vault

---

## Option 5: Drafts App (iOS/Mac)

**Works on**: iOS, Mac
**Cost**: Free (basic), $30/year (pro)
**Quality**: Uses Apple dictation

### Setup
1. Install Drafts app
2. Speak into Drafts (uses system dictation)
3. Create action to export to Obsidian vault

### Export Action
Drafts can send text directly to a file:
- Create Action: "Send to Inbox"
- Action: Append to file at `/path/to/vault/00_Inbox/Voice-Captures.md`

### Pros/Cons
- ✅ Fast capture, always ready
- ✅ Good action system for routing
- ✅ Syncs across Apple devices
- ❌ Apple ecosystem only
- ❌ Pro features require subscription

---

## Option 6: Audio Notes in Obsidian

**Works on**: Desktop, Mobile
**Cost**: Free
**Quality**: Depends on transcription method

### Setup
1. Record audio directly in Obsidian (or attach audio file)
2. Use plugin or external tool to transcribe

### Plugins to Consider
- **Whisper Transcription**: Local transcription in Obsidian
- **Audio Recorder**: Record audio notes
- **Google Cloud Speech**: Cloud transcription

### Pros/Cons
- ✅ Everything stays in Obsidian
- ✅ Audio attached to note
- ❌ Plugin quality varies
- ❌ Transcription can be slow

---

## Recommended Setup

### For Most Users (Simple)

**iPhone**: Voice Memos → Manual transcribe with MacWhisper → Paste to Inbox
**Mac**: Apple Dictation directly into Obsidian

### For Power Users (Automated)

**Capture**: Otter.ai or Drafts
**Transcribe**: Whisper API
**Route**: Automation to drop `.md` files into `00_Inbox/`

### For Privacy-Conscious

**Capture**: Voice Memos
**Transcribe**: Whisper local (on-device)
**Route**: Manual copy to vault

---

## Voice Capture Best Practices

### 1. Capture Context
Start recordings with context:
> "Note for [project name]: I just realized that..."

This makes processing easier later.

### 2. Keep It Short
Aim for 1-3 minute captures. Longer = harder to process.

### 3. One Thought Per Capture
Don't ramble across multiple topics. Stop, start new recording.

### 4. Process Same Day
Voice captures decay fast. What made sense when you said it may be cryptic tomorrow.

### 5. Use a Consistent Landing Spot
All voice captures → `00_Inbox/Voice/` or a single file `00_Inbox/Voice-Captures.md`

Don't scatter them across the vault.

---

## Voice Capture Template

When processing voice captures, use this format:

```markdown
## Voice Capture - [DATE] [TIME]

**Context**: [Where were you, what prompted this]

**Raw Transcript**:
[Paste transcription here]

**Extracted Actions**:
- [ ] [Action item]
- [ ] [Action item]

**Key Ideas**:
- [Idea 1]
- [Idea 2]

**Route To**: [Project/Context/Knowledge]
```

---

## Integration with Claude

You can have Claude help process voice captures:

```
/add-task Process voice captures from today
```

Or create a custom command `/process-voice`:

```markdown
---
description: Process voice captures from Inbox
---

## Process Voice Captures

1. Read files in `00_Inbox/Voice/` or `00_Inbox/Voice-Captures.md`
2. For each capture:
   - Extract action items
   - Identify project associations
   - Suggest routing
3. Ask user to confirm before moving
```

---

## Troubleshooting

### Transcription is inaccurate
- Speak more clearly, slower
- Use better microphone
- Try Whisper (better than most)
- Edit manually—it's faster than re-recording

### Too many captures piling up
- Set daily reminder to process
- Keep captures shorter
- Be more selective about what to capture

### Can't get files into vault
- Use iCloud/Dropbox sync
- Set up Shortcuts automation
- Accept manual copy as workflow

---

## Summary

| Method | Best For | Effort |
|--------|----------|--------|
| Apple Dictation | Quick captures | Low |
| Whisper | Best accuracy | Medium |
| Voice Memos + Shortcuts | iPhone automation | Medium |
| Otter.ai | Meetings | Low |
| Drafts | Apple power users | Medium |
| Obsidian plugins | All-in-one | Varies |

**Start simple**: Apple Dictation + manual paste into Inbox.
**Upgrade when**: You're capturing >5 voice notes per day and processing is a bottleneck.

---

*Voice capture removes friction. But the value is in processing, not recording.*
