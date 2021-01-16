---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324158"
---
# <span data-ttu-id="a35f3-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="a35f3-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="a35f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a35f3-103">Получите строку подключения для MariaDB под заданной структурой.</span><span class="sxs-lookup"><span data-stu-id="a35f3-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="a35f3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a35f3-104">SYNTAX</span></span>

### <span data-ttu-id="a35f3-105">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a35f3-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a35f3-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="a35f3-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a35f3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a35f3-107">DESCRIPTION</span></span>
<span data-ttu-id="a35f3-108">Получите строку подключения для MariaDB под заданной структурой.</span><span class="sxs-lookup"><span data-stu-id="a35f3-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="a35f3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a35f3-109">EXAMPLES</span></span>

### <span data-ttu-id="a35f3-110">Пример 1. Получить строку подключения от MariaDB</span><span class="sxs-lookup"><span data-stu-id="a35f3-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="a35f3-111">Эта команда получает строку подключения MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a35f3-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="a35f3-112">Пример 2. Получить строку подключения для MariaDB</span><span class="sxs-lookup"><span data-stu-id="a35f3-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="a35f3-113">Эта команда получает строку подключения MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a35f3-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="a35f3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35f3-114">PARAMETERS</span></span>

### <span data-ttu-id="a35f3-115">-Client</span><span class="sxs-lookup"><span data-stu-id="a35f3-115">-Client</span></span>
<span data-ttu-id="a35f3-116">Подключение типа клиента</span><span class="sxs-lookup"><span data-stu-id="a35f3-116">Connect client type</span></span>

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

### <span data-ttu-id="a35f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35f3-117">-DefaultProfile</span></span>
<span data-ttu-id="a35f3-118">Region DefaultParameters— учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a35f3-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a35f3-119">-InputObject</span></span>
<span data-ttu-id="a35f3-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a35f3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a35f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a35f3-121">-Name</span></span>
<span data-ttu-id="a35f3-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-122">The name of the server.</span></span>

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

### <span data-ttu-id="a35f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a35f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="a35f3-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="a35f3-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="a35f3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a35f3-125">-SubscriptionId</span></span>
<span data-ttu-id="a35f3-126">ИД подписки является частью URI для каждого звонка в службу.</span><span class="sxs-lookup"><span data-stu-id="a35f3-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="a35f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35f3-127">CommonParameters</span></span>
<span data-ttu-id="a35f3-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35f3-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a35f3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35f3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a35f3-130">INPUTS</span></span>

### <span data-ttu-id="a35f3-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="a35f3-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="a35f3-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a35f3-132">OUTPUTS</span></span>

### <span data-ttu-id="a35f3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a35f3-133">System.String</span></span>

## <span data-ttu-id="a35f3-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a35f3-134">NOTES</span></span>

<span data-ttu-id="a35f3-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a35f3-135">ALIASES</span></span>

<span data-ttu-id="a35f3-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a35f3-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a35f3-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a35f3-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a35f3-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a35f3-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a35f3-139">INPUTOBJECT <IServer> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a35f3-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="a35f3-140">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a35f3-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="a35f3-141">`[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="a35f3-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="a35f3-142">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="a35f3-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a35f3-143">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="a35f3-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="a35f3-144">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="a35f3-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="a35f3-145">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="a35f3-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="a35f3-146">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="a35f3-147">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a35f3-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="a35f3-148">Задайте для этого назначения ресурсу systemAssigned, чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a35f3-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="a35f3-149">`[MasterServerId <String>]`: он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="a35f3-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="a35f3-150">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этот сервер.</span><span class="sxs-lookup"><span data-stu-id="a35f3-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="a35f3-151">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="a35f3-152">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="a35f3-153">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="a35f3-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="a35f3-154">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a35f3-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="a35f3-155">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a35f3-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="a35f3-156">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="a35f3-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="a35f3-157">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="a35f3-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="a35f3-158">`[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.</span><span class="sxs-lookup"><span data-stu-id="a35f3-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="a35f3-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="a35f3-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="a35f3-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="a35f3-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="a35f3-161">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="a35f3-162">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="a35f3-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="a35f3-163">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="a35f3-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="a35f3-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a35f3-164">RELATED LINKS</span></span>
