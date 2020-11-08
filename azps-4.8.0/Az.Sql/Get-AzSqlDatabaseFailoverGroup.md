---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078701"
---
# <span data-ttu-id="27221-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="27221-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27221-102">SYNOPSIS</span></span>
<span data-ttu-id="27221-103">Возвращает или перечисляет группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="27221-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="27221-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27221-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27221-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27221-105">DESCRIPTION</span></span>
<span data-ttu-id="27221-106">Возвращает определенную группу отработки отказа базы данных Azure SQL или списки групп отказа на сервере.</span><span class="sxs-lookup"><span data-stu-id="27221-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="27221-107">Для выполнения команды можно использовать любой сервер в группе отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="27221-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="27221-108">Возвращенные значения будут отражать состояние указанного сервера относительно группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="27221-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="27221-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27221-109">EXAMPLES</span></span>

### <span data-ttu-id="27221-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27221-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="27221-111">Список всех групп отказов на сервере.</span><span class="sxs-lookup"><span data-stu-id="27221-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="27221-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="27221-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="27221-113">Получить определенную группу для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="27221-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="27221-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="27221-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="27221-115">Получение всех групп, отработок отказа, на сервере, который начинается с "FG".</span><span class="sxs-lookup"><span data-stu-id="27221-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="27221-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27221-116">PARAMETERS</span></span>

### <span data-ttu-id="27221-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27221-117">-DefaultProfile</span></span>
<span data-ttu-id="27221-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="27221-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27221-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="27221-119">-FailoverGroupName</span></span>
<span data-ttu-id="27221-120">Имя группы для восстановления базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27221-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="27221-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27221-121">-ResourceGroupName</span></span>
<span data-ttu-id="27221-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27221-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="27221-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="27221-123">-ServerName</span></span>
<span data-ttu-id="27221-124">Имя сервера базы данных SQL Azure, из которого требуется получить группу для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="27221-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="27221-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27221-125">CommonParameters</span></span>
<span data-ttu-id="27221-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27221-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27221-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27221-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27221-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27221-128">INPUTS</span></span>

### <span data-ttu-id="27221-129">System. String</span><span class="sxs-lookup"><span data-stu-id="27221-129">System.String</span></span>

## <span data-ttu-id="27221-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27221-130">OUTPUTS</span></span>

### <span data-ttu-id="27221-131">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="27221-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="27221-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="27221-132">NOTES</span></span>

## <span data-ttu-id="27221-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27221-133">RELATED LINKS</span></span>

[<span data-ttu-id="27221-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27221-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27221-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="27221-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="27221-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27221-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27221-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27221-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="27221-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
