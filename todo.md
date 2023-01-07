1. [ ] load config file (using viper)
2. [ ] stdlib mux
3. [ ] stdlib session
	1. JWT (shortlived)
		1. use cookies, set cookie as SameSite strict
	2. fallback to session in redis (for refresh)
	3. redirect to auth
4. [ ] postgres handler https://github.com/jackc/pgx (instead of GORM)
5. [ ] smtp handler
6. [ ] https://github.com/marketplace/actions/discord-webhook-action
7. [ ] nginx static catch for app.html