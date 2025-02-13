| 参数名                                         | 描述                                                                             |
| ---------------------------------------------- | -------------------------------------------------------------------------------- |
| `spring.r2dbc.url`                             | 数据库连接地址，详细可查阅下方的 `数据库配置`                                    |
| `spring.r2dbc.username`                        | 数据库用户名                                                                     |
| `spring.r2dbc.password`                        | 数据库密码                                                                       |
| `spring.sql.init.platform`                     | 数据库平台名称，支持 `postgresql`、`mysql`、`h2`，需要与 `SPRING_R2DBC_URL` 对应 |
| `halo.external-url`                            | 外部访问链接，如果需要再公网访问，需要配置为实际访问地址                         |
| `halo.security.initializer.superadminusername` | 初始超级管理员用户名                                                             |
| `halo.security.initializer.superadminpassword` | 初始超级管理员密码                                                               |

数据库配置：

| 链接方式    | 链接地址格式                                                                       | `SPRING_SQL_INIT_PLATFORM` |
| ----------- | ---------------------------------------------------------------------------------- | -------------------------- |
| PostgreSQL  | `r2dbc:pool:postgresql://{HOST}:{PORT}/{DATABASE}`                                 | postgresql                 |
| MySQL       | `r2dbc:pool:mysql://{HOST}:{PORT}/{DATABASE}`                                      | mysql                      |
| H2 Database | `r2dbc:h2:file:///${halo.work-dir}/db/halo-next?MODE=MySQL&DB_CLOSE_ON_EXIT=FALSE` | h2                         |
