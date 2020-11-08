---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243253"
---
# <span data-ttu-id="a21d7-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a21d7-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="a21d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a21d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a21d7-103">Возвращает сведения об избыточной резервной копии базы данных SQL, управляемой с управлением Azure.</span><span class="sxs-lookup"><span data-stu-id="a21d7-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="a21d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a21d7-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a21d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a21d7-106">Командлет **Get-AzSqlInstanceDatabaseGeoBackup** получает из управляемого экземпляра базы данных SQL Azure одно или несколько резервных копий баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a21d7-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a21d7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a21d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a21d7-108">Пример 1: получение всех избыточных резервных копий базы данных на экземпляре</span><span class="sxs-lookup"><span data-stu-id="a21d7-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="a21d7-109">Эта команда получает избыточные резервные копии базы данных на экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a21d7-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="a21d7-110">Пример 2: получение избыточной резервной копии базы данных по имени на управляемом экземпляре</span><span class="sxs-lookup"><span data-stu-id="a21d7-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="a21d7-111">Эта команда получает избыточную резервную копию базы данных с именем managedDatabase1 из экземпляра с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a21d7-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="a21d7-112">Пример 3: получение всех избыточных резервных копий базы данных на экземпляре с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="a21d7-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="a21d7-113">Эта команда получает избыточные резервные копии базы данных на экземпляре с именем managedInstance1, который начинается с "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="a21d7-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="a21d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a21d7-114">PARAMETERS</span></span>

### <span data-ttu-id="a21d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21d7-115">-DefaultProfile</span></span>
<span data-ttu-id="a21d7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a21d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21d7-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a21d7-117">-InstanceName</span></span>
<span data-ttu-id="a21d7-118">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a21d7-118">The name of the instance.</span></span>

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

### <span data-ttu-id="a21d7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a21d7-119">-Name</span></span>
<span data-ttu-id="a21d7-120">Имя извлекаемой базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a21d7-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="a21d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="a21d7-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a21d7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a21d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21d7-123">CommonParameters</span></span>
<span data-ttu-id="a21d7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a21d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21d7-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a21d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21d7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a21d7-126">INPUTS</span></span>

### <span data-ttu-id="a21d7-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="a21d7-127">None</span></span>

## <span data-ttu-id="a21d7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21d7-128">OUTPUTS</span></span>

### <span data-ttu-id="a21d7-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a21d7-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="a21d7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a21d7-130">NOTES</span></span>

## <span data-ttu-id="a21d7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a21d7-131">RELATED LINKS</span></span>
