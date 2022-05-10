## Paper title: The E3SM Diagnostics Package (E3SM Diags v2.6): A Python-basedDiagnostics Package for Earth System Models Evaluation
## Preprint: https://gmd.copernicus.org/preprints/gmd-2022-38/gmd-2022-38.pdf

### Review data

- **Review by: Valeriu Predoi**
- **Date: 10 May 2022**

### General suggestions

- title: E3SM Diags v2.6 is mentioned, but 2.6.1 on conda-forge https://anaconda.org/conda-forge/e3sm_diags
  suggestion: either change to "2.6+" or don't specify the version in the title, or specify why 2.6 is a major
  release even though the number doesn't suggest that way;
- Abstract: please provide a reference/link for AMWG diagnostics package;
- Introduction: line 27: "Most tools listed here are focused on the atmosphere" - not entirely true, ESMValTool
  has a solid component for ocean model data evaluation; suggest changing to "Most tools listed here
  have started with a main focus on the atmosphere, but evolved to analyze other ESM realms too"
- Introduction: line 32 - please provide a reference (methods paper, documentation and/or software repository) for AMWG
- Introduction: line 57 - "...project takes a distinct but related approach" - contradiction in terms
- Introduction: line 63 "Distribution of these Python packages is now mostly accomplished through Conda" - please provide
  a reference to the Anaconda documentation/main page; also note that "conda" is the executable and the
  package manager tool, but Anaconda is the organization and the actual package manager, so it's probably best to 
  use Anaconda in this context, maybe even "Anaconda/Miniconda"
- Introduction: line 72 - "This paper is a comprehensive description of E3SM Diags (as of version 2.6)" - anything special
  about v2.6? Please briefly describe why the choice of version;
- Table 1: I am assuming the references will be available as active links in the final version of the paper?
  (idem): ESMValTool: AR5 and AR6, please, also - ESMValTool is a PyPi package too https://pypi.org/project/ESMValTool/
- Optional: ESMValTool handles OBS datasets too, that are not necessarily CMIP-like file formats, via a process
  of CMOR-standardization (CMORization), maybe woth mentioning?
- Tech overview: line 76 - maybe provide a link to the installation section of your documentation?
- Tech overview: line 83: multi-threading, really, up to you if you want to change from multiprocessing to multi-threading
- Tech overview: general: it would be nice to provide links to various main sections of the package documentation
  e.g. when talking about installation, configuration, running instructions
- S3.1: line 128: how is the reference grid chosen?
- S3.2: line 157: a very detailed explanation on how the (calibration) run works, but a rather frugal explanation of how CMIP data is retrieved from an ESGF node: "The built-in derived variable module takes in CMIP variables and handles variable name and unit conversions" - it'd be good to have this explained a bit better, and in a user-friendly way e.g. data specifications include: var name, mip, experiment name, frequency etc - with these parameters gathered from user input, the code goes and grabs data from the ESGF via standard-path DRS structure conventions etc
- 
