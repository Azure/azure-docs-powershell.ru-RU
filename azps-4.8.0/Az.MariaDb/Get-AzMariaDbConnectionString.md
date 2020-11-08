---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079558"
---
# <span data-ttu-id="a5b4e-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="a5b4e-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="a5b4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b4e-103">Получение строки подключения для MariaDB в данной среде.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="a5b4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5b4e-104">SYNTAX</span></span>

### <span data-ttu-id="a5b4e-105">ServerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5b4e-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5b4e-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="a5b4e-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b4e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-107">DESCRIPTION</span></span>
<span data-ttu-id="a5b4e-108">Получение строки подключения для MariaDB в данной среде.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="a5b4e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b4e-110">Пример 1: получение строки подключения для MariaDB</span><span class="sxs-lookup"><span data-stu-id="a5b4e-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="a5b4e-111">Эта команда получает строку подключения для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="a5b4e-112">Пример 2: получение строки подключения для MariaDB</span><span class="sxs-lookup"><span data-stu-id="a5b4e-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="a5b4e-113">Эта команда получает строку подключения для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="a5b4e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b4e-115">-Клиент</span><span class="sxs-lookup"><span data-stu-id="a5b4e-115">-Client</span></span>
<span data-ttu-id="a5b4e-116">Тип клиента подключения</span><span class="sxs-lookup"><span data-stu-id="a5b4e-116">Connect client type</span></span>

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

### <span data-ttu-id="a5b4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b4e-117">-DefaultProfile</span></span>
<span data-ttu-id="a5b4e-118">Region DefaultParameters учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b4e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b4e-119">-InputObject</span></span>
<span data-ttu-id="a5b4e-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5b4e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5b4e-121">-Name</span></span>
<span data-ttu-id="a5b4e-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-122">The name of the server.</span></span>

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

### <span data-ttu-id="a5b4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5b4e-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="a5b4e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5b4e-125">-SubscriptionId</span></span>
<span data-ttu-id="a5b4e-126">Идентификатор подписки — это часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="a5b4e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b4e-127">CommonParameters</span></span>
<span data-ttu-id="a5b4e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b4e-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b4e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b4e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5b4e-130">INPUTS</span></span>

### <span data-ttu-id="a5b4e-131">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="a5b4e-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="a5b4e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-132">OUTPUTS</span></span>

### <span data-ttu-id="a5b4e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b4e-133">System.String</span></span>

## <span data-ttu-id="a5b4e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5b4e-134">NOTES</span></span>

<span data-ttu-id="a5b4e-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-135">ALIASES</span></span>

<span data-ttu-id="a5b4e-136">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5b4e-137">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5b4e-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5b4e-139">INPUTOBJECT <IServer> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a5b4e-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="a5b4e-140">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="a5b4e-141">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a5b4e-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="a5b4e-142">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a5b4e-143">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="a5b4e-144">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="a5b4e-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="a5b4e-145">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="a5b4e-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="a5b4e-146">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="a5b4e-147">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="a5b4e-148">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="a5b4e-149">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="a5b4e-150">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="a5b4e-151">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="a5b4e-152">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="a5b4e-153">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="a5b4e-154">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="a5b4e-155">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="a5b4e-156">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="a5b4e-157">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="a5b4e-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="a5b4e-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="a5b4e-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="a5b4e-161">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="a5b4e-162">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="a5b4e-163">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="a5b4e-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b4e-164">RELATED LINKS</span></span>

