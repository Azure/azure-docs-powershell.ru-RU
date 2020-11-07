---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ac63ae50893ec54a2d14431c55229fad71c80c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728799"
---
# <span data-ttu-id="ab518-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab518-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="ab518-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab518-102">SYNOPSIS</span></span>
<span data-ttu-id="ab518-103">Настройка политики хранения для архивации по короткому критерию.</span><span class="sxs-lookup"><span data-stu-id="ab518-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="ab518-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab518-104">SYNTAX</span></span>

### <span data-ttu-id="ab518-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab518-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab518-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab518-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab518-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab518-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab518-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab518-108">DESCRIPTION</span></span>
<span data-ttu-id="ab518-109">Командлет **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** получает краткосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="ab518-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="ab518-110">Политика — срок хранения (в днях) для резервного копирования на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="ab518-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="ab518-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab518-111">EXAMPLES</span></span>

### <span data-ttu-id="ab518-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab518-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="ab518-113">Эта команда устанавливает краткосрочную политику хранения для Database01 в 35 дней.</span><span class="sxs-lookup"><span data-stu-id="ab518-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="ab518-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ab518-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="ab518-115">Эта команда задает краткосрочную политику хранения для Database01 в 35 дней с помощью трубопроводов в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="ab518-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="ab518-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab518-116">PARAMETERS</span></span>

### <span data-ttu-id="ab518-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ab518-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="ab518-118">Объект базы данных, для которого требуется получить политику.</span><span class="sxs-lookup"><span data-stu-id="ab518-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="ab518-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab518-119">-DatabaseName</span></span>
<span data-ttu-id="ab518-120">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="ab518-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="ab518-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab518-121">-DefaultProfile</span></span>
<span data-ttu-id="ab518-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab518-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab518-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab518-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab518-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab518-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab518-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab518-125">-ResourceId</span></span>
<span data-ttu-id="ab518-126">Краткосрочный идентификатор ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="ab518-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="ab518-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="ab518-127">-RetentionDays</span></span>
<span data-ttu-id="ab518-128">Параметр хранения резервных копий в днях.</span><span class="sxs-lookup"><span data-stu-id="ab518-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="ab518-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ab518-129">-ServerName</span></span>
<span data-ttu-id="ab518-130">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="ab518-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="ab518-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab518-131">-Confirm</span></span>
<span data-ttu-id="ab518-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ab518-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab518-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab518-133">-WhatIf</span></span>
<span data-ttu-id="ab518-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ab518-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab518-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab518-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab518-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab518-136">CommonParameters</span></span>
<span data-ttu-id="ab518-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab518-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab518-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab518-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab518-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab518-139">INPUTS</span></span>

### <span data-ttu-id="ab518-140">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ab518-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ab518-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ab518-141">System.String</span></span>

## <span data-ttu-id="ab518-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab518-142">OUTPUTS</span></span>

### <span data-ttu-id="ab518-143">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ab518-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ab518-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab518-144">NOTES</span></span>

## <span data-ttu-id="ab518-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab518-145">RELATED LINKS</span></span>
