# VAPI MCP Documentation

---

## 🌟 Overview

The VAPI MCP allows Claude to initiate and manage voice AI phone calls.

---

## ⚡ Capabilities

### Call Management
- **Create Call:** Initiate outbound calls
- **Get Call:** Check call status and transcript
- **List Calls:** View recent calls
- **Stop Call:** End an active call

### Assistant Management
- **List Assistants:** View available voice assistants

---

## 📞 Creating a Call

**Required:**
- Phone number (E.164 format: +1234567890)

**Optional:**
- Assistant ID (or uses default)
- Customer name (for context)
- Call purpose
- First message

---

## 💡 Example Use Cases

### Simple Call
"Call +1234567890 and remind them about the meeting"

### With Specific Assistant
"Use the appointment scheduler assistant to call +1234567890"

### Check Status
"What's the status of call [call-id]?"

### Get Transcript
"Get the transcript from my last call"

---

## 🔧 Tips

1. Always use E.164 phone format
2. Keep first messages concise
3. Define clear call purposes
4. Check call status for transcripts
5. Handle voicemail scenarios

---

## ⚠️ Limitations

- Outbound calls only (via this MCP)
- Call length limits may apply
- Regional restrictions possible
- Costs per call

---

*Voice AI at your command!*