---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243481"
---
# <span data-ttu-id="bea87-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="bea87-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="bea87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bea87-102">SYNOPSIS</span></span>
<span data-ttu-id="bea87-103">Получение строки подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bea87-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bea87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bea87-104">SYNTAX</span></span>

### <span data-ttu-id="bea87-105">Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bea87-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bea87-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bea87-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bea87-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bea87-107">DESCRIPTION</span></span>
<span data-ttu-id="bea87-108">Получение строки подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bea87-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bea87-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bea87-109">EXAMPLES</span></span>

### <span data-ttu-id="bea87-110">Пример 1: получение строки подключения сервера MySql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="bea87-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="bea87-111">Этот командлет получает строку подключения сервера MySql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="bea87-112">Пример 2: получение строки подключения сервера MySql по удостоверению</span><span class="sxs-lookup"><span data-stu-id="bea87-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="bea87-113">Этот командлет получает строку подключения сервера MySql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="bea87-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="bea87-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bea87-114">PARAMETERS</span></span>

### <span data-ttu-id="bea87-115">-Клиент</span><span class="sxs-lookup"><span data-stu-id="bea87-115">-Client</span></span>
<span data-ttu-id="bea87-116">Поставщик клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bea87-116">Client connection provider.</span></span>

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

### <span data-ttu-id="bea87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea87-117">-DefaultProfile</span></span>
<span data-ttu-id="bea87-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bea87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bea87-119">-InputObject</span></span>
<span data-ttu-id="bea87-120">Исходный объект сервера, из которого создается реплика.</span><span class="sxs-lookup"><span data-stu-id="bea87-120">The source server object to create replica from.</span></span>
<span data-ttu-id="bea87-121">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="bea87-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bea87-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bea87-122">-Name</span></span>
<span data-ttu-id="bea87-123">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea87-124">-ResourceGroupName</span></span>
<span data-ttu-id="bea87-125">Имя группы ресурсов, содержащей ресурс, это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="bea87-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea87-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bea87-126">-SubscriptionId</span></span>
<span data-ttu-id="bea87-127">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="bea87-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea87-128">CommonParameters</span></span>
<span data-ttu-id="bea87-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bea87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea87-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bea87-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea87-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bea87-131">INPUTS</span></span>

### <span data-ttu-id="bea87-132">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="bea87-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bea87-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bea87-133">OUTPUTS</span></span>

### <span data-ttu-id="bea87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bea87-134">System.String</span></span>

## <span data-ttu-id="bea87-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bea87-135">NOTES</span></span>

<span data-ttu-id="bea87-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="bea87-136">ALIASES</span></span>

<span data-ttu-id="bea87-137">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bea87-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bea87-138">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bea87-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bea87-139">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bea87-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bea87-140">INPUTOBJECT <IServer> : исходный серверный объект для создания реплики.</span><span class="sxs-lookup"><span data-stu-id="bea87-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="bea87-141">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="bea87-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="bea87-142">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="bea87-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="bea87-143">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="bea87-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bea87-144">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="bea87-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bea87-145">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="bea87-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bea87-146">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="bea87-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bea87-147">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bea87-148">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="bea87-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bea87-149">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="bea87-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bea87-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Состояние, показывающее, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bea87-151">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="bea87-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bea87-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Принудительная минимальная версия TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bea87-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Разрешены ли доступ к общедоступной сети для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bea87-154">Значение не является обязательным, но если оно передано, должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="bea87-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bea87-155">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="bea87-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bea87-156">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bea87-157">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bea87-158">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="bea87-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bea87-159">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bea87-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bea87-160">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="bea87-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bea87-161">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="bea87-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bea87-162">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="bea87-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bea87-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bea87-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bea87-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="bea87-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bea87-166">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bea87-167">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="bea87-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bea87-168">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="bea87-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bea87-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bea87-169">RELATED LINKS</span></span>

