# Public GitHub Actions policy

Automatic CI is allowed only for cheap, narrowly scoped checks on `push` to `main`. Do not automatically run test matrices, Windows executables, emulators, GPU jobs or releases. Both existing workflows (`ci.yml`, `build-windows-exe.yml`) require explicit `workflow_dispatch` from `main`; all jobs have main-ref guards. Preserve release approval inputs, permissions and secrets. AI agents should run local tests on feature branches, avoid automatically starting costly CI and inspect actual run logs before reporting success.
