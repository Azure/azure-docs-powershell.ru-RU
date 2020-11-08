---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243519"
---
# <span data-ttu-id="8956e-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="8956e-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="8956e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8956e-102">SYNOPSIS</span></span>
<span data-ttu-id="8956e-103">Создание реплики сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="8956e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8956e-104">SYNTAX</span></span>

### <span data-ttu-id="8956e-105">ServerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8956e-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8956e-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="8956e-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8956e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8956e-107">DESCRIPTION</span></span>
<span data-ttu-id="8956e-108">Создание реплики сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="8956e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8956e-109">EXAMPLES</span></span>

### <span data-ttu-id="8956e-110">Пример 1: создание базы данных реплики для MariaDB</span><span class="sxs-lookup"><span data-stu-id="8956e-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8956e-111">Эта команда создает базу данных реплики для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="8956e-112">Пример 2: создание базы данных реплики для MariaDB</span><span class="sxs-lookup"><span data-stu-id="8956e-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8956e-113">Эта команда создает базу данных реплики для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="8956e-114">Пример 3: создание базы данных реплики для MariaDB</span><span class="sxs-lookup"><span data-stu-id="8956e-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8956e-115">Эта команда с параметром InputObject создает базу данных реплики с параметром InputObject для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="8956e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8956e-116">PARAMETERS</span></span>

### <span data-ttu-id="8956e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8956e-117">-AsJob</span></span>
<span data-ttu-id="8956e-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8956e-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8956e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8956e-119">-DefaultProfile</span></span>
<span data-ttu-id="8956e-120">Region DefaultParameters учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8956e-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8956e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8956e-121">-Location</span></span>
<span data-ttu-id="8956e-122">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="8956e-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8956e-123">-Master</span><span class="sxs-lookup"><span data-stu-id="8956e-123">-Master</span></span>
<span data-ttu-id="8956e-124">Исходный объект сервера, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="8956e-124">The source server object to restore from.</span></span>
<span data-ttu-id="8956e-125">Для конструирования ознакомьтесь с разделом "Заметки" ЭТАЛОНных свойств и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8956e-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8956e-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="8956e-126">-MasterName</span></span>
<span data-ttu-id="8956e-127">Имя сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8956e-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="8956e-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="8956e-128">-NoWait</span></span>
<span data-ttu-id="8956e-129">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="8956e-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8956e-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="8956e-130">-ReplicaName</span></span>
<span data-ttu-id="8956e-131">Имя реплики.</span><span class="sxs-lookup"><span data-stu-id="8956e-131">Replica name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8956e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8956e-132">-ResourceGroupName</span></span>
<span data-ttu-id="8956e-133">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8956e-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8956e-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="8956e-134">-Sku</span></span>
<span data-ttu-id="8956e-135">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8956e-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8956e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8956e-136">-SubscriptionId</span></span>
<span data-ttu-id="8956e-137">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8956e-137">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8956e-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="8956e-138">-Tag</span></span>
<span data-ttu-id="8956e-139">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="8956e-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8956e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8956e-140">-Confirm</span></span>
<span data-ttu-id="8956e-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8956e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8956e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8956e-142">-WhatIf</span></span>
<span data-ttu-id="8956e-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8956e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8956e-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8956e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8956e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8956e-145">CommonParameters</span></span>
<span data-ttu-id="8956e-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8956e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8956e-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8956e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8956e-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8956e-148">INPUTS</span></span>

### <span data-ttu-id="8956e-149">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="8956e-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8956e-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8956e-150">OUTPUTS</span></span>

### <span data-ttu-id="8956e-151">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="8956e-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8956e-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8956e-152">NOTES</span></span>

<span data-ttu-id="8956e-153">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8956e-153">ALIASES</span></span>

<span data-ttu-id="8956e-154">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8956e-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8956e-155">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8956e-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8956e-156">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8956e-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8956e-157">ОБРАЗЕЦ <IServer> : исходный объект сервера, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="8956e-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="8956e-158">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="8956e-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="8956e-159">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="8956e-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="8956e-160">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="8956e-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8956e-161">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="8956e-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8956e-162">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="8956e-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8956e-163">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="8956e-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8956e-164">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8956e-165">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="8956e-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8956e-166">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8956e-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8956e-167">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="8956e-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8956e-168">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="8956e-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8956e-169">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8956e-170">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8956e-171">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="8956e-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8956e-172">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8956e-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8956e-173">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8956e-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8956e-174">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="8956e-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8956e-175">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="8956e-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8956e-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8956e-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8956e-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="8956e-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8956e-179">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8956e-180">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8956e-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8956e-181">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="8956e-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8956e-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8956e-182">RELATED LINKS</span></span>

