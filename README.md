# H3lix Client

## Introduction

> What is H3lix client? H3lix client is a Minecraft bedrock edition internal hack client meant for people that have nothing better to do than to download and inject a sketchy dll file.

## Code Samples

`Autosprint module`
```cpp
#include "AutoSprint.h"

void AutoSprint::onGmTick() {
	if (Player != nullptr) {
		if (Player->velocity.magnitudexz() > 0.05f) {
			Player->setSprinting(true);
		}
	}
}
```
`ClickTP module`
```cpp
#include "ClickTP.h"

void ClickTP::onMouse(char action, bool isDown, bool* cancel) {
	if (action == 2 && isDown) {
		if (Player != nullptr) {
			MultiPlayerLevel* Level = Player->MultiPlayerLevel;
			Vec3_i blockPos = Level->facingBlockPos;
			if (blockPos != Vec3_i(0, 0, 0)) {
				Player->setPos(Vec3(blockPos.x + 0.5f, blockPos.y + 2.f, blockPos.z + 0.5f));
			}
		}
	}
}
```

## Installation

> 1. Download the injector and dll from "here".
> 2. Unzip them to your desktop.
> 3. Open the injector and Minecraft.
> 4. Once Minecraft is fully loaded and you are in a world, go back to the injector.
> 5. Insert the dll location into the injector, and press inject.
