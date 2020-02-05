# Post Game Jam Structure Refactor

02-04-2020

### Feature Branch

```
feature/cleanup-part-two
```

---

## TODO

- [x] Comb over css. Use variables and extract good global styles to root.
- [ ] Add Audio Service [HowlerJS]
- [x] Add Haptic Feedback Service [Navigator.vibrate()]
- [ ] Add Full Screen Service [Fullscreen API]
- [ ] Clean Out Console Logs

---

### Error in `game-asset-data-service.getServiceBotByPlayer()`

Origionally written with an assignment operator. Refactoring to equality.

```typescript
public getServiceBotByPlayer(playerType: string) {
    const serviceBot = this.serviceBots.find(sb => sb.playerType === playerType);
    return serviceBot ? serviceBot : null;
  }
```

---

### SpiderBot Gif Not Showing in player display

Sending the player bio instead of url. Fixed

---

### Join Container Component HTML 

Loop over bots. Done

---

### Haptic Feedback Service

| method   | description                         |
| -------- | ----------------------------------- |
| clear()  | Terminates active vibration         |
| bump()   | Quick tap. Good for touch response. |
| notify() | Short Buzz                          |
| tick()   | Pattern of short taps               |
| danger() | Pattern of long vibrations          |

---





