---
title: "記録保管庫"
slug: "doc"
---


git filter-branch --force --env-filter '
        # GIT_COMMITTER_NAMEの書き換え
        if [ "$GIT_COMMITTER_NAME" = "95128233+at-im@user.noreply.github.com ];
        then
                GIT_COMMITTER_NAME="imachange@proton.me";
        fi
        ' -- --all