- navbar: right #4

- register
	- sendgrid SMTP api
- download data
	- download even if banned
- delete
	- s3 progress (of the job to remove their user archive)
		- unattached/unadopted contributions deletable
		- attached/adopted works around forever, authorship hidden
- recover
	- via email
	- via friend (configure recover roles in settings)
		- decision to send email
	- disable 2fa during recovery
- next-of-kin process
	- recycle (allow username to be reused)
	- memorialize (don't allow re-use)
	- takeover (recovery email shifts to friends)
- log in
	- oauth redirect?
	- vue auth+jwt
	- totp
	- webauthn
		https://github.com/duo-labs/webauthn.io
		https://github.com/duo-labs/webauthn
		https://github.com/google/webauthndemo
- log out
- 