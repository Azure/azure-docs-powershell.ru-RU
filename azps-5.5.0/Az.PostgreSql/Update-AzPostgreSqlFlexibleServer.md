---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218068"
---
# <span data-ttu-id="e2f0a-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="e2f0a-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="e2f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f0a-103">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-103">Updates an existing server.</span></span>
<span data-ttu-id="e2f0a-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e2f0a-105">Используйте Update-AzPostSqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e2f0a-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2f0a-106">SYNTAX</span></span>

### <span data-ttu-id="e2f0a-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f0a-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2f0a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2f0a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2f0a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f0a-109">DESCRIPTION</span></span>
<span data-ttu-id="e2f0a-110">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-110">Updates an existing server.</span></span>
<span data-ttu-id="e2f0a-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e2f0a-112">Используйте Update-AzPostgreSqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e2f0a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f0a-113">EXAMPLES</span></span>

### <span data-ttu-id="e2f0a-114">Пример 1. Обновление сервера PostgreSql с помощью имени группы ресурсов и сервера</span><span class="sxs-lookup"><span data-stu-id="e2f0a-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="e2f0a-115">Этот cmdlet обновляет сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="e2f0a-116">Пример 2. Обновление сервера PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="e2f0a-117">Этот cmdlet обновляет Сервер PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="e2f0a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2f0a-118">PARAMETERS</span></span>

### <span data-ttu-id="e2f0a-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e2f0a-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="e2f0a-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="e2f0a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2f0a-121">-AsJob</span></span>
<span data-ttu-id="e2f0a-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="e2f0a-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="e2f0a-123">-BackupRetentionDay</span></span>
<span data-ttu-id="e2f0a-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-124">Backup retention days for the server.</span></span>
<span data-ttu-id="e2f0a-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="e2f0a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f0a-126">-DefaultProfile</span></span>
<span data-ttu-id="e2f0a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f0a-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="e2f0a-128">-HaEnabled</span></span>
<span data-ttu-id="e2f0a-129">Включить или отключить функцию высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f0a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f0a-130">-InputObject</span></span>
<span data-ttu-id="e2f0a-131">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-131">Identity Parameter.</span></span>
<span data-ttu-id="e2f0a-132">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2f0a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e2f0a-133">-Name</span></span>
<span data-ttu-id="e2f0a-134">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-134">The name of the server.</span></span>

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

### <span data-ttu-id="e2f0a-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2f0a-135">-NoWait</span></span>
<span data-ttu-id="e2f0a-136">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e2f0a-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="e2f0a-137">-ReplicationRole</span></span>
<span data-ttu-id="e2f0a-138">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="e2f0a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f0a-139">-ResourceGroupName</span></span>
<span data-ttu-id="e2f0a-140">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e2f0a-141">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e2f0a-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2f0a-142">-Sku</span></span>
<span data-ttu-id="e2f0a-143">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e2f0a-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e2f0a-144">-SkuTier</span></span>
<span data-ttu-id="e2f0a-145">Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="e2f0a-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="e2f0a-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="e2f0a-146">-SslEnforcement</span></span>
<span data-ttu-id="e2f0a-147">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="e2f0a-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="e2f0a-148">-StorageAutogrow</span></span>
<span data-ttu-id="e2f0a-149">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="e2f0a-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="e2f0a-150">-StorageInMb</span></span>
<span data-ttu-id="e2f0a-151">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="e2f0a-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2f0a-152">-SubscriptionId</span></span>
<span data-ttu-id="e2f0a-153">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e2f0a-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2f0a-154">-Tag</span></span>
<span data-ttu-id="e2f0a-155">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e2f0a-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f0a-156">-Confirm</span></span>
<span data-ttu-id="e2f0a-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f0a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f0a-158">-WhatIf</span></span>
<span data-ttu-id="e2f0a-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f0a-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f0a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f0a-161">CommonParameters</span></span>
<span data-ttu-id="e2f0a-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f0a-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2f0a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f0a-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2f0a-164">INPUTS</span></span>

### <span data-ttu-id="e2f0a-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e2f0a-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e2f0a-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2f0a-166">OUTPUTS</span></span>

### <span data-ttu-id="e2f0a-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e2f0a-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="e2f0a-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2f0a-168">NOTES</span></span>

<span data-ttu-id="e2f0a-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2f0a-169">ALIASES</span></span>

<span data-ttu-id="e2f0a-170">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e2f0a-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2f0a-171">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2f0a-172">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2f0a-173">INPUTOBJECT <IPostgreSqlIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e2f0a-174">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e2f0a-175">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e2f0a-176">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e2f0a-177">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e2f0a-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2f0a-178">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e2f0a-179">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e2f0a-180">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="e2f0a-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e2f0a-182">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e2f0a-183">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e2f0a-184">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="e2f0a-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e2f0a-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f0a-185">RELATED LINKS</span></span>

