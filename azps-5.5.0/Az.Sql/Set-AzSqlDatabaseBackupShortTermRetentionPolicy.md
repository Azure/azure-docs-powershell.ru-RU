---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230049"
---
# <span data-ttu-id="a2b12-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a2b12-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="a2b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b12-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b12-103">Задает политику хранения для резервного копирования в течение короткого срока.</span><span class="sxs-lookup"><span data-stu-id="a2b12-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="a2b12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2b12-104">SYNTAX</span></span>

### <span data-ttu-id="a2b12-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2b12-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b12-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2b12-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b12-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2b12-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b12-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2b12-108">DESCRIPTION</span></span>
<span data-ttu-id="a2b12-109">Для этой базы данных зарегистрируется политика хранения, зарегистрированная для этого клиента **Set-AzSqlDatabaseBackupShortTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="a2b12-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="a2b12-110">Политика — это срок хранения резервных копий, которые будут восстанавливаться за несколько дней.</span><span class="sxs-lookup"><span data-stu-id="a2b12-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="a2b12-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2b12-111">EXAMPLES</span></span>

### <span data-ttu-id="a2b12-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2b12-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="a2b12-113">Эта команда задает кратковременную политику хранения для базы данных01, которая составляет 35 дней.</span><span class="sxs-lookup"><span data-stu-id="a2b12-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="a2b12-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2b12-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="a2b12-115">Эта команда задает кратковременную политику хранения для базы данных01 в течение 35 дней путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="a2b12-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="a2b12-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2b12-116">PARAMETERS</span></span>

### <span data-ttu-id="a2b12-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a2b12-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="a2b12-118">Объект базы данных, для который нужно получить политику.</span><span class="sxs-lookup"><span data-stu-id="a2b12-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="a2b12-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2b12-119">-DatabaseName</span></span>
<span data-ttu-id="a2b12-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a2b12-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="a2b12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b12-121">-DefaultProfile</span></span>
<span data-ttu-id="a2b12-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b12-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2b12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b12-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2b12-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2b12-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2b12-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2b12-125">-ResourceId</span></span>
<span data-ttu-id="a2b12-126">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="a2b12-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="a2b12-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a2b12-127">-RetentionDays</span></span>
<span data-ttu-id="a2b12-128">Параметр хранения резервной копии в днях.</span><span class="sxs-lookup"><span data-stu-id="a2b12-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="a2b12-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2b12-129">-ServerName</span></span>
<span data-ttu-id="a2b12-130">Имя службы Azure SQL Server которая находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a2b12-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="a2b12-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2b12-131">-Confirm</span></span>
<span data-ttu-id="a2b12-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b12-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b12-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b12-133">-WhatIf</span></span>
<span data-ttu-id="a2b12-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b12-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b12-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2b12-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b12-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b12-136">CommonParameters</span></span>
<span data-ttu-id="a2b12-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b12-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b12-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2b12-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b12-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2b12-139">INPUTS</span></span>

### <span data-ttu-id="a2b12-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a2b12-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="a2b12-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a2b12-141">System.String</span></span>

## <span data-ttu-id="a2b12-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2b12-142">OUTPUTS</span></span>

### <span data-ttu-id="a2b12-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a2b12-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a2b12-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2b12-144">NOTES</span></span>

## <span data-ttu-id="a2b12-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2b12-145">RELATED LINKS</span></span>
