---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974664"
---
# <span data-ttu-id="8e07c-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="8e07c-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="8e07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e07c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e07c-103">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="8e07c-103">Updates an existing server.</span></span>
<span data-ttu-id="8e07c-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8e07c-105">Используйте Update-AzPostSqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8e07c-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8e07c-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e07c-106">SYNTAX</span></span>

### <span data-ttu-id="8e07c-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e07c-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e07c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8e07c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e07c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e07c-109">DESCRIPTION</span></span>
<span data-ttu-id="8e07c-110">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="8e07c-110">Updates an existing server.</span></span>
<span data-ttu-id="8e07c-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8e07c-112">Используйте Update-AzPostgreSqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8e07c-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8e07c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e07c-113">EXAMPLES</span></span>

### <span data-ttu-id="8e07c-114">Пример 1. Обновление сервера PostgreSql с помощью имени группы ресурсов и сервера</span><span class="sxs-lookup"><span data-stu-id="8e07c-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="8e07c-115">Этот cmdlet обновляет сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="8e07c-116">Пример 2. Обновление сервера PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8e07c-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="8e07c-117">Этот cmdlet обновляет Сервер PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="8e07c-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="8e07c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e07c-118">PARAMETERS</span></span>

### <span data-ttu-id="8e07c-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8e07c-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8e07c-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="8e07c-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8e07c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e07c-121">-AsJob</span></span>
<span data-ttu-id="8e07c-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="8e07c-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="8e07c-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8e07c-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8e07c-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-124">Backup retention days for the server.</span></span>
<span data-ttu-id="8e07c-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="8e07c-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8e07c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e07c-126">-DefaultProfile</span></span>
<span data-ttu-id="8e07c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e07c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e07c-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="8e07c-128">-HaEnabled</span></span>
<span data-ttu-id="8e07c-129">Включить или отключить функцию высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="8e07c-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="8e07c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e07c-130">-InputObject</span></span>
<span data-ttu-id="8e07c-131">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="8e07c-131">Identity Parameter.</span></span>
<span data-ttu-id="8e07c-132">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="8e07c-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e07c-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="8e07c-133">-MaintenanceWindow</span></span>
<span data-ttu-id="8e07c-134">Период времени (UTC), назначенный для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8e07c-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="8e07c-135">Примеры: "Вс:23:30", чтобы запланировать на воскресенье, 23:30 (UTC).</span><span class="sxs-lookup"><span data-stu-id="8e07c-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="8e07c-136">Чтобы вернуться к стандартной сдавли в режиме "Отключено"</span><span class="sxs-lookup"><span data-stu-id="8e07c-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="8e07c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="8e07c-137">-Name</span></span>
<span data-ttu-id="8e07c-138">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-138">The name of the server.</span></span>

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

### <span data-ttu-id="8e07c-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e07c-139">-NoWait</span></span>
<span data-ttu-id="8e07c-140">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8e07c-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8e07c-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8e07c-141">-ReplicationRole</span></span>
<span data-ttu-id="8e07c-142">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="8e07c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e07c-143">-ResourceGroupName</span></span>
<span data-ttu-id="8e07c-144">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="8e07c-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8e07c-145">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8e07c-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8e07c-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="8e07c-146">-Sku</span></span>
<span data-ttu-id="8e07c-147">Название SKU, например Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="8e07c-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="8e07c-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8e07c-148">-SkuTier</span></span>
<span data-ttu-id="8e07c-149">Уровень конкретного SKU.</span><span class="sxs-lookup"><span data-stu-id="8e07c-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="8e07c-150">Принятые значения: Скайп, ОбщееТип, Оптимизированная память.</span><span class="sxs-lookup"><span data-stu-id="8e07c-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="8e07c-151">По умолчанию: срыв.</span><span class="sxs-lookup"><span data-stu-id="8e07c-151">Default: Burstable.</span></span>

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

### <span data-ttu-id="8e07c-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8e07c-152">-SslEnforcement</span></span>
<span data-ttu-id="8e07c-153">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="8e07c-153">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="8e07c-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8e07c-154">-StorageAutogrow</span></span>
<span data-ttu-id="8e07c-155">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="8e07c-155">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="8e07c-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8e07c-156">-StorageInMb</span></span>
<span data-ttu-id="8e07c-157">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8e07c-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e07c-158">-SubscriptionId</span></span>
<span data-ttu-id="8e07c-159">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="8e07c-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8e07c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e07c-160">-Tag</span></span>
<span data-ttu-id="8e07c-161">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="8e07c-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8e07c-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e07c-162">-Confirm</span></span>
<span data-ttu-id="8e07c-163">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e07c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e07c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e07c-164">-WhatIf</span></span>
<span data-ttu-id="8e07c-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e07c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e07c-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e07c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e07c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e07c-167">CommonParameters</span></span>
<span data-ttu-id="8e07c-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e07c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e07c-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e07c-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e07c-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e07c-170">INPUTS</span></span>

### <span data-ttu-id="8e07c-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8e07c-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8e07c-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e07c-172">OUTPUTS</span></span>

### <span data-ttu-id="8e07c-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8e07c-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="8e07c-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e07c-174">NOTES</span></span>

<span data-ttu-id="8e07c-175">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8e07c-175">ALIASES</span></span>

<span data-ttu-id="8e07c-176">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8e07c-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e07c-177">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8e07c-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e07c-178">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e07c-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e07c-179">INPUTOBJECT: <IPostgreSqlIdentity> Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="8e07c-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8e07c-180">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8e07c-181">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="8e07c-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8e07c-182">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8e07c-183">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8e07c-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e07c-184">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="8e07c-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8e07c-185">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e07c-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8e07c-186">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8e07c-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="8e07c-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8e07c-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8e07c-188">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8e07c-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8e07c-189">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8e07c-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8e07c-190">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="8e07c-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8e07c-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e07c-191">RELATED LINKS</span></span>

