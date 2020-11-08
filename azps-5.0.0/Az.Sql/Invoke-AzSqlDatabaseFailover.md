---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245661"
---
# <span data-ttu-id="5ad1f-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="5ad1f-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="5ad1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ad1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad1f-103">Отработка отказа базы данных.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-103">Failovers a database.</span></span>

## <span data-ttu-id="5ad1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ad1f-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad1f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad1f-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad1f-106">Командлет Invoke-AzSqlDatabaseFailover отработка отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="5ad1f-107">Если база данных находится в пуле эластичных БД, эта команда будет отпустить указанную базу данных, не затрагивая другие базы данных в том же пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="5ad1f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ad1f-108">EXAMPLES</span></span>

### <span data-ttu-id="5ad1f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ad1f-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5ad1f-110">Эта команда будет отработка отказа основной реплики базы данных с именем "Database01" на сервере с именем "Server01"</span><span class="sxs-lookup"><span data-stu-id="5ad1f-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="5ad1f-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5ad1f-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="5ad1f-112">Эта команда отменяет отработку отказа для считывания вторичной реплики базы данных с именем "Database01" на сервере с именем "Server01"</span><span class="sxs-lookup"><span data-stu-id="5ad1f-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="5ad1f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ad1f-113">PARAMETERS</span></span>

### <span data-ttu-id="5ad1f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ad1f-114">-AsJob</span></span>
<span data-ttu-id="5ad1f-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ad1f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ad1f-116">-DatabaseName</span></span>
<span data-ttu-id="5ad1f-117">Имя базы данных SQL Azure для перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad1f-118">-DefaultProfile</span></span>
<span data-ttu-id="5ad1f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5ad1f-120">-Force</span></span>
<span data-ttu-id="5ad1f-121">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="5ad1f-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ad1f-122">-PassThru</span></span>
<span data-ttu-id="5ad1f-123">При успешном выполнении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="5ad1f-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="5ad1f-125">-ReadableSecondary</span></span>
<span data-ttu-id="5ad1f-126">Отработка отказа для восприятия вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5ad1f-126">Failover the readable secondary replica instead of the default primary replica</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ad1f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ad1f-129">-ServerName</span></span>
<span data-ttu-id="5ad1f-130">Имя сервера базы данных SQL Azure, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-130">The name of the Azure SQL Database Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad1f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ad1f-131">-Confirm</span></span>
<span data-ttu-id="5ad1f-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ad1f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad1f-133">-WhatIf</span></span>
<span data-ttu-id="5ad1f-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ad1f-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ad1f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad1f-136">CommonParameters</span></span>
<span data-ttu-id="5ad1f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ad1f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad1f-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ad1f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad1f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ad1f-139">INPUTS</span></span>

### <span data-ttu-id="5ad1f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5ad1f-140">System.String</span></span>

## <span data-ttu-id="5ad1f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad1f-141">OUTPUTS</span></span>

## <span data-ttu-id="5ad1f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ad1f-142">NOTES</span></span>

## <span data-ttu-id="5ad1f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ad1f-143">RELATED LINKS</span></span>

[<span data-ttu-id="5ad1f-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="5ad1f-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="5ad1f-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-148">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-150">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ad1f-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5ad1f-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5ad1f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
