---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506670"
---
# <span data-ttu-id="c23aa-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c23aa-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="c23aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c23aa-103">Получает резервную копию краткого срока хранения.</span><span class="sxs-lookup"><span data-stu-id="c23aa-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="c23aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c23aa-104">SYNTAX</span></span>

### <span data-ttu-id="c23aa-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c23aa-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c23aa-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c23aa-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c23aa-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c23aa-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c23aa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c23aa-108">DESCRIPTION</span></span>
<span data-ttu-id="c23aa-109">Для этой базы данных с недолгой политикой хранения регистрируется политика хранения **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="c23aa-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="c23aa-110">Политика — это срок хранения резервных копий, которые будут восстанавливаться за несколько дней.</span><span class="sxs-lookup"><span data-stu-id="c23aa-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="c23aa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c23aa-111">EXAMPLES</span></span>

### <span data-ttu-id="c23aa-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c23aa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="c23aa-113">Эта команда получает краткое срок политики хранения для базы данных01.</span><span class="sxs-lookup"><span data-stu-id="c23aa-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="c23aa-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c23aa-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="c23aa-115">Эта команда получает краткое сроки политики хранения для базы данных01 путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="c23aa-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="c23aa-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c23aa-116">Example 3</span></span>
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

<span data-ttu-id="c23aa-117">Эта команда получает краткое сроки политики хранения для всех удаленных баз данных, которые называются database01, с помощью piping в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="c23aa-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="c23aa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23aa-118">PARAMETERS</span></span>

### <span data-ttu-id="c23aa-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c23aa-119">-DatabaseName</span></span>
<span data-ttu-id="c23aa-120">Имя базы данных экземпляра Azure SQL Azure, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="c23aa-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="c23aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23aa-121">-DefaultProfile</span></span>
<span data-ttu-id="c23aa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c23aa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c23aa-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="c23aa-123">-DeletionDate</span></span>
<span data-ttu-id="c23aa-124">Дата удаления базы данных экземпляра Azure SQL для получения резервных копий с точностью в миллисекунд (например, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="c23aa-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="c23aa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c23aa-125">-InputObject</span></span>
<span data-ttu-id="c23aa-126">Прямой или удаленный объект базы данных для получения/изменения политики.</span><span class="sxs-lookup"><span data-stu-id="c23aa-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="c23aa-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c23aa-127">-InstanceName</span></span>
<span data-ttu-id="c23aa-128">Имя управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c23aa-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="c23aa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c23aa-129">-ResourceGroupName</span></span>
<span data-ttu-id="c23aa-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c23aa-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c23aa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c23aa-131">-ResourceId</span></span>
<span data-ttu-id="c23aa-132">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="c23aa-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="c23aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23aa-133">CommonParameters</span></span>
<span data-ttu-id="c23aa-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23aa-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c23aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23aa-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c23aa-136">INPUTS</span></span>

### <span data-ttu-id="c23aa-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c23aa-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="c23aa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c23aa-138">System.String</span></span>

## <span data-ttu-id="c23aa-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c23aa-139">OUTPUTS</span></span>

### <span data-ttu-id="c23aa-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c23aa-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c23aa-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c23aa-141">NOTES</span></span>

## <span data-ttu-id="c23aa-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c23aa-142">RELATED LINKS</span></span>
