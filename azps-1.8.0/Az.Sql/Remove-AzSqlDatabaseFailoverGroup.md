---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 93b20d240e2115fb6522032c13d6d116f3db55aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728860"
---
# <span data-ttu-id="76d89-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="76d89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76d89-102">SYNOPSIS</span></span>
<span data-ttu-id="76d89-103">Удаляет группу отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="76d89-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="76d89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76d89-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76d89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76d89-105">DESCRIPTION</span></span>
<span data-ttu-id="76d89-106">Эта команда удаляет группу отработки отказа с указанным именем, оставляя все базы данных и связи репликации неизменными.</span><span class="sxs-lookup"><span data-stu-id="76d89-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="76d89-107">Конечная точка прослушивателя будет отменена из DNS.</span><span class="sxs-lookup"><span data-stu-id="76d89-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="76d89-108">Для выполнения команды следует использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="76d89-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="76d89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76d89-109">EXAMPLES</span></span>

### <span data-ttu-id="76d89-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76d89-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="76d89-111">Удаление группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="76d89-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="76d89-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76d89-112">PARAMETERS</span></span>

### <span data-ttu-id="76d89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d89-113">-DefaultProfile</span></span>
<span data-ttu-id="76d89-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76d89-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76d89-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="76d89-115">-FailoverGroupName</span></span>
<span data-ttu-id="76d89-116">Имя удаляемой группы отработки отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="76d89-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d89-117">-Force</span><span class="sxs-lookup"><span data-stu-id="76d89-117">-Force</span></span>
<span data-ttu-id="76d89-118">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="76d89-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d89-119">-ResourceGroupName</span></span>
<span data-ttu-id="76d89-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76d89-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="76d89-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="76d89-121">-ServerName</span></span>
<span data-ttu-id="76d89-122">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="76d89-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="76d89-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76d89-123">-Confirm</span></span>
<span data-ttu-id="76d89-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76d89-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d89-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d89-125">-WhatIf</span></span>
<span data-ttu-id="76d89-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76d89-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d89-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76d89-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d89-128">CommonParameters</span></span>
<span data-ttu-id="76d89-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76d89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d89-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76d89-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d89-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76d89-131">INPUTS</span></span>

### <span data-ttu-id="76d89-132">System. String</span><span class="sxs-lookup"><span data-stu-id="76d89-132">System.String</span></span>

## <span data-ttu-id="76d89-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76d89-133">OUTPUTS</span></span>

### <span data-ttu-id="76d89-134">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="76d89-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="76d89-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="76d89-135">NOTES</span></span>

## <span data-ttu-id="76d89-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76d89-136">RELATED LINKS</span></span>

[<span data-ttu-id="76d89-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="76d89-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="76d89-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="76d89-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="76d89-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="76d89-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="76d89-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="76d89-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="76d89-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
