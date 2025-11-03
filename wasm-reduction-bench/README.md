# wasm-reduction-bench

This directory contains wasm-reduction-bench, a collection of 28 bug-triggering Wasm programs with the oracle scripts and engines.

## Example usage

NOTE: You should add PATH to [./engines](./engines) directory before running the reduction tools.

Every Wasm program reduction tool has different cli options. But most take the bug-triggering Wasm program and an oracle script as input.
In our benchmark, an oracle script is a Python script that returns exit code 0 if the input Wasm program triggers the bug, and exit code 1 otherwise.

Here is an example command with [wasm-shrink](https://crates.io/crates/wasm-shrink)

```bash
wasm-tools shrink ./oracles/fixed-by-718f067.py ./programs/wamr#2789.wasm
```

## List of programs

wasm-reduction-bench contains the following 28 bug-triggering Wasm programs under the [programs](./programs) directory.

- boa.wasm
- bullet.wasm
- commanderkeen.wasm
- ffmpeg.wasm
- figma-startpage.wasm
- funky-kart.wasm
- guiicons.wasm
- hydro.wasm
- jqkungfu.wasm
- jsc.wasm
- mandelbrot.wasm
- pacalc.wasm
- parquet.wasm
- pathfinding.wasm
- rfxgen.wasm
- rguilayout.wasm
- rguistyler.wasm
- riconpacker.wasm
- rtexviewer.wasm
- sandspiel.wasm
- sqlgui.wasm
- wamr#2450.wasm
- wamr#2789.wasm
- wamr#2862.wasm
- wasmedge#3018.wasm
- wasmedge#3019.wasm
- wasmedge#3057.wasm
- wasmedge#3076.wasm

## List of engines

wasm-reduction-bench contains the following 39 engines under the [engines](./engines) directory.
They are compiled for x86_64 Linux.

NOTE: wasmedge-862fffd.tar.gz and wasmedge-93fd4ae.tar.gz exceeded the size limit of GitHub, so they are included as .tar.gz files. You should extract them before use.

- iwasm-0b0af1b
- iwasm-0ee5ffc
- iwasm-7308b1e
- iwasm-8d1cf46
- iwasm-b6216a5
- iwasm-e360b7a
- wamrc-0b0af1b
- wamrc-0ee5ffc
- wamrc-718f067
- wamrc-7308b1e
- wamrc-873558c
- wamrc-b6216a5
- wasmedge-862fffd
- wasmedge-93fd4ae
- wasmtime-14.0.4
- wizard-0b43b85
- wizard-0d6926f
- wizard-253bd02
- wizard-25abe41
- wizard-25e04ac
- wizard-33ec201
- wizard-4e3e221
- wizard-563da52
- wizard-5b33b84
- wizard-67358ae
- wizard-6d2b057
- wizard-6e539a4
- wizard-6e594e9
- wizard-708ea77
- wizard-81555ab
- wizard-92a333
- wizard-92a3330
- wizard-b576c16
- wizard-be2b145
- wizard-c0f4ac3
- wizard-ccf0c56
- wizard-d46ae4f
- wizard-f7aca00
- wizard-fe0487a

## List of oracle scripts

wasm-reduction-bench contains the following 13 oracle scripts under the [oracles](./oracles) directory.

- fixed-by-0b43b85.py
- fixed-by-0ee5ffc.py
- fixed-by-33ec201.py
- fixed-by-4e3e221.py
- fixed-by-6d2b057.py
- fixed-by-708ea77.py
- fixed-by-718f067.py
- fixed-by-81555ab.py
- fixed-by-93fd4ae.py
- fixed-by-bc135ad.py
- fixed-by-ccf0c56.py
- fixed-by-e360b7a.py
- fixed-by-f7aca00.py

## Mapping of programs to oracles

The following table shows which oracle script corresponds to which Wasm program.

| Program (.wasm)      | Oracle script       |
| -------------------- | ------------------- |
| boa.wasm             | fixed-by-6d2b057.py |
| bullet.wasm          | fixed-by-f7aca00.py |
| commanderkeen.wasm   | fixed-by-bc135ad.py |
| ffmpeg.wasm          | fixed-by-4e3e221.py |
| figma-startpage.wasm | fixed-by-33ec201.py |
| funky-kart.wasm      | fixed-by-6d2b057.py |
| guiicons.wasm        | fixed-by-6d2b057.py |
| hydro.wasm           | fixed-by-708ea77.py |
| jqkungfu.wasm        | fixed-by-4e3e221.py |
| jsc.wasm             | fixed-by-6d2b057.py |
| mandelbrot.wasm      | fixed-by-0b43b85.py |
| pacalc.wasm          | fixed-by-81555ab.py |
| parquet.wasm         | fixed-by-33ec201.py |
| pathfinding.wasm     | fixed-by-ccf0c56.py |
| rfxgen.wasm          | fixed-by-6d2b057.py |
| rguilayout.wasm      | fixed-by-6d2b057.py |
| rguistyler.wasm      | fixed-by-6d2b057.py |
| riconpacker.wasm     | fixed-by-6d2b057.py |
| rtexviewer.wasm      | fixed-by-708ea77.py |
| sandspiel.wasm       | fixed-by-ccf0c56.py |
| sqlgui.wasm          | fixed-by-6d2b057.py |
| wamr#2450.wasm       | fixed-by-e360b7a.py |
| wamr#2789.wasm       | fixed-by-718f067.py |
| wamr#2862.wasm       | fixed-by-0ee5ffc.py |
| wasmedge#3018.wasm   | fixed-by-93fd4ae.py |
| wasmedge#3019.wasm   | fixed-by-93fd4ae.py |
| wasmedge#3057.wasm   | fixed-by-93fd4ae.py |
| wasmedge#3076.wasm   | fixed-by-93fd4ae.py |

## Citation

To refer to wasm-reduction-bench in your publications, please use the following BibTeX entry:

```bibtex
@inproceedings{Baek2025RR-Reduce,
  author       = {Doehyun Baek and Daniel Lehmann and Ben L. Titzer and Sukyoung Ryu and Michael Pradel},
  title        = {Execution-Aware Program Reduction for WebAssembly via Record and Replay},
  booktitle    = {Proceedings of the 39th {IEEE/ACM} International Conference on Automated Software Engineering, {ASE} 2025, Seoul, South Korea, November 16 - November 20, 2025},
  year         = {2025},
}
```
