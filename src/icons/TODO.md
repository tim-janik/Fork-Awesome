
## Possibly uncentered

The following Font-Awesome icons could be improved by horizontally centering:

    ls \
    arrow* \
    backward* \
    university* \
    calendar* \
    fort-awesome* \
    forward* \
    hand-* \
    ils* \
    key* \
    long-arrow-* \
    mars-stroke-* \
    maxcdn* \
    mercury* \
    paragraph* \
    pie-chart* \
    sort-amount-* \
    street-view* \
    television* \
    transgender* \
    truck* \
    user-* \
    venus*


## Missing viewBox specification

The following Fork-Awesome icons still need a viewBox:

    att.svg
    bell-rigning-o.svg
    bell-ringing.svg
    discord-alt.svg
    discord.svg
    ffmpeg.svg
    globe-e.svg
    globe-w.svg
    gnupg.svg
    joplin.svg
    medium-square.svg
    patreon.svg
    peertube.svg
    snowdrift.svg
    sun.svg
    tor-onion.svg
    volume-mute.svg
    wire.svg


## Incorrect viewBox specification

The list of remaining Fork-Awesome icons. Some of which need
viewBox fixups to avoid clipping or out-of-bounds positioning:

    activitypub.svg
    archive-org.svg
    archlinux.svg
    artstation.svg
    biometric.svg
    bootstrap.svg
    c.svg
    debian.svg
    dev-to.svg
    diaspora.svg
    digitalocean.svg
    dogmazic.svg
    emby.svg
    ethereum.svg
    facebook-messenger.svg
    f-droid.svg
    file-epub.svg
    fork-awesome.svg
    freedombox.svg
    friendica.svg
    gimp.svg
    gitea.svg
    gnu-social.svg
    hackaday.svg
    hackster.svg
    hashnode.svg
    hubzilla.svg
    inkscape.svg
    jirafeau.svg
    keybase.svg
    key-modern.svg
    laravel.svg
    liberapay-square.svg
    liberapay.svg
    mastodon-alt.svg
    mastodon-square.svg
    mastodon.svg
    matrix-org.svg
    moon.svg
    nextcloud-square.svg
    nextcloud.svg
    nodejs.svg
    php.svg
    pixelfed.svg
    pleroma.svg
    python.svg
    react.svg
    scuttlebutt.svg
    shaarli-o.svg
    shaarli.svg
    signalapp.svg
    social-home.svg
    spell-check.svg
    syncthing.svg
    tipeee.svg
    unslpash.svg
    wikidata.svg
    xmpp.svg
    zotero.svg


## Remove clipPath definitions

The file signalapp.svg needs cleanups to remove unused clipPath
and filter specifications. The icon looks like it can be reduced
to an ordinary path.


## Make Sprite Release

    cd src/icons/svg
    test -z "`git status -zu`" || echo ERROR: clean untracked files
    ../../../node_modules/.bin/svgstore `fgrep viewBox *.svg -l` -o fork-awesome-sprites-0.0.svg
