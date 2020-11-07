---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: ce68b8c8a03fbfe99adbb6070df072dd8ebb0cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728995"
---
# <span data-ttu-id="828a4-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="828a4-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="828a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="828a4-102">SYNOPSIS</span></span>
<span data-ttu-id="828a4-103">Получает удаленную базу данных, которую можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="828a4-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="828a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="828a4-104">SYNTAX</span></span>

### <span data-ttu-id="828a4-105">DeletedDatabaseList (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="828a4-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="828a4-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="828a4-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="828a4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="828a4-107">DESCRIPTION</span></span>
<span data-ttu-id="828a4-108">Командлет **Get-AzSqlDeletedInstanceDatabaseBackup** получает указанную удаленную резервную копию базы данных экземпляра SQL, которую вы можете восстановить, или все удаленные резервные копии, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="828a4-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="828a4-109">Этот командлет также поддерживается службой базы данных Stretch Database (SQL) в Azure.</span><span class="sxs-lookup"><span data-stu-id="828a4-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="828a4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="828a4-110">EXAMPLES</span></span>

### <span data-ttu-id="828a4-111">Пример 1: получение всех удаленных резервных копий базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="828a4-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="828a4-112">Эта команда возвращает все удаленные резервные копии базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="828a4-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="828a4-113">Пример 2: получение указанной удаленной резервной копии базы данных</span><span class="sxs-lookup"><span data-stu-id="828a4-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="828a4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="828a4-114">PARAMETERS</span></span>

### <span data-ttu-id="828a4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="828a4-115">-DatabaseName</span></span>
<span data-ttu-id="828a4-116">Имя базы данных экземпляра Azure SQL, для которой требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="828a4-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828a4-117">-DefaultProfile</span></span>
<span data-ttu-id="828a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="828a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828a4-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="828a4-119">-DeletionDate</span></span>
<span data-ttu-id="828a4-120">Дата удаления базы данных экземпляра Azure SQL, для которой требуется получить резервные копии с точностью до миллисекунд (например, 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="828a4-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="828a4-121">-InstanceName</span></span>
<span data-ttu-id="828a4-122">Имя управляемого экземпляра Azure SQL, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="828a4-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="828a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="828a4-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="828a4-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828a4-125">CommonParameters</span></span>
<span data-ttu-id="828a4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="828a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828a4-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="828a4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828a4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="828a4-128">INPUTS</span></span>

### <span data-ttu-id="828a4-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="828a4-129">None</span></span>

## <span data-ttu-id="828a4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="828a4-130">OUTPUTS</span></span>

### <span data-ttu-id="828a4-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="828a4-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="828a4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="828a4-132">NOTES</span></span>

## <span data-ttu-id="828a4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="828a4-133">RELATED LINKS</span></span>
