# Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. 

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Contribution Guidelines

1. **Issue Creation**: 
   - Always create an issue before contributing any code or suggesting changes.
   - For new ideas, create a separate issue and discuss with the maintainers before proceeding.

2. **Labels**: 
   - Labels are assigned only once a specific issue is resolved. No labels will be assigned for partial completions or unreviewed contributions.

3. **Adding New Models**:
   - When creating a new model with minimal changes, name it as `V1`, `V2`, etc., based on the upgrade version. Do **not** overwrite the existing model file.
   - Move the existing model to the `past-architecture` folder to track the evolution of model architectures.
   - If you use a different technique, name the file accordingly and include the version number indicating the stage of improvement (e.g., `TechniqueName_V1`).

4. **Model Submission Requirements**:
   - All submissions should include:
     - A ZIP file containing the dataset.
     - The downloaded model file.
     - The accuracy percentage of the model.
   - Create a folder named `latest-model` for each model submission, containing the model with the highest accuracy for that particular technique.
   - **Note**: Only the highest accuracy model should be displayed outside of the `past-architecture` and `latest-model` folders.

5. **Improvement to Existing Models**:
   - If a technique has already been implemented and you believe you can improve the accuracy, create a separate issue before making changes.
   - Points or labels will only be awarded if the improved model achieves higher accuracy using the same technique. A contributor will not receive additional points for the same technique if they have already contributed it.

6. **ReadMe Files**:
   - When submitting a new model, include a `README.md` within the folder explaining:
     - The model architecture.
     - A detailed description of how the model works.
   - Keep the `README.md` file alongside the model in the folder for easy access.

7. **Pull Request Process**:
   - Ensure any install or build dependencies are removed before the end of the layer when doing a build.
   - Update the `CHANGES.md` with details of changes to the interface, including new environment variables, exposed ports, useful file locations, and container parameters.
   - Increase the version numbers in any examples files and the `README.md` to the new version that this Pull Request would represent.

---

## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment include:

- Using welcoming and inclusive language.
- Being respectful of differing viewpoints and experiences.
- Gracefully accepting constructive criticism.
- Focusing on what is best for the community.
- Showing empathy towards other community members.

Examples of unacceptable behavior by participants include:

- The use of sexualized language or imagery and unwelcome sexual attention or advances.
- Trolling, insulting/derogatory comments, and personal or political attacks.
- Public or private harassment.
- Publishing others' private information, such as a physical or electronic address, without explicit permission.
- Other conduct that could reasonably be considered inappropriate in a professional setting.

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable behavior and are expected to take appropriate and fair corrective action in response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or reject comments, commits, code, wiki edits, issues, and other contributions that are not aligned to this Code of Conduct, or to ban temporarily or permanently any contributor for other behaviors that they deem inappropriate, threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces when an individual is representing the project or its community. Examples include using an official project e-mail address, posting via an official social media account, or acting as an appointed representative at an online or offline event. Representation of a project may be further defined and clarified by project maintainers.

### Enforcement Guidelines

To ensure fairness and transparency, we will follow these enforcement guidelines in cases of violations:

#### 1. Warning
A private, written warning will be given to the contributor in response to the first minor incident of unacceptable behavior. The contributor will be informed of the issue, and no further action will be taken unless repeated violations occur.

#### 2. Temporary Ban
For repeated or severe violations, a temporary ban from the community or project spaces may be enforced. The duration will depend on the severity of the incident and the behavior in question.

#### 3. Permanent Ban
In cases of serious, persistent, or malicious violations, the contributor may face a permanent ban from all project spaces. The decision for a permanent ban will involve input from other maintainers.

### Reporting Violations

Instances of abusive, harassing, or otherwise unacceptable behavior may be reported by contacting the project team at [drakathakash@gmail.com](mailto:drakathakash@gmail.com). All complaints will be reviewed and investigated, resulting in a response deemed necessary and appropriate. The project team is obligated to maintain confidentiality with regard to the reporter of an incident.

Project maintainers who do not follow or enforce the Code of Conduct in good faith may face temporary or permanent repercussions as determined by other members of the project's leadership.

---
