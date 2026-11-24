# Deploy each Olive Eyrie theme separately

The two theme folders are independent static sites. Create one Vercel project per folder and use the folder name as that project's **Root Directory**:

| Vercel project | Root Directory | Build settings |
| --- | --- | --- |
| `olive-eyrie-slow-escape` | `theme-one` | Framework: Other; leave build command and output directory empty |
| `olive-eyrie-good-gathering` | `theme-two` | Framework: Other; leave build command and output directory empty |

Each project serves its folder's `index.html` directly. Both themes use only static HTML, CSS, and JavaScript; they need no build step or install command. The image and font assets load from external URLs.

## Current deployment blocker

This workspace is not a Git repository, and Vercel is not connected to this session. The Vercel deployment integration can create and deploy Git-linked projects, but it is unavailable until the Vercel connection is completed and the source is in a repository the integration can access. After that, create the two projects above from the same repository, each with its own root directory.
