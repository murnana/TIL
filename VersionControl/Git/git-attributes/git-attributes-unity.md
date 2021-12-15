## Unity用の`gitattributes`のテンプレ

```
*   text encoding=utf-8 eol=lf

# Text
.gitignore          text encoding=utf-8 eol=lf linguist-vendored export-ignore
.gitattributes      text encoding=utf-8 eol=lf linguist-vendored export-ignore
.editorconfig       text encoding=utf-8 eol=lf linguist-vendored
*.md                text encoding=utf-8 eol=lf linguist-vendored
*.cs                text encoding=utf-8 eol=lf
*.meta              text encoding=utf-8 eol=lf linguist-vendored
*.asset             text encoding=utf-8 eol=lf linguist-vendored
*.txt               text encoding=utf-8 eol=lf linguist-vendored
*.json              text encoding=utf-8 eol=lf linguist-vendored
*.asmdef            text encoding=utf-8 eol=lf linguist-vendored
*.shader            text encoding=utf-8 eol=lf
*.hlsl              text encoding=utf-8 eol=lf
*.shadersubgraph    text encoding=utf-8 eol=lf
*.mat               text encoding=utf-8 eol=lf linguist-vendored
*.playable          text encoding=utf-8 eol=lf linguist-vendored
*.unity             text encoding=utf-8 eol=lf linguist-vendored

# Audio
*.wav   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored
*.mp3   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored

# Font
*.ttf   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored

# Image
*.png   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored
*.tif   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored

# Model
*.fbx   binary filter=lfs diff=lfs merge=lfs -text linguist-vendored
*.blend binary filter=lfs diff=lfs merge=lfs -text linguist-vendored
```
