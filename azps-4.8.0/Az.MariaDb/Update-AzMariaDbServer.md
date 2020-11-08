---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079550"
---
# <span data-ttu-id="dee8d-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="dee8d-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="dee8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dee8d-102">SYNOPSIS</span></span>
<span data-ttu-id="dee8d-103">Обновление существующего сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-103">Updates an existing server.</span></span>
<span data-ttu-id="dee8d-104">Текст запроса может содержать один или несколько свойств, представленных в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="dee8d-105">Если вы хотите изменить параметры сервера, например wait_timeout или net_retry_count, используйте Update-AzMariaDbConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dee8d-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="dee8d-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dee8d-106">SYNTAX</span></span>

### <span data-ttu-id="dee8d-107">ServerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dee8d-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dee8d-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="dee8d-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dee8d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee8d-109">DESCRIPTION</span></span>
<span data-ttu-id="dee8d-110">Обновление существующего сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-110">Updates an existing server.</span></span>
<span data-ttu-id="dee8d-111">Текст запроса может содержать один или несколько свойств, представленных в обычном определении сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="dee8d-112">Если вы хотите изменить параметры сервера, например wait_timeout или net_retry_count, используйте Update-AzMariaDbConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dee8d-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="dee8d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dee8d-113">EXAMPLES</span></span>

### <span data-ttu-id="dee8d-114">Пример 1: обновление MariaDB</span><span class="sxs-lookup"><span data-stu-id="dee8d-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="dee8d-115">Эта команда обновляет MariaDB.</span><span class="sxs-lookup"><span data-stu-id="dee8d-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="dee8d-116">Пример 2: обновление MariaDB</span><span class="sxs-lookup"><span data-stu-id="dee8d-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="dee8d-117">Эта команда обновляет MariaDB.</span><span class="sxs-lookup"><span data-stu-id="dee8d-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="dee8d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dee8d-118">PARAMETERS</span></span>

### <span data-ttu-id="dee8d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="dee8d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="dee8d-120">Пароль для входа в учетную запись администратора.</span><span class="sxs-lookup"><span data-stu-id="dee8d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="dee8d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dee8d-121">-AsJob</span></span>
<span data-ttu-id="dee8d-122">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dee8d-122">Run the command as a job</span></span>

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

### <span data-ttu-id="dee8d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="dee8d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="dee8d-124">Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="dee8d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee8d-125">-DefaultProfile</span></span>
<span data-ttu-id="dee8d-126">Region DefaultParameters учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dee8d-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee8d-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="dee8d-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="dee8d-128">Включите геоизбыточное или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="dee8d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dee8d-129">-InputObject</span></span>
<span data-ttu-id="dee8d-130">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="dee8d-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dee8d-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dee8d-131">-Name</span></span>
<span data-ttu-id="dee8d-132">Имя сервера MariaDB</span><span class="sxs-lookup"><span data-stu-id="dee8d-132">MariaDB server name</span></span>

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

### <span data-ttu-id="dee8d-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="dee8d-133">-NoWait</span></span>
<span data-ttu-id="dee8d-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="dee8d-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dee8d-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="dee8d-135">-ReplicationRole</span></span>
<span data-ttu-id="dee8d-136">Роль сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="dee8d-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="dee8d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee8d-137">-ResourceGroupName</span></span>
<span data-ttu-id="dee8d-138">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="dee8d-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="dee8d-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="dee8d-139">-Sku</span></span>
<span data-ttu-id="dee8d-140">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="dee8d-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="dee8d-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="dee8d-141">-SslEnforcement</span></span>
<span data-ttu-id="dee8d-142">Включите шифрование SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="dee8d-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="dee8d-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="dee8d-143">-StorageAutogrow</span></span>
<span data-ttu-id="dee8d-144">Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="dee8d-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="dee8d-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="dee8d-145">-StorageInMb</span></span>
<span data-ttu-id="dee8d-146">Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="dee8d-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dee8d-147">-SubscriptionId</span></span>
<span data-ttu-id="dee8d-148">Идентификатор подписки — это часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="dee8d-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="dee8d-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="dee8d-149">-Tag</span></span>
<span data-ttu-id="dee8d-150">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="dee8d-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="dee8d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dee8d-151">-Confirm</span></span>
<span data-ttu-id="dee8d-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dee8d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee8d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee8d-153">-WhatIf</span></span>
<span data-ttu-id="dee8d-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dee8d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee8d-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dee8d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee8d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee8d-156">CommonParameters</span></span>
<span data-ttu-id="dee8d-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dee8d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee8d-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dee8d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee8d-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dee8d-159">INPUTS</span></span>

### <span data-ttu-id="dee8d-160">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="dee8d-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="dee8d-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee8d-161">OUTPUTS</span></span>

### <span data-ttu-id="dee8d-162">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="dee8d-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dee8d-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="dee8d-163">NOTES</span></span>

<span data-ttu-id="dee8d-164">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="dee8d-164">ALIASES</span></span>

<span data-ttu-id="dee8d-165">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dee8d-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dee8d-166">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dee8d-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dee8d-167">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dee8d-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dee8d-168">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="dee8d-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dee8d-169">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dee8d-170">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dee8d-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dee8d-171">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dee8d-172">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="dee8d-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dee8d-173">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="dee8d-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dee8d-174">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="dee8d-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dee8d-175">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="dee8d-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dee8d-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dee8d-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dee8d-177">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dee8d-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dee8d-178">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="dee8d-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="dee8d-179">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dee8d-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dee8d-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dee8d-180">RELATED LINKS</span></span>

