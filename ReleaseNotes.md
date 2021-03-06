# Release Notes

# 1.5.2

## Features

- Update clojure version to 1.3.0

- Update to jclouds 1.5.5

- Enable node tags for AWS EC2.

- Implement compute-service-properties.  The service can now be introspected.

- Implement NodeHardware protocol.  Node hardware is now queryable.

## Fixes

- Fix service-properties support in jclouds 1.5.6+

- Fix node tagging support

- Remove slingshot and fix 0.8 tests

- Log node start failure exceptions

- Use only :image-id for template if specified
  Stop other information in the template from preventing a match.

- Ensure node start exceptions are reported

# 1.5.1

- Fix destruction of failed nodes

# 1.5.0

- Handle case where jclouds returns nil credentials

- Update to jclouds 1.5.2

# 1.5.0-alpha.1

- Update to jclouds 1.5.0 beta.11

- Make jclouds-all and jclouds-sshj test scoped

- Make os-version return nil instead of an empty string
  When the version is not available from jclouds, avoid returning an empty
  string.

- Force the use of a run script
  This ensures that ssh is useable when the nodes are returned from jclouds

- Add test for image-user and fix

- Add support for pallet 0.8.x

- Add logic to detect sshj and jsch extensions
  jsch was being assumed.

- Add jclouds template to logging

- Ensure ssh-port returns a value

- Implement getStatus on ComputeMetadataIncludingStatus
  It was being implemented on NodeMetadata

- Add getStatus method to JcloudsNode
