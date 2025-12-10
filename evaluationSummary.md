# Evaluation Results

## Performance in general
- **Total line mappings**: 286
- **Correct mappings**: 236
- **Accuracy**: 82.5%  
Check **'testEclipse.csv'** for complete and detailed results

**Perfect Performance (100%):**
- BaseTypes (v2-7)
- DirectoryDialog
- JavaCodeScanner
- JavaModelManager

**Strong Performance:**
- ArrayReference (91.7%)
- CompilationUnitDocumentProvider (94.1%)
- GC (92.3%)
- GC2 (90.9%)

**Average - Weak Performance:**
- TabFolder (16.7%)
- ASTResolving (50%)
- PluginSearchScope (50%)
- SaveManager (66.7%)
- RefreshLocal (66.7%)

 Perform well on typical code modifications, a bit struggle with heavy refactoring, accuracy exceeds Unix diff baseline
