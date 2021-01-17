---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391884"
---
# <span data-ttu-id="64b09-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="64b09-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="64b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b09-102">SYNOPSIS</span></span>
<span data-ttu-id="64b09-103">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="64b09-103">Updates an existing server.</span></span>
<span data-ttu-id="64b09-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="64b09-105">Используйте Update-AzPostSqlConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="64b09-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="64b09-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64b09-106">SYNTAX</span></span>

### <span data-ttu-id="64b09-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64b09-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64b09-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64b09-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64b09-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64b09-109">DESCRIPTION</span></span>
<span data-ttu-id="64b09-110">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="64b09-110">Updates an existing server.</span></span>
<span data-ttu-id="64b09-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="64b09-112">Используйте Update-AzPostSqlConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="64b09-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="64b09-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64b09-113">EXAMPLES</span></span>

### <span data-ttu-id="64b09-114">Пример 1. Обновление сервера PostgreSql с помощью имени группы ресурсов и сервера</span><span class="sxs-lookup"><span data-stu-id="64b09-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="64b09-115">Этот cmdlet обновляет сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="64b09-116">Пример 2. Обновление сервера PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="64b09-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="64b09-117">Этот cmdlet обновляет Сервер PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="64b09-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="64b09-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64b09-118">PARAMETERS</span></span>

### <span data-ttu-id="64b09-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="64b09-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="64b09-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="64b09-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64b09-121">-AsJob</span></span>
<span data-ttu-id="64b09-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="64b09-122">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="64b09-123">-BackupRetentionDay</span></span>
<span data-ttu-id="64b09-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-124">Backup retention days for the server.</span></span>
<span data-ttu-id="64b09-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="64b09-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b09-126">-DefaultProfile</span></span>
<span data-ttu-id="64b09-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64b09-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64b09-128">-InputObject</span></span>
<span data-ttu-id="64b09-129">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="64b09-129">Identity Parameter.</span></span>
<span data-ttu-id="64b09-130">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="64b09-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-131">-Name</span><span class="sxs-lookup"><span data-stu-id="64b09-131">-Name</span></span>
<span data-ttu-id="64b09-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64b09-133">-NoWait</span></span>
<span data-ttu-id="64b09-134">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="64b09-134">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="64b09-135">-ReplicationRole</span></span>
<span data-ttu-id="64b09-136">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-136">The replication role of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b09-137">-ResourceGroupName</span></span>
<span data-ttu-id="64b09-138">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="64b09-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="64b09-139">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="64b09-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="64b09-140">-Sku</span></span>
<span data-ttu-id="64b09-141">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="64b09-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="64b09-142">-SkuCapacity</span></span>
<span data-ttu-id="64b09-143">Возможность масштабирования и утери, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-143">The scale up/out capacity, representing server's compute units.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="64b09-144">-SkuFamily</span></span>
<span data-ttu-id="64b09-145">Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="64b09-145">The family of hardware.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="64b09-146">-SkuTier</span></span>
<span data-ttu-id="64b09-147">Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="64b09-147">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="64b09-148">-SslEnforcement</span></span>
<span data-ttu-id="64b09-149">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="64b09-149">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="64b09-150">-StorageAutogrow</span></span>
<span data-ttu-id="64b09-151">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="64b09-151">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="64b09-152">-StorageInMb</span></span>
<span data-ttu-id="64b09-153">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-153">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64b09-154">-SubscriptionId</span></span>
<span data-ttu-id="64b09-155">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="64b09-155">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="64b09-156">-Tag</span></span>
<span data-ttu-id="64b09-157">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="64b09-157">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64b09-158">-Confirm</span></span>
<span data-ttu-id="64b09-159">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64b09-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b09-160">-WhatIf</span></span>
<span data-ttu-id="64b09-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64b09-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b09-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="64b09-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b09-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b09-163">CommonParameters</span></span>
<span data-ttu-id="64b09-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b09-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b09-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64b09-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b09-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64b09-166">INPUTS</span></span>

### <span data-ttu-id="64b09-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="64b09-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="64b09-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64b09-168">OUTPUTS</span></span>

### <span data-ttu-id="64b09-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="64b09-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="64b09-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64b09-170">NOTES</span></span>

<span data-ttu-id="64b09-171">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64b09-171">ALIASES</span></span>

<span data-ttu-id="64b09-172">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="64b09-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64b09-173">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="64b09-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64b09-174">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64b09-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64b09-175">INPUTOBJECT: <IPostgreSqlIdentity> Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="64b09-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="64b09-176">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="64b09-177">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="64b09-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="64b09-178">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="64b09-179">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="64b09-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64b09-180">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="64b09-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="64b09-181">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64b09-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="64b09-182">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="64b09-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="64b09-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="64b09-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="64b09-184">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="64b09-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="64b09-185">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="64b09-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="64b09-186">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="64b09-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="64b09-187">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64b09-187">RELATED LINKS</span></span>

