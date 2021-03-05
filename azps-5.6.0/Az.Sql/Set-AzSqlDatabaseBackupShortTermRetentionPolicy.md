---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ccdcf55b61b57b54848f3310d7366bb76e0f6805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994955"
---
# <span data-ttu-id="1f248-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f248-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="1f248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f248-102">SYNOPSIS</span></span>
<span data-ttu-id="1f248-103">Задает политику хранения для резервного копирования в течение краткого срока.</span><span class="sxs-lookup"><span data-stu-id="1f248-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="1f248-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f248-104">SYNTAX</span></span>

### <span data-ttu-id="1f248-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f248-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f248-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f248-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f248-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f248-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f248-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f248-108">DESCRIPTION</span></span>
<span data-ttu-id="1f248-109">Для этой базы данных с учетом краткого срока политики хранения зарегистрируется политика хранения **Set-AzSqlDatabaseBackupShortTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="1f248-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="1f248-110">Политика — это период хранения в днях для восстановления резервных копий за данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="1f248-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="1f248-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f248-111">EXAMPLES</span></span>

### <span data-ttu-id="1f248-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f248-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="1f248-113">Эта команда задает кратковременную политику хранения для базы данных01, которая составляет 35 дней.</span><span class="sxs-lookup"><span data-stu-id="1f248-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="1f248-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1f248-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="1f248-115">Эта команда задает кратковременную политику хранения для базы данных01 (35 дней) путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="1f248-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="1f248-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f248-116">PARAMETERS</span></span>

### <span data-ttu-id="1f248-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1f248-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="1f248-118">Объект базы данных, для который нужно получить политику.</span><span class="sxs-lookup"><span data-stu-id="1f248-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f248-119">-DatabaseName</span></span>
<span data-ttu-id="1f248-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1f248-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f248-121">-DefaultProfile</span></span>
<span data-ttu-id="1f248-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f248-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f248-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f248-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f248-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f248-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f248-125">-ResourceId</span></span>
<span data-ttu-id="1f248-126">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="1f248-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="1f248-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="1f248-127">-RetentionDays</span></span>
<span data-ttu-id="1f248-128">Параметр хранения резервной копии в днях.</span><span class="sxs-lookup"><span data-stu-id="1f248-128">The backup retention setting, in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f248-129">-ServerName</span></span>
<span data-ttu-id="1f248-130">Имя azure, SQL Server находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1f248-130">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f248-131">-Confirm</span></span>
<span data-ttu-id="1f248-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1f248-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f248-133">-WhatIf</span></span>
<span data-ttu-id="1f248-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f248-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f248-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f248-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f248-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f248-136">CommonParameters</span></span>
<span data-ttu-id="1f248-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f248-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f248-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f248-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f248-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f248-139">INPUTS</span></span>

### <span data-ttu-id="1f248-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1f248-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="1f248-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1f248-141">System.String</span></span>

## <span data-ttu-id="1f248-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f248-142">OUTPUTS</span></span>

### <span data-ttu-id="1f248-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1f248-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="1f248-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f248-144">NOTES</span></span>

## <span data-ttu-id="1f248-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f248-145">RELATED LINKS</span></span>
