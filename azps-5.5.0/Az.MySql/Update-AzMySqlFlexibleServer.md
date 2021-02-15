---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214097"
---
# <span data-ttu-id="eef93-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="eef93-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="eef93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef93-102">SYNOPSIS</span></span>
<span data-ttu-id="eef93-103">Обновляет существующий гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="eef93-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="eef93-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="eef93-105">Используйте Update-AzMySqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="eef93-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="eef93-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eef93-106">SYNTAX</span></span>

### <span data-ttu-id="eef93-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eef93-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eef93-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eef93-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eef93-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eef93-109">DESCRIPTION</span></span>
<span data-ttu-id="eef93-110">Обновляет существующий гибкий сервер MySQL.</span><span class="sxs-lookup"><span data-stu-id="eef93-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="eef93-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="eef93-112">Используйте Update-AzMySqlFlexibleServerConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="eef93-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="eef93-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eef93-113">EXAMPLES</span></span>

### <span data-ttu-id="eef93-114">Пример 1. Обновление mySql-сервера по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="eef93-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="eef93-115">Этот cmdlet обновляет MySql Server с помощью группы ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="eef93-116">Пример 2. Обновление личных удостоверений на сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="eef93-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="eef93-117">Этот cmdlet обновляет MySql Server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="eef93-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="eef93-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef93-118">PARAMETERS</span></span>

### <span data-ttu-id="eef93-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="eef93-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="eef93-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="eef93-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="eef93-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eef93-121">-AsJob</span></span>
<span data-ttu-id="eef93-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="eef93-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="eef93-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="eef93-123">-BackupRetentionDay</span></span>
<span data-ttu-id="eef93-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-124">Backup retention days for the server.</span></span>
<span data-ttu-id="eef93-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="eef93-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="eef93-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef93-126">-DefaultProfile</span></span>
<span data-ttu-id="eef93-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eef93-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef93-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="eef93-128">-HaEnabled</span></span>
<span data-ttu-id="eef93-129">Включить или отключить функцию высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="eef93-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="eef93-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eef93-130">-InputObject</span></span>
<span data-ttu-id="eef93-131">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="eef93-131">Identity Parameter.</span></span>
<span data-ttu-id="eef93-132">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="eef93-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eef93-133">-Name</span><span class="sxs-lookup"><span data-stu-id="eef93-133">-Name</span></span>
<span data-ttu-id="eef93-134">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-134">The name of the server.</span></span>

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

### <span data-ttu-id="eef93-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eef93-135">-NoWait</span></span>
<span data-ttu-id="eef93-136">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="eef93-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="eef93-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="eef93-137">-ReplicationRole</span></span>
<span data-ttu-id="eef93-138">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="eef93-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef93-139">-ResourceGroupName</span></span>
<span data-ttu-id="eef93-140">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="eef93-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="eef93-141">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="eef93-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eef93-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="eef93-142">-Sku</span></span>
<span data-ttu-id="eef93-143">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="eef93-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="eef93-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="eef93-144">-SkuTier</span></span>
<span data-ttu-id="eef93-145">Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="eef93-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="eef93-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="eef93-146">-SslEnforcement</span></span>
<span data-ttu-id="eef93-147">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="eef93-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="eef93-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="eef93-148">-StorageAutogrow</span></span>
<span data-ttu-id="eef93-149">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="eef93-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="eef93-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="eef93-150">-StorageInMb</span></span>
<span data-ttu-id="eef93-151">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="eef93-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eef93-152">-SubscriptionId</span></span>
<span data-ttu-id="eef93-153">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="eef93-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="eef93-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="eef93-154">-Tag</span></span>
<span data-ttu-id="eef93-155">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="eef93-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="eef93-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eef93-156">-Confirm</span></span>
<span data-ttu-id="eef93-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eef93-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef93-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef93-158">-WhatIf</span></span>
<span data-ttu-id="eef93-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eef93-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eef93-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eef93-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef93-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef93-161">CommonParameters</span></span>
<span data-ttu-id="eef93-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef93-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef93-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef93-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef93-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eef93-164">INPUTS</span></span>

### <span data-ttu-id="eef93-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="eef93-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="eef93-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eef93-166">OUTPUTS</span></span>

### <span data-ttu-id="eef93-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="eef93-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="eef93-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eef93-168">NOTES</span></span>

<span data-ttu-id="eef93-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="eef93-169">ALIASES</span></span>

<span data-ttu-id="eef93-170">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="eef93-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eef93-171">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="eef93-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eef93-172">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eef93-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eef93-173">INPUTOBJECT: <IMySqlIdentity> Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="eef93-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="eef93-174">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="eef93-175">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="eef93-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="eef93-176">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="eef93-177">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="eef93-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eef93-178">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="eef93-179">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="eef93-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="eef93-180">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eef93-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eef93-181">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="eef93-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="eef93-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="eef93-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="eef93-183">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="eef93-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="eef93-184">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="eef93-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eef93-185">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="eef93-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="eef93-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eef93-186">RELATED LINKS</span></span>

