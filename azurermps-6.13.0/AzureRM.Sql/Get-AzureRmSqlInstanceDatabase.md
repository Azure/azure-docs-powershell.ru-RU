---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563967"
---
# <span data-ttu-id="a13da-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a13da-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="a13da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a13da-102">SYNOPSIS</span></span>
<span data-ttu-id="a13da-103">Возвращает сведения об управляемой базе данных экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a13da-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a13da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a13da-104">SYNTAX</span></span>

### <span data-ttu-id="a13da-105">GetInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a13da-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a13da-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a13da-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a13da-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="a13da-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a13da-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a13da-108">DESCRIPTION</span></span>
<span data-ttu-id="a13da-109">Командлет **Get-AzureRmSqlInstanceDatabase** получает одну или несколько баз данных SQL Azure из управляемого экземпляра базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a13da-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a13da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a13da-110">EXAMPLES</span></span>

### <span data-ttu-id="a13da-111">Пример 1: получение всех баз данных в экземпляре</span><span class="sxs-lookup"><span data-stu-id="a13da-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="a13da-112">Эта команда получает все базы данных на экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a13da-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="a13da-113">Пример 2: получение базы данных по имени на управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="a13da-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="a13da-114">Эта команда получает базу данных с именем managedDatabase1 из экземпляра с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a13da-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="a13da-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a13da-115">PARAMETERS</span></span>

### <span data-ttu-id="a13da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13da-116">-DefaultProfile</span></span>
<span data-ttu-id="a13da-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a13da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a13da-118">-InstanceName</span></span>
<span data-ttu-id="a13da-119">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a13da-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="a13da-120">-InstanceObject</span></span>
<span data-ttu-id="a13da-121">Объект экземпляра, используемый для считывания базы данных экземпляра</span><span class="sxs-lookup"><span data-stu-id="a13da-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a13da-122">-InstanceResourceId</span></span>
<span data-ttu-id="a13da-123">Идентификатор ресурса объекта экземпляра, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a13da-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a13da-124">-Name</span></span>
<span data-ttu-id="a13da-125">Имя базы данных экземпляра Azure SQL для извлечения.</span><span class="sxs-lookup"><span data-stu-id="a13da-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a13da-126">-ResourceGroupName</span></span>
<span data-ttu-id="a13da-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a13da-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a13da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13da-128">CommonParameters</span></span>
<span data-ttu-id="a13da-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a13da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13da-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a13da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13da-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a13da-131">INPUTS</span></span>

### <span data-ttu-id="a13da-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a13da-132">System.String</span></span>
<span data-ttu-id="a13da-133">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a13da-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a13da-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a13da-134">OUTPUTS</span></span>

### <span data-ttu-id="a13da-135">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a13da-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a13da-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a13da-136">NOTES</span></span>

## <span data-ttu-id="a13da-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a13da-137">RELATED LINKS</span></span>
