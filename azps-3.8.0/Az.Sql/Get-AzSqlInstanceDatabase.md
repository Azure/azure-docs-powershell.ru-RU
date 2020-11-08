---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074287"
---
# <span data-ttu-id="ed7c2-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ed7c2-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="ed7c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7c2-103">Возвращает сведения об управляемой базе данных экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="ed7c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed7c2-104">SYNTAX</span></span>

### <span data-ttu-id="ed7c2-105">GetInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed7c2-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7c2-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ed7c2-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7c2-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="ed7c2-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed7c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ed7c2-109">Командлет **Get-AzSqlInstanceDatabase** получает одну или несколько баз данных SQL Azure из управляемого экземпляра базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ed7c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed7c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ed7c2-111">Пример 1: получение всех баз данных в экземпляре</span><span class="sxs-lookup"><span data-stu-id="ed7c2-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="ed7c2-112">Эта команда получает все базы данных на экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="ed7c2-113">Пример 2: получение базы данных по имени на управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="ed7c2-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="ed7c2-114">Эта команда получает базу данных с именем managedDatabase1 из экземпляра с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="ed7c2-115">Пример 3: получение всех баз данных на экземпляре с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="ed7c2-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="ed7c2-116">Эта команда получает все базы данных на экземпляре с именем managedInstance1, который начинается с "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="ed7c2-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="ed7c2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed7c2-117">PARAMETERS</span></span>

### <span data-ttu-id="ed7c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7c2-118">-DefaultProfile</span></span>
<span data-ttu-id="ed7c2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed7c2-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ed7c2-120">-InstanceName</span></span>
<span data-ttu-id="ed7c2-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-121">The instance name.</span></span>

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

### <span data-ttu-id="ed7c2-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="ed7c2-122">-InstanceObject</span></span>
<span data-ttu-id="ed7c2-123">Объект экземпляра, используемый для считывания базы данных экземпляра</span><span class="sxs-lookup"><span data-stu-id="ed7c2-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="ed7c2-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="ed7c2-124">-InstanceResourceId</span></span>
<span data-ttu-id="ed7c2-125">Идентификатор ресурса объекта экземпляра, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="ed7c2-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed7c2-126">-Name</span></span>
<span data-ttu-id="ed7c2-127">Имя базы данных экземпляра Azure SQL для извлечения.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="ed7c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed7c2-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed7c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7c2-130">CommonParameters</span></span>
<span data-ttu-id="ed7c2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed7c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7c2-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed7c2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7c2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed7c2-133">INPUTS</span></span>

### <span data-ttu-id="ed7c2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed7c2-134">System.String</span></span>

### <span data-ttu-id="ed7c2-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ed7c2-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ed7c2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed7c2-136">OUTPUTS</span></span>

### <span data-ttu-id="ed7c2-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ed7c2-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ed7c2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed7c2-138">NOTES</span></span>

## <span data-ttu-id="ed7c2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed7c2-139">RELATED LINKS</span></span>
