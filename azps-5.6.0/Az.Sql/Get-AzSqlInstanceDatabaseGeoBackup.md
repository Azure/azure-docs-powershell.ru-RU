---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999464"
---
# <span data-ttu-id="769ac-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="769ac-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="769ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="769ac-102">SYNOPSIS</span></span>
<span data-ttu-id="769ac-103">Возвращает сведения о том, SQL базе данных управляемого экземпляра Azure является избыточным резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="769ac-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="769ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="769ac-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="769ac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="769ac-105">DESCRIPTION</span></span>
<span data-ttu-id="769ac-106">Для **этого** с его SQL azure получаются избыточные резервные копии из экземпляра, управляемого базой данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="769ac-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="769ac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="769ac-107">EXAMPLES</span></span>

### <span data-ttu-id="769ac-108">Пример 1. Получить в экземпляре все избыточные резервные копии базы данных</span><span class="sxs-lookup"><span data-stu-id="769ac-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="769ac-109">Эта команда получает все избыточные резервные копии базы данных для экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="769ac-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="769ac-110">Пример 2. Резервное копирование избыточной базы данных по имени в управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="769ac-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="769ac-111">Эта команда получает избыточное резервное копирование базы данных с именем ManagedDatabase1 из экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="769ac-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="769ac-112">Пример 3. Получите все избыточные резервные копии базы данных в экземпляре с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="769ac-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="769ac-113">Эта команда получает все избыточные резервные копии базы данных в экземпляре ManagedInstance1, которые начинаются с "ManagedDatabase".</span><span class="sxs-lookup"><span data-stu-id="769ac-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="769ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="769ac-114">PARAMETERS</span></span>

### <span data-ttu-id="769ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769ac-115">-DefaultProfile</span></span>
<span data-ttu-id="769ac-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="769ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="769ac-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="769ac-117">-InstanceName</span></span>
<span data-ttu-id="769ac-118">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="769ac-118">The name of the instance.</span></span>

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

### <span data-ttu-id="769ac-119">-Name</span><span class="sxs-lookup"><span data-stu-id="769ac-119">-Name</span></span>
<span data-ttu-id="769ac-120">Имя базы данных экземпляра, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="769ac-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="769ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="769ac-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="769ac-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="769ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769ac-123">CommonParameters</span></span>
<span data-ttu-id="769ac-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769ac-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="769ac-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769ac-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="769ac-126">INPUTS</span></span>

### <span data-ttu-id="769ac-127">Нет</span><span class="sxs-lookup"><span data-stu-id="769ac-127">None</span></span>

## <span data-ttu-id="769ac-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="769ac-128">OUTPUTS</span></span>

### <span data-ttu-id="769ac-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="769ac-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="769ac-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="769ac-130">NOTES</span></span>

## <span data-ttu-id="769ac-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="769ac-131">RELATED LINKS</span></span>
