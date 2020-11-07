---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906613"
---
# <span data-ttu-id="882fd-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="882fd-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="882fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="882fd-102">SYNOPSIS</span></span>
<span data-ttu-id="882fd-103">Отработка отказа базы данных.</span><span class="sxs-lookup"><span data-stu-id="882fd-103">Failovers a database.</span></span>

## <span data-ttu-id="882fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="882fd-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="882fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="882fd-105">DESCRIPTION</span></span>
<span data-ttu-id="882fd-106">Командлет Invoke-AzSqlDatabaseFailover отработка отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="882fd-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="882fd-107">Если база данных находится в пуле эластичных БД, эта команда будет отпустить указанную базу данных, не затрагивая другие базы данных в том же пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="882fd-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="882fd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="882fd-108">EXAMPLES</span></span>

### <span data-ttu-id="882fd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="882fd-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="882fd-110">Эта команда будет отработка отказа базы данных с именем "Database01" на сервере с именем "Server01"</span><span class="sxs-lookup"><span data-stu-id="882fd-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="882fd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="882fd-111">PARAMETERS</span></span>

### <span data-ttu-id="882fd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="882fd-112">-AsJob</span></span>
<span data-ttu-id="882fd-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="882fd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="882fd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="882fd-114">-DatabaseName</span></span>
<span data-ttu-id="882fd-115">Имя базы данных SQL Azure для перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="882fd-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="882fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882fd-116">-DefaultProfile</span></span>
<span data-ttu-id="882fd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="882fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882fd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="882fd-118">-Force</span></span>
<span data-ttu-id="882fd-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="882fd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="882fd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="882fd-120">-PassThru</span></span>
<span data-ttu-id="882fd-121">При успешном выполнении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="882fd-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="882fd-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="882fd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="882fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="882fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="882fd-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="882fd-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="882fd-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="882fd-125">-ServerName</span></span>
<span data-ttu-id="882fd-126">Имя сервера базы данных SQL Azure, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="882fd-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="882fd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="882fd-127">-Confirm</span></span>
<span data-ttu-id="882fd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="882fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="882fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="882fd-129">-WhatIf</span></span>
<span data-ttu-id="882fd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="882fd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="882fd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="882fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="882fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882fd-132">CommonParameters</span></span>
<span data-ttu-id="882fd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="882fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882fd-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="882fd-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882fd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="882fd-135">INPUTS</span></span>

### <span data-ttu-id="882fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="882fd-136">System.String</span></span>

## <span data-ttu-id="882fd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="882fd-137">OUTPUTS</span></span>

## <span data-ttu-id="882fd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="882fd-138">NOTES</span></span>

## <span data-ttu-id="882fd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="882fd-139">RELATED LINKS</span></span>

[<span data-ttu-id="882fd-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="882fd-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="882fd-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="882fd-142">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="882fd-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="882fd-144">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="882fd-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="882fd-146">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="882fd-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="882fd-147">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="882fd-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
