# [Choice] Node.js version (use -bullseye variants on local arm64/Apple Silicon): 20, 18, 16, 14, 20-bullseye, 18-bullseye, 16-bullseye, 14-bullseye, 20-buster, 18-buster, 16-buster, 14-buster
ARG VARIANT=20-bullseye
FROM node:${VARIANT}

# ENV IMAGE_VARIANT="20-bullseye"

# COPY library-scripts/add-patch.sh /tmp/library-scripts/
# RUN bash /tmp/library-scripts/add-patch.sh "${IMAGE_VARIANT}" && rm -rf /tmp/library-scripts

# ARG USERNAME=node
# ARG NPM_GLOBAL=/usr/local/share/npm-global

# # Add NPM global to PATH.
# ENV PATH=${NPM_GLOBAL}/bin:${PATH}

# RUN \
#     # Configure global npm install location, use group to adapt to UID/GID changes
#     if ! cat /etc/group | grep -e "^npm:" > /dev/null 2>&1; then groupadd -r npm; fi \
#     && usermod -a -G npm ${USERNAME} \
#     && umask 0002 \
#     && mkdir -p ${NPM_GLOBAL} \
#     && touch /usr/local/etc/npmrc \
#     && chown ${USERNAME}:npm ${NPM_GLOBAL} /usr/local/etc/npmrc \
#     && chmod g+s ${NPM_GLOBAL} \
#     && npm config -g set prefix ${NPM_GLOBAL} \
#     && su ${USERNAME} -c "npm config -g set prefix ${NPM_GLOBAL}" \
#     # Install eslint
#     && su ${USERNAME} -c "umask 0002 && npm install -g eslint" \
#     && npm cache clean --force > /dev/null 2>&1