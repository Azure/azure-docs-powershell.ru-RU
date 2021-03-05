---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0db4d25f224f1c6984ba9b57184859e8fa2c6c28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003864"
---
# <span data-ttu-id="5426b-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="5426b-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="5426b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5426b-102">SYNOPSIS</span></span>
<span data-ttu-id="5426b-103">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="5426b-103">Updates an existing server.</span></span>
<span data-ttu-id="5426b-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5426b-105">Используйте Update-AzMariaDbConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5426b-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5426b-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5426b-106">SYNTAX</span></span>

### <span data-ttu-id="5426b-107">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5426b-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5426b-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="5426b-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5426b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5426b-109">DESCRIPTION</span></span>
<span data-ttu-id="5426b-110">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="5426b-110">Updates an existing server.</span></span>
<span data-ttu-id="5426b-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5426b-112">Используйте Update-AzMariaDbConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5426b-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5426b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5426b-113">EXAMPLES</span></span>

### <span data-ttu-id="5426b-114">Пример 1. Обновление MariaDB</span><span class="sxs-lookup"><span data-stu-id="5426b-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="5426b-115">Эта команда обновляет Ее.</span><span class="sxs-lookup"><span data-stu-id="5426b-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="5426b-116">Пример 2. Обновление MariaDB</span><span class="sxs-lookup"><span data-stu-id="5426b-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="5426b-117">Эта команда обновляет Ее.</span><span class="sxs-lookup"><span data-stu-id="5426b-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="5426b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5426b-118">PARAMETERS</span></span>

### <span data-ttu-id="5426b-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5426b-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5426b-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="5426b-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="5426b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5426b-121">-AsJob</span></span>
<span data-ttu-id="5426b-122">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5426b-122">Run the command as a job</span></span>

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

### <span data-ttu-id="5426b-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5426b-123">-BackupRetentionDay</span></span>
<span data-ttu-id="5426b-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="5426b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5426b-125">-DefaultProfile</span></span>
<span data-ttu-id="5426b-126">Region DefaultParameters The credentials, account, tenant и subscription, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5426b-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5426b-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="5426b-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="5426b-128">В этой области можно включить гео избыточное резервное копирование или не использовать резервное копирование на сервере.</span><span class="sxs-lookup"><span data-stu-id="5426b-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5426b-129">-InputObject</span></span>
<span data-ttu-id="5426b-130">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5426b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5426b-131">-Name</span></span>
<span data-ttu-id="5426b-132">Имя сервера MariaDB</span><span class="sxs-lookup"><span data-stu-id="5426b-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5426b-133">-NoWait</span></span>
<span data-ttu-id="5426b-134">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5426b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5426b-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="5426b-135">-ReplicationRole</span></span>
<span data-ttu-id="5426b-136">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="5426b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5426b-137">-ResourceGroupName</span></span>
<span data-ttu-id="5426b-138">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="5426b-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="5426b-139">-Sku</span></span>
<span data-ttu-id="5426b-140">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5426b-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="5426b-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="5426b-141">-SslEnforcement</span></span>
<span data-ttu-id="5426b-142">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="5426b-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="5426b-143">-StorageAutogrow</span></span>
<span data-ttu-id="5426b-144">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="5426b-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5426b-145">-StorageInMb</span></span>
<span data-ttu-id="5426b-146">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="5426b-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5426b-147">-SubscriptionId</span></span>
<span data-ttu-id="5426b-148">ИД подписки является частью URI для каждого звонка в службу</span><span class="sxs-lookup"><span data-stu-id="5426b-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5426b-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="5426b-149">-Tag</span></span>
<span data-ttu-id="5426b-150">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="5426b-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5426b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5426b-151">-Confirm</span></span>
<span data-ttu-id="5426b-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5426b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5426b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5426b-153">-WhatIf</span></span>
<span data-ttu-id="5426b-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5426b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5426b-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5426b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5426b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5426b-156">CommonParameters</span></span>
<span data-ttu-id="5426b-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5426b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5426b-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5426b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5426b-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5426b-159">INPUTS</span></span>

### <span data-ttu-id="5426b-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="5426b-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="5426b-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5426b-161">OUTPUTS</span></span>

### <span data-ttu-id="5426b-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="5426b-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5426b-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5426b-163">NOTES</span></span>

<span data-ttu-id="5426b-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5426b-164">ALIASES</span></span>

<span data-ttu-id="5426b-165">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5426b-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5426b-166">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5426b-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5426b-167">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5426b-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5426b-168">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5426b-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5426b-169">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5426b-170">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5426b-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5426b-171">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5426b-172">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5426b-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5426b-173">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="5426b-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5426b-174">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="5426b-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5426b-175">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="5426b-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5426b-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5426b-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5426b-177">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5426b-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5426b-178">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="5426b-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="5426b-179">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="5426b-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5426b-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5426b-180">RELATED LINKS</span></span>

