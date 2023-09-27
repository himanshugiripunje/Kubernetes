      apiVersion: snapshot.storage.k8s.io/v1
      kind: VolumeSnapshot
      metadata:
        name: new-snapshot-test
      spec:
        volumeSnapshotClassName: vol-snap-class
        source:
          persistentVolumeClaimName: nfs-pvc
      apiVersion: snapshot.storage.k8s.io/v1
      kind: VolumeSnapshotClass
      metadata:
        name: vol-snap-class
      driver: hostpath.csi.k8s.io
      deletionPolicy: Delete
      parameters:
      apiVersion: snapshot.storage.k8s.io/v1
      kind: VolumeSnapshotContent
      metadata:
        name: vol-snap-content
      spec:
        deletionPolicy: Delete
        driver: hostpath.csi.k8s.io
        source:
          snapshotHandle: 7bdd0de3-aaeb-11e8-9aae-0242ac110002
        volumeSnapshotRef:
          name: new-snapshot-test
        volumeSnapshotClassName: vol-snap-class
