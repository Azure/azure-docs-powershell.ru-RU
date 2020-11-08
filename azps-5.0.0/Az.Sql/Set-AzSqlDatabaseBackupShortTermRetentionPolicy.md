---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248799"
---
# <span data-ttu-id="fbcd9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fbcd9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="fbcd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbcd9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcd9-103">Настройка политики хранения для архивации по короткому критерию.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="fbcd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbcd9-104">SYNTAX</span></span>

### <span data-ttu-id="fbcd9-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbcd9-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcd9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fbcd9-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcd9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fbcd9-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcd9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbcd9-108">DESCRIPTION</span></span>
<span data-ttu-id="fbcd9-109">Командлет **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** получает краткосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="fbcd9-110">Политика — срок хранения (в днях) для резервного копирования на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="fbcd9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbcd9-111">EXAMPLES</span></span>

### <span data-ttu-id="fbcd9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbcd9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="fbcd9-113">Эта команда устанавливает краткосрочную политику хранения для Database01 в 35 дней.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="fbcd9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fbcd9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="fbcd9-115">Эта команда задает краткосрочную политику хранения для Database01 в 35 дней с помощью трубопроводов в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="fbcd9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbcd9-116">PARAMETERS</span></span>

### <span data-ttu-id="fbcd9-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fbcd9-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="fbcd9-118">Объект базы данных, для которого требуется получить политику.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="fbcd9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbcd9-119">-DatabaseName</span></span>
<span data-ttu-id="fbcd9-120">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="fbcd9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcd9-121">-DefaultProfile</span></span>
<span data-ttu-id="fbcd9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbcd9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbcd9-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbcd9-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbcd9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbcd9-125">-ResourceId</span></span>
<span data-ttu-id="fbcd9-126">Краткосрочный идентификатор ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="fbcd9-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="fbcd9-127">-RetentionDays</span></span>
<span data-ttu-id="fbcd9-128">Параметр хранения резервных копий в днях.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="fbcd9-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fbcd9-129">-ServerName</span></span>
<span data-ttu-id="fbcd9-130">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="fbcd9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbcd9-131">-Confirm</span></span>
<span data-ttu-id="fbcd9-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcd9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcd9-133">-WhatIf</span></span>
<span data-ttu-id="fbcd9-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbcd9-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbcd9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcd9-136">CommonParameters</span></span>
<span data-ttu-id="fbcd9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbcd9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcd9-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbcd9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcd9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbcd9-139">INPUTS</span></span>

### <span data-ttu-id="fbcd9-140">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fbcd9-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="fbcd9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fbcd9-141">System.String</span></span>

## <span data-ttu-id="fbcd9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbcd9-142">OUTPUTS</span></span>

### <span data-ttu-id="fbcd9-143">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fbcd9-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="fbcd9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbcd9-144">NOTES</span></span>

## <span data-ttu-id="fbcd9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbcd9-145">RELATED LINKS</span></span>
