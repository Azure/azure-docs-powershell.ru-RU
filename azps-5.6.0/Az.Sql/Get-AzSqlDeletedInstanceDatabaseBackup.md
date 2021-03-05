---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: 1d41e42b673eccc692c317f3e9d1d20c5551da4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999672"
---
# <span data-ttu-id="0c9e3-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0c9e3-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="0c9e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9e3-103">Удаляет базу данных, которую можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="0c9e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c9e3-104">SYNTAX</span></span>

### <span data-ttu-id="0c9e3-105">Список deletedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c9e3-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c9e3-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="0c9e3-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c9e3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c9e3-107">DESCRIPTION</span></span>
<span data-ttu-id="0c9e3-108">Для этого можно использовать указанный SQL экземпляра базы данных **Get-AzSqlDeletedInstanceDataBaseBackup** или все удаленные резервные копии, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="0c9e3-109">Этот cmdlet также поддерживается службой SQL Instance Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0c9e3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c9e3-110">EXAMPLES</span></span>

### <span data-ttu-id="0c9e3-111">Пример 1. Все удаленные резервные копии базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="0c9e3-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="0c9e3-112">Эта команда получает все удаленные резервные копии баз данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="0c9e3-113">Пример 2. Получить указанную удаленную резервную копию базы данных</span><span class="sxs-lookup"><span data-stu-id="0c9e3-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="0c9e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-114">PARAMETERS</span></span>

### <span data-ttu-id="0c9e3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c9e3-115">-DatabaseName</span></span>
<span data-ttu-id="0c9e3-116">Имя базы данных экземпляра Azure SQL Azure, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="0c9e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9e3-117">-DefaultProfile</span></span>
<span data-ttu-id="0c9e3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c9e3-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0c9e3-119">-DeletionDate</span></span>
<span data-ttu-id="0c9e3-120">Дата удаления базы данных экземпляра Azure SQL для получения резервных копий с точностью в миллисекунд (например, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="0c9e3-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="0c9e3-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0c9e3-121">-InstanceName</span></span>
<span data-ttu-id="0c9e3-122">Имя управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="0c9e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c9e3-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c9e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9e3-125">CommonParameters</span></span>
<span data-ttu-id="0c9e3-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9e3-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c9e3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9e3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-128">INPUTS</span></span>

### <span data-ttu-id="0c9e3-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0c9e3-129">None</span></span>

## <span data-ttu-id="0c9e3-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-130">OUTPUTS</span></span>

### <span data-ttu-id="0c9e3-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="0c9e3-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="0c9e3-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c9e3-132">NOTES</span></span>

## <span data-ttu-id="0c9e3-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c9e3-133">RELATED LINKS</span></span>
