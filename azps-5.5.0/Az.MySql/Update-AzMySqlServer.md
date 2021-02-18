---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 6168c557e3ae3a417f4c04195e6ef166ea3a01d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224092"
---
# <span data-ttu-id="faf22-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="faf22-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="faf22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf22-102">SYNOPSIS</span></span>
<span data-ttu-id="faf22-103">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="faf22-103">Updates an existing server.</span></span>
<span data-ttu-id="faf22-104">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="faf22-105">Используйте Update-AzMySqlConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="faf22-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="faf22-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="faf22-106">SYNTAX</span></span>

### <span data-ttu-id="faf22-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="faf22-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faf22-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="faf22-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faf22-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faf22-109">DESCRIPTION</span></span>
<span data-ttu-id="faf22-110">Обновляет существующий сервер.</span><span class="sxs-lookup"><span data-stu-id="faf22-110">Updates an existing server.</span></span>
<span data-ttu-id="faf22-111">Тело запроса может содержать от одного до многих свойств, присутствующих в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="faf22-112">Используйте Update-AzMySqlConfiguration, если вам нужны параметры сервера обновления, например wait_timeout или net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="faf22-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="faf22-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="faf22-113">EXAMPLES</span></span>

### <span data-ttu-id="faf22-114">Пример 1. Обновление mySql-сервера по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="faf22-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="faf22-115">Этот cmdlet обновляет MySql Server с помощью группы ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="faf22-116">Пример 2. Обновление личных удостоверений на сервере MySql.</span><span class="sxs-lookup"><span data-stu-id="faf22-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="faf22-117">Этот cmdlet обновляет MySql Server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="faf22-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="faf22-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faf22-118">PARAMETERS</span></span>

### <span data-ttu-id="faf22-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="faf22-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="faf22-120">Пароль для входа администратора.</span><span class="sxs-lookup"><span data-stu-id="faf22-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="faf22-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faf22-121">-AsJob</span></span>
<span data-ttu-id="faf22-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="faf22-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="faf22-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="faf22-123">-BackupRetentionDay</span></span>
<span data-ttu-id="faf22-124">Дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-124">Backup retention days for the server.</span></span>
<span data-ttu-id="faf22-125">Количество дней — от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="faf22-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="faf22-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf22-126">-DefaultProfile</span></span>
<span data-ttu-id="faf22-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="faf22-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf22-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faf22-128">-InputObject</span></span>
<span data-ttu-id="faf22-129">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="faf22-129">Identity Parameter.</span></span>
<span data-ttu-id="faf22-130">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="faf22-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="faf22-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="faf22-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="faf22-132">Установите минимальную версию TLS для подключений к серверу, если включен SSL.</span><span class="sxs-lookup"><span data-stu-id="faf22-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="faf22-133">Значение по умолчанию — TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="faf22-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf22-134">-Name</span><span class="sxs-lookup"><span data-stu-id="faf22-134">-Name</span></span>
<span data-ttu-id="faf22-135">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-135">The name of the server.</span></span>

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

### <span data-ttu-id="faf22-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="faf22-136">-NoWait</span></span>
<span data-ttu-id="faf22-137">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="faf22-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="faf22-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="faf22-138">-ReplicationRole</span></span>
<span data-ttu-id="faf22-139">Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="faf22-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf22-140">-ResourceGroupName</span></span>
<span data-ttu-id="faf22-141">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="faf22-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="faf22-142">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="faf22-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="faf22-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="faf22-143">-Sku</span></span>
<span data-ttu-id="faf22-144">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="faf22-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="faf22-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="faf22-145">-SkuCapacity</span></span>
<span data-ttu-id="faf22-146">Возможность масштабирования и утери, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="faf22-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="faf22-147">-SkuFamily</span></span>
<span data-ttu-id="faf22-148">Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="faf22-148">The family of hardware.</span></span>

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

### <span data-ttu-id="faf22-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="faf22-149">-SkuTier</span></span>
<span data-ttu-id="faf22-150">Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="faf22-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="faf22-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="faf22-151">-SslEnforcement</span></span>
<span data-ttu-id="faf22-152">Включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="faf22-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="faf22-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="faf22-153">-StorageAutogrow</span></span>
<span data-ttu-id="faf22-154">Включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="faf22-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="faf22-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="faf22-155">-StorageInMb</span></span>
<span data-ttu-id="faf22-156">Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="faf22-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faf22-157">-SubscriptionId</span></span>
<span data-ttu-id="faf22-158">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="faf22-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="faf22-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="faf22-159">-Tag</span></span>
<span data-ttu-id="faf22-160">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="faf22-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="faf22-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faf22-161">-Confirm</span></span>
<span data-ttu-id="faf22-162">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf22-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf22-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf22-163">-WhatIf</span></span>
<span data-ttu-id="faf22-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf22-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faf22-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="faf22-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf22-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf22-166">CommonParameters</span></span>
<span data-ttu-id="faf22-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf22-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf22-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faf22-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf22-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faf22-169">INPUTS</span></span>

### <span data-ttu-id="faf22-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="faf22-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="faf22-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="faf22-171">OUTPUTS</span></span>

### <span data-ttu-id="faf22-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="faf22-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="faf22-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="faf22-173">NOTES</span></span>

<span data-ttu-id="faf22-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="faf22-174">ALIASES</span></span>

<span data-ttu-id="faf22-175">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="faf22-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="faf22-176">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="faf22-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="faf22-177">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="faf22-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="faf22-178">INPUTOBJECT: <IMySqlIdentity> Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="faf22-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="faf22-179">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="faf22-180">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="faf22-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="faf22-181">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="faf22-182">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="faf22-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="faf22-183">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="faf22-184">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="faf22-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="faf22-185">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="faf22-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="faf22-186">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="faf22-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="faf22-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="faf22-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="faf22-188">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="faf22-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="faf22-189">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="faf22-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="faf22-190">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="faf22-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="faf22-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faf22-191">RELATED LINKS</span></span>

