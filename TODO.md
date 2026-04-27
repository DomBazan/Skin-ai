# Fix ESLint Warnings in CameraCapture.jsx

## Steps
- [ ] Add `useCallback` to React imports
- [ ] Remove unused `isCapturing` state and its `setIsCapturing` calls
- [ ] Add `isStartingCameraRef` to guard `startCamera` without creating hook deps
- [ ] Wrap `startCamera` in `useCallback` with empty deps (using ref for guard)
- [ ] Wrap `checkCameraPermission` in `useCallback` with `[startCamera]` dep
- [ ] Fix first `useEffect` dep array to `[checkCameraPermission]`
- [ ] Fix second `useEffect` dep array to `[startCamera]` and remove eslint-disable comment
- [ ] Fix redundant `alt` text (`Captured photo` -> `Captured`)
- [ ] Run `npm run build` to verify zero warnings
- [ ] Commit and push changes

