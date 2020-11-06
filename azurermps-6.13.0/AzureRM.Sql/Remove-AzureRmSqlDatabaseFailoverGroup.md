---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 426b44b6c01e40a616d834d2768e5d050a2bc1db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566375"
---
# <span data-ttu-id="083e9-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="083e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="083e9-102">SYNOPSIS</span></span>
<span data-ttu-id="083e9-103">Удаляет группу отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="083e9-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="083e9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="083e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="083e9-105">DESCRIPTION</span></span>
<span data-ttu-id="083e9-106">Эта команда удаляет группу отработки отказа с указанным именем, оставляя все базы данных и связи репликации неизменными.</span><span class="sxs-lookup"><span data-stu-id="083e9-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="083e9-107">Конечная точка прослушивателя будет отменена из DNS.</span><span class="sxs-lookup"><span data-stu-id="083e9-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="083e9-108">Для выполнения команды следует использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="083e9-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="083e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="083e9-109">EXAMPLES</span></span>

### <span data-ttu-id="083e9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="083e9-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="083e9-111">Удаление группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="083e9-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="083e9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="083e9-112">PARAMETERS</span></span>

### <span data-ttu-id="083e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083e9-113">-DefaultProfile</span></span>
<span data-ttu-id="083e9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="083e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083e9-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="083e9-115">-FailoverGroupName</span></span>
<span data-ttu-id="083e9-116">Имя удаляемой группы отработки отказа базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="083e9-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="083e9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="083e9-117">-Force</span></span>
<span data-ttu-id="083e9-118">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="083e9-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="083e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="083e9-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="083e9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="083e9-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="083e9-121">-ServerName</span></span>
<span data-ttu-id="083e9-122">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="083e9-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="083e9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="083e9-123">-Confirm</span></span>
<span data-ttu-id="083e9-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="083e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083e9-125">-WhatIf</span></span>
<span data-ttu-id="083e9-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="083e9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083e9-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="083e9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083e9-128">CommonParameters</span></span>
<span data-ttu-id="083e9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="083e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083e9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083e9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="083e9-131">INPUTS</span></span>

### <span data-ttu-id="083e9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="083e9-132">System.String</span></span>

## <span data-ttu-id="083e9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="083e9-133">OUTPUTS</span></span>

### <span data-ttu-id="083e9-134">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="083e9-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="083e9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="083e9-135">NOTES</span></span>

## <span data-ttu-id="083e9-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="083e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="083e9-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="083e9-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="083e9-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="083e9-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="083e9-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="083e9-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="083e9-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="083e9-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="083e9-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
