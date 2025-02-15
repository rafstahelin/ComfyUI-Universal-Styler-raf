
# ComfyUI Universal Styler RAF

## **Problem**

The original ComfyUI-NAI-styler node has a hardcoded path that causes loading delays and browser refresh issues when updating through ComfyUI's custom node manager.

## **Solution**

Created a forked version with corrected paths to avoid conflicts and maintain stability through updates.

## **Setup Instructions**

1. Fork and Clone

```bash
git clone https://github.com/rafstahelin/ComfyUI-Universal-Styler-raf.git
cd ComfyUI-Universal-Styler-raf
```

1. Configure Git (if not already done)

```bash
git config --global user.name "your_username"
git config --global user.email "your_email"
```

1. Set Up Upstream for Updates

```bash
git remote add upstream https://github.com/KoreTeknology/ComfyUI-NAI-styler.git
```

## **Updating the Node**

When new updates are available from the original repository:

```bash
git fetch upstream
git merge upstream/main --strategy-option ours --strategy recursive -X ours
```

This method preserves local path modifications while pulling new features and fixes.

## **Key Changes**

- Modified **`naistyler_nodes.py`** to use correct folder path
- Renamed repository to avoid conflicts with original
- Implemented Git strategy to maintain changes through updates

## **Notes**

- Original loading delay issue resolved
- Updates from original repository can be safely pulled
- Node functionality remains unchanged
- Path modifications persist through ComfyUI updates

*Created by @rafstahelin to fix ComfyUI-NAI-styler path issues*
