---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0334f022266843290f56fa8ee635634bce7caa56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974307"
---
# <span data-ttu-id="2ac8d-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ac8d-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="2ac8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac8d-103">Получает резервную копию краткого срока хранения.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="2ac8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ac8d-104">SYNTAX</span></span>

### <span data-ttu-id="2ac8d-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ac8d-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac8d-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac8d-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac8d-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ac8d-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac8d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac8d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac8d-109">Для этой базы данных зарегистрируется **краткое** политика хранения, зарегистрированная для этой базы данных, с ее учетом.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="2ac8d-110">Политика — это период хранения в днях для восстановления резервных копий за данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="2ac8d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ac8d-111">EXAMPLES</span></span>

### <span data-ttu-id="2ac8d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ac8d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="2ac8d-113">Эта команда получает краткое срок политики хранения для базы данных01.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="2ac8d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2ac8d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="2ac8d-115">Эта команда получает краткое сроки политики хранения для базы данных01 путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="2ac8d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2ac8d-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="2ac8d-117">Эта команда получает краткое срок политики хранения для всех удаленных баз данных, которые называются database01, путем перенагрывки в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="2ac8d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac8d-118">PARAMETERS</span></span>

### <span data-ttu-id="2ac8d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ac8d-119">-DatabaseName</span></span>
<span data-ttu-id="2ac8d-120">Имя базы данных экземпляра Azure SQL Azure, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac8d-121">-DefaultProfile</span></span>
<span data-ttu-id="2ac8d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac8d-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="2ac8d-123">-DeletionDate</span></span>
<span data-ttu-id="2ac8d-124">Дата удаления базы данных экземпляра Azure SQL для получения резервных копий с точностью в миллисекунд (например, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="2ac8d-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac8d-125">-InputObject</span></span>
<span data-ttu-id="2ac8d-126">Live или deleted database object to get/set the policy for.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2ac8d-127">-InstanceName</span></span>
<span data-ttu-id="2ac8d-128">Имя управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac8d-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ac8d-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac8d-131">-ResourceId</span></span>
<span data-ttu-id="2ac8d-132">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac8d-133">CommonParameters</span></span>
<span data-ttu-id="2ac8d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac8d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ac8d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac8d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac8d-136">INPUTS</span></span>

### <span data-ttu-id="2ac8d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2ac8d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="2ac8d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac8d-138">System.String</span></span>

## <span data-ttu-id="2ac8d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac8d-139">OUTPUTS</span></span>

### <span data-ttu-id="2ac8d-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2ac8d-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="2ac8d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ac8d-141">NOTES</span></span>

## <span data-ttu-id="2ac8d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ac8d-142">RELATED LINKS</span></span>
