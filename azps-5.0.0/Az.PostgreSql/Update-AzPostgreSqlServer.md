---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247557"
---
# <span data-ttu-id="60f1f-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="60f1f-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="60f1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="60f1f-103">Обновление существующего сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-103">Updates an existing server.</span></span>
<span data-ttu-id="60f1f-104">Текст запроса может содержать один или несколько свойств, представленных в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="60f1f-105">Если вы хотите изменить параметры сервера, например wait_timeout или net_retry_count, используйте Update-AzPostSqlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60f1f-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="60f1f-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60f1f-106">SYNTAX</span></span>

### <span data-ttu-id="60f1f-107">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60f1f-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60f1f-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="60f1f-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60f1f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60f1f-109">DESCRIPTION</span></span>
<span data-ttu-id="60f1f-110">Обновление существующего сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-110">Updates an existing server.</span></span>
<span data-ttu-id="60f1f-111">Текст запроса может содержать один или несколько свойств, представленных в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="60f1f-112">Если вы хотите изменить параметры сервера, например wait_timeout или net_retry_count, используйте Update-AzPostSqlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60f1f-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="60f1f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60f1f-113">EXAMPLES</span></span>

### <span data-ttu-id="60f1f-114">Пример 1: обновление сервера PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="60f1f-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="60f1f-115">Этот командлет обновляет сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="60f1f-116">Пример 2: обновление сервера PostgreSql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="60f1f-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="60f1f-117">Этот командлет обновляет сервер PostgreSql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="60f1f-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="60f1f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60f1f-118">PARAMETERS</span></span>

### <span data-ttu-id="60f1f-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="60f1f-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="60f1f-120">Пароль для входа в учетную запись администратора.</span><span class="sxs-lookup"><span data-stu-id="60f1f-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="60f1f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60f1f-121">-AsJob</span></span>
<span data-ttu-id="60f1f-122">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="60f1f-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="60f1f-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="60f1f-123">-BackupRetentionDay</span></span>
<span data-ttu-id="60f1f-124">Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-124">Backup retention days for the server.</span></span>
<span data-ttu-id="60f1f-125">Число дней в интервале от 7 до 35.</span><span class="sxs-lookup"><span data-stu-id="60f1f-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="60f1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f1f-126">-DefaultProfile</span></span>
<span data-ttu-id="60f1f-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60f1f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f1f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f1f-128">-InputObject</span></span>
<span data-ttu-id="60f1f-129">Параметр удостоверения.</span><span class="sxs-lookup"><span data-stu-id="60f1f-129">Identity Parameter.</span></span>
<span data-ttu-id="60f1f-130">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="60f1f-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60f1f-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60f1f-131">-Name</span></span>
<span data-ttu-id="60f1f-132">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-132">The name of the server.</span></span>

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

### <span data-ttu-id="60f1f-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="60f1f-133">-NoWait</span></span>
<span data-ttu-id="60f1f-134">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="60f1f-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="60f1f-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="60f1f-135">-ReplicationRole</span></span>
<span data-ttu-id="60f1f-136">Роль сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="60f1f-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="60f1f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f1f-137">-ResourceGroupName</span></span>
<span data-ttu-id="60f1f-138">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="60f1f-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="60f1f-139">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="60f1f-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="60f1f-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="60f1f-140">-Sku</span></span>
<span data-ttu-id="60f1f-141">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="60f1f-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="60f1f-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="60f1f-142">-SkuCapacity</span></span>
<span data-ttu-id="60f1f-143">Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="60f1f-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="60f1f-144">-SkuFamily</span></span>
<span data-ttu-id="60f1f-145">Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="60f1f-145">The family of hardware.</span></span>

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

### <span data-ttu-id="60f1f-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="60f1f-146">-SkuTier</span></span>
<span data-ttu-id="60f1f-147">Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="60f1f-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="60f1f-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="60f1f-148">-SslEnforcement</span></span>
<span data-ttu-id="60f1f-149">Включите шифрование SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="60f1f-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="60f1f-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="60f1f-150">-StorageAutogrow</span></span>
<span data-ttu-id="60f1f-151">Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="60f1f-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="60f1f-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="60f1f-152">-StorageInMb</span></span>
<span data-ttu-id="60f1f-153">Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="60f1f-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60f1f-154">-SubscriptionId</span></span>
<span data-ttu-id="60f1f-155">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="60f1f-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="60f1f-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="60f1f-156">-Tag</span></span>
<span data-ttu-id="60f1f-157">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="60f1f-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="60f1f-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60f1f-158">-Confirm</span></span>
<span data-ttu-id="60f1f-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60f1f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f1f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f1f-160">-WhatIf</span></span>
<span data-ttu-id="60f1f-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60f1f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f1f-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60f1f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f1f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f1f-163">CommonParameters</span></span>
<span data-ttu-id="60f1f-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60f1f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f1f-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f1f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f1f-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60f1f-166">INPUTS</span></span>

### <span data-ttu-id="60f1f-167">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="60f1f-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="60f1f-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60f1f-168">OUTPUTS</span></span>

### <span data-ttu-id="60f1f-169">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="60f1f-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="60f1f-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="60f1f-170">NOTES</span></span>

<span data-ttu-id="60f1f-171">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="60f1f-171">ALIASES</span></span>

<span data-ttu-id="60f1f-172">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="60f1f-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60f1f-173">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="60f1f-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60f1f-174">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60f1f-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60f1f-175">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="60f1f-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="60f1f-176">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="60f1f-177">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="60f1f-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="60f1f-178">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="60f1f-179">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="60f1f-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60f1f-180">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="60f1f-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="60f1f-181">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60f1f-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="60f1f-182">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="60f1f-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="60f1f-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="60f1f-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="60f1f-184">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="60f1f-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="60f1f-185">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="60f1f-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="60f1f-186">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="60f1f-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="60f1f-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60f1f-187">RELATED LINKS</span></span>

