---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394276"
---
# <span data-ttu-id="86003-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="86003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86003-102">SYNOPSIS</span></span>
<span data-ttu-id="86003-103">Возвращает или перечисляет группы отбойных SQL баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="86003-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="86003-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86003-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86003-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86003-105">DESCRIPTION</span></span>
<span data-ttu-id="86003-106">Возвращает определенную группу отбойных SQL баз данных Azure или список групп отбойных серверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="86003-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="86003-107">Для выполнения команды может использоваться любой сервер в группе отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="86003-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="86003-108">Возвращаемая величина будет отражать состояние указанного сервера в отношении группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="86003-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="86003-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86003-109">EXAMPLES</span></span>

### <span data-ttu-id="86003-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86003-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="86003-111">Список всех групп отбойных серверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="86003-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="86003-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="86003-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="86003-113">Получите определенную группу отбойных передачи.</span><span class="sxs-lookup"><span data-stu-id="86003-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="86003-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="86003-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="86003-115">Получите все группы отбойных серверов, которые начинаются с "fg".</span><span class="sxs-lookup"><span data-stu-id="86003-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="86003-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86003-116">PARAMETERS</span></span>

### <span data-ttu-id="86003-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86003-117">-DefaultProfile</span></span>
<span data-ttu-id="86003-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86003-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86003-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="86003-119">-FailoverGroupName</span></span>
<span data-ttu-id="86003-120">Имя группы отбойных SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="86003-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="86003-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86003-121">-ResourceGroupName</span></span>
<span data-ttu-id="86003-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86003-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="86003-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86003-123">-ServerName</span></span>
<span data-ttu-id="86003-124">Имя сервера базы данных Azure SQL, из которого извлекается группа отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="86003-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="86003-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86003-125">CommonParameters</span></span>
<span data-ttu-id="86003-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86003-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86003-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86003-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86003-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86003-128">INPUTS</span></span>

### <span data-ttu-id="86003-129">System.String</span><span class="sxs-lookup"><span data-stu-id="86003-129">System.String</span></span>

## <span data-ttu-id="86003-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86003-130">OUTPUTS</span></span>

### <span data-ttu-id="86003-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="86003-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="86003-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86003-132">NOTES</span></span>

## <span data-ttu-id="86003-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86003-133">RELATED LINKS</span></span>

[<span data-ttu-id="86003-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="86003-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="86003-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="86003-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="86003-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="86003-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="86003-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="86003-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="86003-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
