---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407108"
---
# <span data-ttu-id="bf629-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="bf629-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="bf629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf629-102">SYNOPSIS</span></span>
<span data-ttu-id="bf629-103">Возвращает сведения о том, SQL базе данных управляемого экземпляра Azure является избыточным резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="bf629-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="bf629-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf629-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf629-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf629-105">DESCRIPTION</span></span>
<span data-ttu-id="bf629-106">Для **этого** с его SQL azure получаются избыточные резервные копии из экземпляра, управляемого базой данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bf629-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="bf629-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf629-107">EXAMPLES</span></span>

### <span data-ttu-id="bf629-108">Пример 1. Получить в экземпляре все избыточные резервные копии базы данных</span><span class="sxs-lookup"><span data-stu-id="bf629-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="bf629-109">Эта команда получает все избыточные резервные копии базы данных для экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="bf629-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="bf629-110">Пример 2. Резервное копирование избыточной базы данных по имени в управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="bf629-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="bf629-111">Эта команда получает избыточное резервное копирование базы данных с именем ManagedDatabase1 из экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="bf629-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="bf629-112">Пример 3. Получите все избыточные резервные копии базы данных в экземпляре с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="bf629-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="bf629-113">Эта команда получает все избыточные резервные копии базы данных в экземпляре ManagedInstance1, которые начинаются с "ManagedDatabase".</span><span class="sxs-lookup"><span data-stu-id="bf629-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="bf629-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf629-114">PARAMETERS</span></span>

### <span data-ttu-id="bf629-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf629-115">-DefaultProfile</span></span>
<span data-ttu-id="bf629-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf629-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf629-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bf629-117">-InstanceName</span></span>
<span data-ttu-id="bf629-118">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bf629-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf629-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bf629-119">-Name</span></span>
<span data-ttu-id="bf629-120">Имя базы данных экземпляра, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="bf629-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf629-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf629-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf629-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf629-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf629-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf629-123">CommonParameters</span></span>
<span data-ttu-id="bf629-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf629-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf629-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf629-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf629-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf629-126">INPUTS</span></span>

### <span data-ttu-id="bf629-127">Нет</span><span class="sxs-lookup"><span data-stu-id="bf629-127">None</span></span>

## <span data-ttu-id="bf629-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf629-128">OUTPUTS</span></span>

### <span data-ttu-id="bf629-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bf629-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="bf629-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf629-130">NOTES</span></span>

## <span data-ttu-id="bf629-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf629-131">RELATED LINKS</span></span>
