# ML_hodgepodge

Different essentials to teach Machine Learning to other groups.
This repository will be updated as different lessons are required.

**Levels.**

- `Basic` : The most basic lessons, starting from scratch and self-contained.
- `Intermediate` : More advanced lessons that assume basic libraries are already known and installed, but still self-contained in terms of what is taught.
- `Advanced` : Lessons that employ the standard library structure, featuring more complex code not that self-contained.

## Structure

The repository is structured into the following directories:

- `/data`: Data folder.
- `/notebook`: Notebooks folder, with self-contained lessons.

## Tools

- [uv](https://docs.astral.sh/uv/): Manage dependencies, Python versions and virtual environments.

### UV

#### Repository usage

1. [Install uv](https://docs.astral.sh/uv/getting-started/installation/).
2. Clone repository
3. Install package and dependencies in a virtual environment:

    ```{bash}
    uv sync
    ```

4. Run reposiroty scripts with uv run, for instance:

    ```{bash}
    uv run main.py
    ```

    Alternatively, activate the virtual env and run the scripts normally:

    ```{bash}
    source .venv/bin/activate
    ```

#### Development

- Add dependencies:

    ```{bash}
    uv add <PACKAGE>
    ```

- Add dev dependencies:

    ```{bash}
    uv add --dev <PACKAGE>
    ```

uv automatically updates `uv.lock` file and sync the environment. This can also be done manually with:

```{bash}
uv sync
```

In addition, `uv.lock` can be manually regenerated with:

```{bash}
uv lock
```

- Remove dependency:

    ```{bash}
    uv remove <PACKAGE>
    ```

In order to remove any virtual env, just make sure it is into the working directory (`ls -lha .`) and remove it with:

```{bash}
rm -rf .venv
```

- Check dependencies:

    ```{bash}
    uv pip list
    ```

## Additiona info

### Template

For a broader Python template, go check [Template for Python libraries by Komorebi-AI](https://github.com/Komorebi-AI/python-template)