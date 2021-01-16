---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506672"
---
# <span data-ttu-id="9162e-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9162e-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="9162e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9162e-102">SYNOPSIS</span></span>
<span data-ttu-id="9162e-103">Возвращает сведения о базе данных azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="9162e-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="9162e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9162e-104">SYNTAX</span></span>

### <span data-ttu-id="9162e-105">GetInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9162e-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9162e-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9162e-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9162e-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="9162e-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9162e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9162e-108">DESCRIPTION</span></span>
<span data-ttu-id="9162e-109">Cmdlet **Get-AzSqlInstanceDatabase** получает одну или несколько баз данных Azure SQL из управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9162e-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9162e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9162e-110">EXAMPLES</span></span>

### <span data-ttu-id="9162e-111">Пример 1. Получить все базы данных в экземпляре</span><span class="sxs-lookup"><span data-stu-id="9162e-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="9162e-112">Эта команда получает все базы данных в экземпляре ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="9162e-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="9162e-113">Пример 2. Получить базу данных по имени в управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="9162e-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="9162e-114">Эта команда получает базу данных с именем ManagedDatabase1 из экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="9162e-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="9162e-115">Пример 3. Использование фильтрации для всех баз данных в экземпляре</span><span class="sxs-lookup"><span data-stu-id="9162e-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="9162e-116">Эта команда получает все базы данных из экземпляра ManagedInstance1, которые начинаются с "ManagedDatabase".</span><span class="sxs-lookup"><span data-stu-id="9162e-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="9162e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9162e-117">PARAMETERS</span></span>

### <span data-ttu-id="9162e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9162e-118">-DefaultProfile</span></span>
<span data-ttu-id="9162e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9162e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9162e-120">-InstanceName</span></span>
<span data-ttu-id="9162e-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9162e-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="9162e-122">-InstanceObject</span></span>
<span data-ttu-id="9162e-123">Объект экземпляра, который используется для получения базы данных экземпляра</span><span class="sxs-lookup"><span data-stu-id="9162e-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="9162e-124">-InstanceResourceId</span></span>
<span data-ttu-id="9162e-125">ИД ресурса объекта экземпляра, который требуется получить</span><span class="sxs-lookup"><span data-stu-id="9162e-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9162e-126">-Name</span></span>
<span data-ttu-id="9162e-127">Имя базы данных экземпляра Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9162e-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9162e-128">-ResourceGroupName</span></span>
<span data-ttu-id="9162e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9162e-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9162e-130">CommonParameters</span></span>
<span data-ttu-id="9162e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9162e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9162e-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9162e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9162e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9162e-133">INPUTS</span></span>

### <span data-ttu-id="9162e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9162e-134">System.String</span></span>

### <span data-ttu-id="9162e-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9162e-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9162e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9162e-136">OUTPUTS</span></span>

### <span data-ttu-id="9162e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9162e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9162e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9162e-138">NOTES</span></span>

## <span data-ttu-id="9162e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9162e-139">RELATED LINKS</span></span>
