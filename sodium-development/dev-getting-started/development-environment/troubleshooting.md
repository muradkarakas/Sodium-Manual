# Troubleshooting

## Error Messages 

### Mysql installation / Configuration

**Message:** Unable to load authentication plugin 'caching\_sha2\_password'.

**Solution:** [https://stackoverflow.com/questions/50387952/how-to-resolve-unable-to-load-authentication-plugin-caching-sha2-password-issu](https://stackoverflow.com/questions/50387952/how-to-resolve-unable-to-load-authentication-plugin-caching-sha2-password-issu)

```text
mysql.exe –u<username> –p
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1234';
```

