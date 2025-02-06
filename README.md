# Copying Files from Local Machine to Remote Cloud Machine Using SSH

## Syntax
```bash
scp [source_file_path] [username]@[remote_host]:[destination_path]
```

## Examples

### Copy a File to the Remote Machine's Home Directory
```bash
scp ~/Documents/example.txt user@remote_server_ip_or_domain:~
```

### Copy a File to a Specific Directory on the Remote Machine
```bash
scp ~/Documents/example.txt user@remote_server_ip:/path/to/target_directory/
```

### Copy an Entire Directory
Add the `-r` flag for recursive copying.
```bash
scp -r ~/my_folder user@remote_server_ip:/path/to/target_directory/
```

## Key Options
- `-P [port_number]`: Specify an SSH port if it isn't the default (22).
- `-i [path_to_private_key]`: Use a specific private key file for authentication.

## Example with Non-Default Port and Key File
```bash
scp -P 2222 -i ~/.ssh/my_key.pem ~/file.txt user@remote_server_ip:/path/to/target_directory/
```

## Notes
- Ensure that the SSH service is running on the remote server.
- You may need correct permissions to access the target directory.
- If prompted, enter your SSH password or key passphrase.
