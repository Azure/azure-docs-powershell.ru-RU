---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250093"
---
# <span data-ttu-id="fa213-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="fa213-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="fa213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa213-102">SYNOPSIS</span></span>
<span data-ttu-id="fa213-103">Восстановление MariaDB из существующей MariaDB.</span><span class="sxs-lookup"><span data-stu-id="fa213-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="fa213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa213-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa213-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa213-105">DESCRIPTION</span></span>
<span data-ttu-id="fa213-106">Восстановление MariaDB из существующей MariaDB.</span><span class="sxs-lookup"><span data-stu-id="fa213-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="fa213-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa213-107">EXAMPLES</span></span>

### <span data-ttu-id="fa213-108">Пример 1: восстановление PointInTime MariaDB по имени сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fa213-109">Эта команда восстанавливает PointInTime MariaDB по имени сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="fa213-110">Пример 2: восстановление PointInTime MariaDB по объекту сервера</span><span class="sxs-lookup"><span data-stu-id="fa213-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fa213-111">Эта команда восстанавливает объект PointInTime MariaDB по объекту сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="fa213-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa213-112">PARAMETERS</span></span>

### <span data-ttu-id="fa213-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa213-113">-AsJob</span></span>
<span data-ttu-id="fa213-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fa213-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fa213-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa213-115">-DefaultProfile</span></span>
<span data-ttu-id="fa213-116">Region DefaultParameters учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa213-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa213-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa213-117">-InputObject</span></span>
<span data-ttu-id="fa213-118">Исходный объект сервера, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="fa213-118">The source server object to restore from.</span></span>
<span data-ttu-id="fa213-119">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fa213-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa213-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fa213-120">-Location</span></span>
<span data-ttu-id="fa213-121">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="fa213-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="fa213-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa213-122">-Name</span></span>
<span data-ttu-id="fa213-123">Имя сервера, с которого будет восстанавливаться конечный сервер.</span><span class="sxs-lookup"><span data-stu-id="fa213-123">The dest server name to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa213-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="fa213-124">-NoWait</span></span>
<span data-ttu-id="fa213-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="fa213-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa213-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa213-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa213-127">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="fa213-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fa213-128">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fa213-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fa213-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="fa213-129">-RestorePointInTime</span></span>
<span data-ttu-id="fa213-130">Region (регион) PointInTimeRestore расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="fa213-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa213-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fa213-131">-ServerName</span></span>
<span data-ttu-id="fa213-132">Имя исходного сервера, с которого нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="fa213-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="fa213-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa213-133">-SubscriptionId</span></span>
<span data-ttu-id="fa213-134">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa213-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa213-135">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fa213-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fa213-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="fa213-136">-Tag</span></span>
<span data-ttu-id="fa213-137">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="fa213-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="fa213-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa213-138">-Confirm</span></span>
<span data-ttu-id="fa213-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa213-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa213-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa213-140">-WhatIf</span></span>
<span data-ttu-id="fa213-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa213-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa213-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa213-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa213-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa213-143">CommonParameters</span></span>
<span data-ttu-id="fa213-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa213-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa213-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa213-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa213-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa213-146">INPUTS</span></span>

### <span data-ttu-id="fa213-147">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="fa213-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="fa213-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa213-148">OUTPUTS</span></span>

### <span data-ttu-id="fa213-149">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="fa213-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="fa213-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa213-150">NOTES</span></span>

<span data-ttu-id="fa213-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fa213-151">ALIASES</span></span>

<span data-ttu-id="fa213-152">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fa213-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa213-153">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fa213-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa213-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa213-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa213-155">INPUTOBJECT <IServer> : исходный серверный объект для восстановления.</span><span class="sxs-lookup"><span data-stu-id="fa213-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="fa213-156">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="fa213-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="fa213-157">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="fa213-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="fa213-158">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fa213-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fa213-159">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="fa213-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="fa213-160">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="fa213-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="fa213-161">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="fa213-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="fa213-162">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="fa213-163">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="fa213-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="fa213-164">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa213-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="fa213-165">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="fa213-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="fa213-166">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="fa213-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="fa213-167">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="fa213-168">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="fa213-169">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="fa213-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="fa213-170">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="fa213-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="fa213-171">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fa213-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="fa213-172">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="fa213-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="fa213-173">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="fa213-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="fa213-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="fa213-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="fa213-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="fa213-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="fa213-177">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="fa213-178">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa213-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="fa213-179">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="fa213-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="fa213-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa213-180">RELATED LINKS</span></span>

