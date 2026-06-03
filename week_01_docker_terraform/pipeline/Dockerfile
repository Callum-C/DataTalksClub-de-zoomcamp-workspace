# base docker image we are building on top of
FROM python:3.13.10-slim

# copy uv binary from the official image
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

# Working directory within the container
WORKDIR /app

# Add virtual environment to PATH
ENV PATH="/app/.venv/bin:$PATH"

# Copy dependency files first
COPY "pyproject.toml" "uv.lock" ".python-version" ./

# Install dependencies from lock file
RUN uv sync --locked

# Copy the script to the container. 1st name is source file, 2nd is destination
COPY pipeline.py pipeline.py

# Define what to do first when container runs
ENTRYPOINT ["uv", "run", "python", "pipeline.py"]