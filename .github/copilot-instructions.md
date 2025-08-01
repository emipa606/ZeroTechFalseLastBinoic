# GitHub Copilot Instructions for ZeroTech-FalseLast-Bionic (Continued)

Welcome to the ZeroTech-FalseLast-Bionic (Continued) mod project for RimWorld. This document provides guidelines and instructions for using GitHub Copilot effectively when contributing to this project.

## Mod Overview and Purpose

ZeroTech-FalseLast-Bionic is a continuation and expansion of LingLuos' original mod. It introduces advanced bionic technologies that significantly enhance the abilities and combat capabilities of colonists in the game of RimWorld. By installing various bionic groups, players can achieve unprecedented strength and defense.

## Key Features and Systems

- **Plain White Bionic Group**: Increases the individual abilities of a colonist over time, doubling the consciousness of the installer through the suit effect.
  
- **Red Blood Bionic Group**: Enhances combat capabilities by increasing individual abilities with each kill.

- **Netherbone Bionic Group**: Strengthens defense by enhancing individual abilities with beat counts.

These features introduce new strategic elements to the gameplay, allowing players to augment their colonists in unique ways.

## Coding Patterns and Conventions

- **Namespace Consistency**: Ensure all classes are within a coherent naming structure relevant to their functionality.

- **Class Naming**: Classes such as `Comp_LingSpawnItem` and `CompLingFPBAiDaQiangHua` should remain descriptive of their role, usually indicating the component type and specific function.

- **Method Naming**: Use camelCase for method names, maintaining descriptiveness. For instance, a method like `aHasHediff()` clearly communicates its purpose.

## XML Integration

- Utilize XML to define the properties and behaviors of bionic components and effects. 

- Ensure XML data definitions are clear and map correctly to C# classes and properties. This enables easier data-driven development and balance adjustments.

## Harmony Patching

- Use the Harmony library for patching RimWorld's existing functionality. This allows for non-destructive changes and enhances compatibility with other mods.

- Craft precise patches to target specific methods. Keep Harmony patch methods static and prefix them with the `HarmonyPatch` attribute to clearly indicate their purpose.

## Suggestions for Copilot

To make effective use of GitHub Copilot:

- **Provide Clear Context**: When writing code, keep your variable, class, and method names descriptive; this helps Copilot suggest more relevant completions.

- **Use Inline Comments**: Comment your code where complex logic is involved, which aids Copilot in understanding the context and purpose of the code.

- **Leverage Existing Patterns**: When adding new features, look at existing classes and methods to understand established patterns. This helps Copilot suggest consistent code snippets.

- **Iterate and Optimize**: Use Copilot proposals as a starting point; feel free to iterate upon them to better fit the project's needs and conventions.

By following these guidelines, contributors can maintain a high standard of code quality and contribute effectively to the continued development of ZeroTech-FalseLast-Bionic.
