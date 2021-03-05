---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 7b23bd6082fc79ff6096f496117c0ff6b63fd134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967480"
---
# <span data-ttu-id="f099a-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f099a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f099a-102">SYNOPSIS</span></span>
<span data-ttu-id="f099a-103">Возвращает или перечисляет группы отбойных SQL баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f099a-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="f099a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f099a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f099a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f099a-105">DESCRIPTION</span></span>
<span data-ttu-id="f099a-106">Возвращает определенную группу SQL отбойной базы данных Azure или группы отбойных серверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="f099a-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="f099a-107">Для выполнения команды может использоваться любой сервер в группе отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="f099a-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="f099a-108">Возвращаемая величина будет отражать состояние указанного сервера в отношении группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="f099a-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="f099a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f099a-109">EXAMPLES</span></span>

### <span data-ttu-id="f099a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f099a-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="f099a-111">Список всех групп отбойных серверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="f099a-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="f099a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f099a-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="f099a-113">Получите определенную группу отбойных передачи.</span><span class="sxs-lookup"><span data-stu-id="f099a-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="f099a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f099a-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="f099a-115">Получите все группы отбойных серверов, которые начинаются с "fg".</span><span class="sxs-lookup"><span data-stu-id="f099a-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="f099a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f099a-116">PARAMETERS</span></span>

### <span data-ttu-id="f099a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f099a-117">-DefaultProfile</span></span>
<span data-ttu-id="f099a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f099a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f099a-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f099a-119">-FailoverGroupName</span></span>
<span data-ttu-id="f099a-120">Имя группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f099a-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f099a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f099a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f099a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f099a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f099a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f099a-123">-ServerName</span></span>
<span data-ttu-id="f099a-124">Имя сервера базы данных Azure SQL, из которого извлекается группа отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="f099a-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="f099a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f099a-125">CommonParameters</span></span>
<span data-ttu-id="f099a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f099a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f099a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f099a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f099a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f099a-128">INPUTS</span></span>

### <span data-ttu-id="f099a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f099a-129">System.String</span></span>

## <span data-ttu-id="f099a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f099a-130">OUTPUTS</span></span>

### <span data-ttu-id="f099a-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f099a-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f099a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f099a-132">NOTES</span></span>

## <span data-ttu-id="f099a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f099a-133">RELATED LINKS</span></span>

[<span data-ttu-id="f099a-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f099a-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f099a-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f099a-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f099a-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f099a-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f099a-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f099a-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f099a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
