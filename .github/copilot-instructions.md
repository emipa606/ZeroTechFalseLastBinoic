# GitHub Copilot Instructions for ZeroTech-FalseLast-Binoic

## Mod Overview and Purpose
ZeroTech-FalseLast-Binoic is an expansion package for the RimWorld game, built as an update to the LingLuos mod. The mod introduces bionic groups that enhance various aspects of a character's abilities, such as increasing strength, combat effectiveness, and defense. This mod aims to provide players with a deeper level of customization and power management in their RimWorld colonies.

## Key Features and Systems
- **Bionic Groups**: The mod introduces three distinct bionic groups:
  - **Plain White Bionic Group**: Enhances the installer's abilities over time and doubles their consciousness.
  - **Red Blood Bionic Group**: Strengthens the installer's combat abilities with each kill.
  - **Netherbone Bionic Group**: Boosts the installer's defense abilities with each heartbeat.
- **CompLingFPBFenJie**: A component for handling bionic functionality.
- **ComppLingFPBTaoZhuang**: Another component for managing bionic effects.
- **CompLingFPBAiDaQiangHua**: A component for artificial enhancement.

## Coding Patterns and Conventions
- **C# Naming Conventions**: Use PascalCase for class and method names, and camelCase for variables.
- **XML Defs**: Follow the RimWorld XML def conventions, ensuring all attributes and tags are correctly named and nested.
- **Harmony Patching**: Use Harmony patches sparingly and clearly document the purpose and impact of each patch.

## XML Integration
- **Def Files**: The mod includes XML files for various definitions such as `ConceptDef`, `HediffDef`, `ThingDef`, and `RecipeDef`.
- **Structure**: Ensure all XML files are correctly placed in the appropriate directories (e.g., `Defs/Implant`) and follow the RimWorld XML schema.
- **Dependencies**: The mod depends on `LingLuo.ZeroTechCore` and `Mlie.ZeroTechCore`. Ensure these dependencies are properly referenced in the `About.xml` file.

## Harmony Patching
- **Purpose**: Harmony patches are used to modify existing RimWorld code without altering the original files.
- **Usage**: Apply patches to methods that need to be customized or extended.
- **Documentation**: Clearly comment and document each patch to explain its functionality and any potential side effects.

## Suggestions for Copilot
- **Code Completion**: Use Copilot for generating method implementations and boilerplate code, especially for new components and classes.
- **XML Generation**: Utilize Copilot to create XML def files, ensuring all necessary attributes and tags are included.
- **Patch Creation**: Use Copilot to generate Harmony patches, focusing on the specific methods that need to be modified.
- **Error Handling**: Write error handling code using Copilot to manage potential issues during patch application and component initialization.

## Example XML File
xml
<ConceptDef Name="LingLuo_Bionic_PlainWhite" description="Enhances the installer's abilities over time and doubles their consciousness." />


## Example C# Code
csharp
public class CompLingFPBFenJie : ThingComp
{
    public override void PostExposeData()
    {
        base.PostExposeData();
        Scribe_Values.Look(ref someField, "someField");
    }

    public override IEnumerable<Gizmo> CompGetGizmosExtra()
    {
        yield return new Command_Action
        {
            defaultLabel = "Do something",
            action = delegate
            {
                // Action implementation
            }
        };
    }
}


## Example Harmony Patch
csharp
[HarmonyPatch(typeof(SomeClass), "SomeMethod")]
public static class Patch_SomeMethod
{
    public static void Postfix(ref int someParameter)
    {
        someParameter *= 2;
    }
}


By following these guidelines, you can effectively utilize GitHub Copilot to enhance your RimWorld modding experience, ensuring that your code is clean, maintainable, and aligned with the conventions of the RimWorld modding community.

## Project Solution Guidelines
- Relevant mod XML files are included as Solution Items under the solution folder named XML, these can be read and modified from within the solution.
- Use these in-solution XML files as the primary files for reference and modification.
- The `.github/copilot-instructions.md` file is included in the solution under the `.github` solution folder, so it should be read/modified from within the solution instead of using paths outside the solution. Update this file once only, as it and the parent-path solution reference point to the same file in this workspace.
- When making functional changes in this mod, ensure the documented features stay in sync with implementation; use the in-solution `.github` copy as the primary file.
- In the solution is also a project called Assembly-CSharp, containing a read-only version of the decompiled game source, for reference and debugging purposes.
- For any new documentation, update this copilot-instructions.md file rather than creating separate documentation files.


## Hard rules (must follow)
- Do NOT run commands that modify the repo (no git commit, git apply, dotnet format) unless explicitly asked.
- Prefer minimal reads: read only the smallest code region needed (around the suspicious lines).
- When mentioning SonarQube issues, automatically use the SonarQube MCP service to fetch and address issues instead of making inferred fixes without querying SonarQube first.
- When mentioning the rimworld log, automatically use the Rimworld MCP service to fetch the log.

