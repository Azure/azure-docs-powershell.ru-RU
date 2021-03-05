---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3d6358d52663c71e06b8186d9123d24b0587d253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968792"
---
# <span data-ttu-id="434b4-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="434b4-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="434b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434b4-102">SYNOPSIS</span></span>
<span data-ttu-id="434b4-103">Обновляет существующий гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="434b4-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="434b4-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="434b4-105">Используйте Update-AzMySqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="434b4-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="434b4-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="434b4-106">SYNTAX</span></span>

### <span data-ttu-id="434b4-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="434b4-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="434b4-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="434b4-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-MaintenanceWindow <String>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="434b4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="434b4-109">DESCRIPTION</span></span>
<span data-ttu-id="434b4-110">Обновляет существующий гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="434b4-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="434b4-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="434b4-112">Используйте Update-AzMySqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="434b4-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="434b4-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="434b4-113">EXAMPLES</span></span>

### <span data-ttu-id="434b4-114">Пример 1. Обновление mySql-сервера по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="434b4-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="434b4-115">Этот cmdlet обновляет MySql Server по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="434b4-116">Пример 2. Обновление личных удостоверений на сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="434b4-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="434b4-117">Этот cmdlet обновляет MySql Server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="434b4-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="434b4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="434b4-118">PARAMETERS</span></span>

### <span data-ttu-id="434b4-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="434b4-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="434b4-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="434b4-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="434b4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="434b4-121">-AsJob</span></span>
<span data-ttu-id="434b4-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="434b4-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="434b4-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="434b4-123">-BackupRetentionDay</span></span>
<span data-ttu-id="434b4-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-124">Backup retention days for the server.</span></span>
<span data-ttu-id="434b4-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="434b4-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="434b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434b4-126">-DefaultProfile</span></span>
<span data-ttu-id="434b4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="434b4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434b4-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="434b4-128">-HaEnabled</span></span>
<span data-ttu-id="434b4-129">Включить или отключить функцию высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="434b4-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434b4-130">-InputObject</span></span>
<span data-ttu-id="434b4-131">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="434b4-131">Identity Parameter.</span></span>
<span data-ttu-id="434b4-132">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="434b4-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="434b4-133">-MaintenanceWindow</span></span>
<span data-ttu-id="434b4-134">Период времени (UTC), назначенный для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="434b4-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="434b4-135">Примеры: "Вс:23:30", чтобы запланировать на воскресенье, 23:30 (UTC).</span><span class="sxs-lookup"><span data-stu-id="434b4-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="434b4-136">Чтобы вернуть стандартный проход в "Отключено"</span><span class="sxs-lookup"><span data-stu-id="434b4-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="434b4-137">-Name</span><span class="sxs-lookup"><span data-stu-id="434b4-137">-Name</span></span>
<span data-ttu-id="434b4-138">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-138">The name of the server.</span></span>

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

### <span data-ttu-id="434b4-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="434b4-139">-NoWait</span></span>
<span data-ttu-id="434b4-140">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="434b4-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="434b4-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="434b4-141">-ReplicationRole</span></span>
<span data-ttu-id="434b4-142">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="434b4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434b4-143">-ResourceGroupName</span></span>
<span data-ttu-id="434b4-144">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="434b4-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="434b4-145">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="434b4-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="434b4-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="434b4-146">-Sku</span></span>
<span data-ttu-id="434b4-147">Как правило, это название SKU уровня +family + cores, например Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="434b4-147">The name of the sku, typically, tier + family + cores, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="434b4-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="434b4-148">-SkuTier</span></span>
<span data-ttu-id="434b4-149">Уровень конкретного SKU.</span><span class="sxs-lookup"><span data-stu-id="434b4-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="434b4-150">Принятые значения: Скайп, ОбщееТип, Оптимизированная память.</span><span class="sxs-lookup"><span data-stu-id="434b4-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="434b4-151">По умолчанию: срыв.</span><span class="sxs-lookup"><span data-stu-id="434b4-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="434b4-152">-SslEnforcement</span></span>
<span data-ttu-id="434b4-153">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="434b4-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="434b4-154">-StorageAutogrow</span></span>
<span data-ttu-id="434b4-155">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="434b4-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="434b4-156">-StorageInMb</span></span>
<span data-ttu-id="434b4-157">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="434b4-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="434b4-158">-SubscriptionId</span></span>
<span data-ttu-id="434b4-159">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="434b4-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="434b4-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="434b4-160">-Tag</span></span>
<span data-ttu-id="434b4-161">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="434b4-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="434b4-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="434b4-162">-Confirm</span></span>
<span data-ttu-id="434b4-163">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="434b4-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434b4-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434b4-164">-WhatIf</span></span>
<span data-ttu-id="434b4-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="434b4-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434b4-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="434b4-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434b4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434b4-167">CommonParameters</span></span>
<span data-ttu-id="434b4-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434b4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434b4-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="434b4-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434b4-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="434b4-170">INPUTS</span></span>

### <span data-ttu-id="434b4-171">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="434b4-171">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="434b4-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="434b4-172">OUTPUTS</span></span>

### <span data-ttu-id="434b4-173">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="434b4-173">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="434b4-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="434b4-174">NOTES</span></span>

<span data-ttu-id="434b4-175">ALIASES</span><span class="sxs-lookup"><span data-stu-id="434b4-175">ALIASES</span></span>

<span data-ttu-id="434b4-176">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="434b4-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="434b4-177">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="434b4-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="434b4-178">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="434b4-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="434b4-179">INPUTOBJECT <IMySqlIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="434b4-179">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="434b4-180">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="434b4-181">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="434b4-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="434b4-182">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="434b4-183">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="434b4-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="434b4-184">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-184">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="434b4-185">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="434b4-185">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="434b4-186">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="434b4-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="434b4-187">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="434b4-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="434b4-188">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="434b4-188">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="434b4-189">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="434b4-189">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="434b4-190">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="434b4-190">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="434b4-191">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="434b4-191">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="434b4-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="434b4-192">RELATED LINKS</span></span>

