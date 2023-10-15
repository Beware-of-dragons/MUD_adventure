Game Design Document - Beware of Dragons

# Game Design Document - Beware of Dragons

## Table of Contents

- [Introduction](#introduction)
  - [Vision Statement](#vision-statement)
  - [Purpose of the GDD](#purpose-of-the-gdd)
  - [Target Audience](#target-audience)
- [Game Overview](#game-overview)
  - [Concept](#concept)
  - [Genre](#genre)
  - [Target Audience](#target-audience)
- [World Building](#world-building)
  - [Lore and Storyline](#lore-and-storyline)
  - [Factions](#factions)
  - [NPCs and Creatures](#npcs-and-creatures)
  - [Locations and Environments](#locations-and-environments)
- [Game Mechanics](#game-mechanics)
  - [Character Classes](#character-classes)
  - [Combat System](#combat-system)
  - [Leveling and Progression](#leveling-and-progression)
  - [Player Interaction](#player-interaction)
  - [Quests and Challenges](#quests-and-challenges)
- [Technical Specifications](#technical-specifications)
  - [Platforms](#platforms)
  - [Programming Languages and Tools](#programming-languages-and-tools)
  - [Database and Server Requirements](#database-and-server-requirements)
  - [Network Architecture](#network-architecture)
  - [Art and Sound Design](#art-and-sound-design)
  - [Art Style](#art-style)
  - [Audio Elements](#audio-elements)
  - [Character and Environment Design](#character-and-environment-design)
  - [User Interface and Experience](#user-interface-and-experience)
  - [Interface Design](#interface-design)
  - [Navigation and Controls](#navigation-and-controls)
  - [Player Feedback](#player-feedback)
- [Development Timeline](#development-timeline)
  - [Milestones](#milestones)
  - [Progress Tracking](#progress-tracking)
  - [Iteration and Testing](#iteration-and-testing)
- [Appendices](#appendices)
- [Glossary](#glossary)
- [References](#references)

# Introduction

## Vision Statement

"Beware of Dragons" is an ambitious project rooted in the realms of Elixir and Phoenix, aimed at creating an immersive and captivating high-fantasy Multi-User Dungeon (MUD) text adventure game. Our vision for this project is twofold:

- **A Captivating Adventure:** At its core, "Beware of Dragons" is an epic adventure set in a richly crafted fantasy world. It offers players the opportunity to explore mythical realms, uncover secrets, and face formidable challenges. As they delve deeper into the game's lore, they will confront choices that have a lasting impact on the game's narrative, making every playthrough a unique and unforgettable experience.

- **A Comprehensive Learning Resource:** Beyond being a game, "Beware of Dragons" serves as a learning resource for game developers, distributed systems enthusiasts, and anyone eager to explore the fusion of fantasy gaming and technical implementation. We aim to provide valuable insights into game design, storytelling, and the intricacies of distributed systems, helping individuals build their skills while they embark on an epic adventure.

## Purpose of the GDD

The purpose of this Game Design Document (GDD) is to serve as a comprehensive blueprint for "Beware of Dragons." Within these pages, you'll find detailed information about the game's mechanics, character classes, combat systems, lore, and much more. Our aim is to offer guidance and understanding to:

- **Game Developers:** Whether you're a seasoned developer or just starting your journey in game development, this GDD offers insights into the creation of MUD text adventure games. It provides a clear path for mastering Elixir, Phoenix, and LiveView while building your game development expertise.

- **Distributed Systems Enthusiasts:** "Beware of Dragons" delves into the technical aspects of creating a multiplayer game, introducing you to the complex world of distributed systems. Through our technical documentation, you'll gain a deeper understanding of the infrastructure supporting the game.

- **Fantasy Enthusiasts:** If you have a passion for high-fantasy worlds, immersive storytelling, and epic adventures, "Beware of Dragons" is sure to captivate your imagination. The game offers a rich and engaging experience set in a universe where creativity knows no bounds.

- **Open Source Contributors:** Join our community of contributors and help shape the development of "Beware of Dragons." Your input and expertise are invaluable in making this project a collaborative and community-driven effort.

## Target Audience

- **Game Developers:** This GDD serves as a one-of-a-kind resource to guide you through the process of creating a MUD text adventure game using Elixir, Phoenix, and LiveView. From design principles to technical implementation, we have you covered, whether you're a beginner or a seasoned developer.

- **Distributed Systems Enthusiasts:** "Beware of Dragons" is more than just a game; it's a technical journey into distributed systems. Discover the complexities and best practices involved in building a multiplayer game with real-world applications.

- **Fantasy Enthusiasts:** Immerse yourself in a high-fantasy world filled with captivating lore, mythical creatures, and epic adventures. "Beware of Dragons" is a playground for your imagination.

- **Open Source Contributors:** We invite you to be part of our growing community. Contribute your skills and knowledge to bring "Beware of Dragons" to life and shape the future of this project.

In "Beware of Dragons," we aim to inspire, educate, and entertain. Whether you're looking to master game development, explore distributed systems, or embark on an unforgettable adventure, this project has something for you. Join us as we journey through the realms of imagination and technology, bound only by the limits of our creativity.

# World Building

## Lore and Backstory
The world of "Beware of Dragons" is a realm where the echoes of darkness and light collide. Ages ago, the world was forged by powerful beings known as the Celestial Architects. They shaped the land, seeded it with magic, and created the races that would inhabit it. The Celestial Architects then departed, leaving behind relics of immense power, coveted by many.

## Geography and Environments
The game world, known as Echovale, is a diverse landscape with tranquil valleys, ancient forests, imposing mountain ranges, and hidden caves. The central location is the Phenixian Citadel, home to the Phenixian Order, perched atop a mountain. The Eclipsian Brotherhood, a treacherous faction, operates from the darkened forests of the Eclipsian Enclave. Beyond them, the Dragon Vanguard guards the sacred lairs of the mighty dragons, deep in the Dragon Spine Mountains.

## Societies and Cultures
Echovale is inhabited by three main factions: the Phenixian Order, the Eclipsian Brotherhood, and the Dragon Vanguard. Each has its own unique culture, values, and traditions. The Phenixian Order values purity, discipline, and the protection of the ancient relics. The Eclipsian Brotherhood seeks to awaken the long-forgotten King using the power of shadows. The Dragon Vanguard consists of individuals who have forged bonds with dragons and seek to protect them from external threats.

## Political Landscape
Echovale doesn't have a unified political structure; instead, each faction operates independently. Tensions and conflicts are rife among them. The Phenixian Order maintains a delicate balance between purity and shadows. The Eclipsian Brotherhood is secretive, with spies infiltrating the Order. The Dragon Vanguard remains an enigmatic force, protecting dragons from both the Order and Brotherhood.

## Religion and Beliefs
Religion plays a minor role in Echovale. The Phenixian Order reveres the Celestial Architects as divine beings. The Eclipsian Covenant has no central religious figure. The Dragon Vanguard views their connection to dragons as a spiritual bond.

## Magic
Magic is prevalent throughout Echovale. The Order practices Aurawelding, a discipline of light and purity, while the Covenant delves into Shadowweaving, the arcane magic of shadows.

# Game Overview

## Concept
Beware of Dragons is a high-fantasy Multi-User Dungeon (MUD) text adventure game that transports players into the mesmerizing realm of Echovale. As a captivating fusion of rich storytelling and technical innovation, this open-source project offers players an immersive journey through a world teeming with mythical creatures, epic quests, and ever-evolving challenges. In this multi-faceted experience, players will find themselves immersed in a captivating narrative, challenged by dynamic combat, and driven by their choices within a complex web of factions, alliances, and rivalries.

## Genre
Beware of Dragons seamlessly blends elements of classic MUDs with the complexity and engagement of modern role-playing games. The game's genre is a melding of high-fantasy, action, and adventure, designed to captivate a diverse audience, from seasoned role-players to those new to the genre. 

## Target Audience
The game is designed to cater to a broad audience. Whether you're a seasoned MUD player looking for a fresh and engaging experience or a newcomer eager to explore the world of text-based games, Beware of Dragons offers a diverse experience for players of all backgrounds.

Intrigued adventurers, creative storytellers, and those interested in understanding the technical underpinnings of MUDs will find something to explore within the game. As an open-source project, this game is not only for those who play it but also for those who wish to understand how games are built from the ground up.

In the following sections, we will delve deeper into the mechanics, the technical aspects, the world-building, and the overall vision for Beware of Dragons.

## Game Mechanics

In Beware of Dragons, the game mechanics are designed to deliver a captivating and immersive experience for players. Here, we explore various facets of the game, from character classes and builds to the currency system, the real-time combat system, and elixirs that enhance gameplay.

### Character Classes

In the world of Beware of Dragons, players choose from three distinct factions, each offering a unique set of character classes:

- **The Order of the Radiant Dawn:** This noble and chivalrous faction provides character classes like Knights, Clerics, and Paladins. Knights are renowned for their exceptional combat skills, while Clerics specialize in healing and support magic. Paladins, on the other hand, combine martial prowess with divine abilities.

- **The Eclipsian Covenant:** The shadowy and enigmatic Covenant features character classes such as Necromancers, Shadowweavers, and Assassins. Necromancers command the forces of death and summon undead minions. Shadowweavers wield dark magic to manipulate shadows, and Assassins are experts in stealth and precision.

- **The Dragon Guardians:** This faction embraces the power of dragons, with character classes like Dragon Warriors, Flame Adepts, and Stormcallers. Dragon Warriors are formidable melee combatants who can form a bond with dragons. Flame Adepts specialize in fire magic, while Stormcallers command the forces of air and electricity.

### Mid/Advanced Character Builds

As players progress through the game, they have the opportunity to refine and diversify their character builds:

- **Mid-Builds:** Upon reaching intermediate levels, players can specialize within their chosen class. For instance, an Order Knight might focus on enhancing their defensive abilities, while an Order Cleric could become a master of healing and support spells.

- **Advanced Builds:** At higher levels, characters can explore advanced builds that blend skills from different classes, resulting in unique and versatile character archetypes. For example, an Order Knight might combine their tanking abilities with some healing spells to create a specialized hybrid build.

### Currency System

#### Astral Essence
- **Source**: Obtained by defeating monsters and enemies in the world.
- **Use as Currency**: Players can spend Astral Essence to buy various in-game items, weapons, and elixirs. This common resource serves as a universal currency in Echovale.
- **Use in Skill Tree**: Astral Essence can be allocated in the player's skill tree to unlock and enhance various abilities and skills. It's a versatile resource that empowers the character's progression.

#### Dragon Shards
- **Source**: Acquired by defeating mid to high-level enemies, especially those with ties to dragons.
- **Use for Equipment Enhancement**: Dragon Shards can be used to enhance and upgrade equipment, such as weapons, armor, and accessories. This resource is crucial for improving the player's combat capabilities and survivability.

#### Ephemeral Soulshards
- **Source**: Rarely found, Ephemeral Soulshards are challenging to obtain and often require defeating powerful foes.
- **Use for Elixir Enhancement**: Ephemeral Soulshards are used to improve the elixirs' effects and expand the player's elixir capacity. They offer a unique advantage in battles by enhancing temporary status boosts.
- **Increase Elixir Capacity**: As players collect more Ephemeral Soulshards, they can gradually increase the maximum number of elixirs they can carry at a time, allowing for better strategic planning and adaptability during challenging encounters.

This currency system balances the in-game economy, rewards players for defeating tougher foes, and promotes thoughtful resource management. It also reinforces the interconnectedness of currency, character progression, and equipment enhancement, enriching the overall gaming experience.

### Combat System

Beware of Dragons boasts a real-time combat system that rewards strategic thinking, precise timing, and resource management:

- **Resource Management:** Combat relies on three primary resources: stamina for physical actions, action points for special abilities, and magic points for casting spells.

- **Status Effects:** Players must be vigilant as various status effects can sway the tide of battle, adding an extra layer of strategy to encounters.

- **Timing and Precision:** In the heat of battle, timing and precision are paramount to success. Players must hone their skills and strategies to overcome formidable foes.

### Elixirs

Elixirs play a crucial role in Beware of Dragons, offering temporary enhancements to players:

- **Five Unique Elixirs:** These elixirs provide distinct benefits, including healing, magical replenishment, and temporary boosts to accuracy and resilience.

- **Elixir Management:** Players begin with the ability to carry a maximum of three elixirs. Through key items discovered during their adventures, they can expand their elixir capacity to a total of eight.

- **Resting at Pyres:** Resting at pyres located throughout the game world allows players to replenish their elixir charges, ensuring they are always prepared for challenging encounters.

The game mechanics in Beware of Dragons are thoughtfully designed to provide players with a dynamic, engaging, and strategic gaming experience. From character class choices to currency management and the nuances of real-time combat, every element contributes to an immersive and rewarding gameplay journey.