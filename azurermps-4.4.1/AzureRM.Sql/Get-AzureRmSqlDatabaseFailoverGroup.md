---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 0e07ce9eb3f3368e17c20a339c65a410b5f1d553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562048"
---
# <span data-ttu-id="2083f-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="2083f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2083f-102">SYNOPSIS</span></span>
<span data-ttu-id="2083f-103">Возвращает или перечисляет группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2083f-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2083f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2083f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2083f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2083f-105">DESCRIPTION</span></span>
<span data-ttu-id="2083f-106">Возвращает определенную группу отработки отказа базы данных Azure SQL или списки групп отказа на сервере.</span><span class="sxs-lookup"><span data-stu-id="2083f-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="2083f-107">Для выполнения команды можно использовать любой сервер в группе отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="2083f-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="2083f-108">Возвращенные значения будут отражать состояние указанного сервера относительно группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="2083f-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="2083f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2083f-109">EXAMPLES</span></span>

### <span data-ttu-id="2083f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2083f-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="2083f-111">Список всех групп отказов на сервере.</span><span class="sxs-lookup"><span data-stu-id="2083f-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="2083f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2083f-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="2083f-113">Получить определенную группу для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="2083f-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="2083f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2083f-114">PARAMETERS</span></span>

### <span data-ttu-id="2083f-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="2083f-115">-FailoverGroupName</span></span>
<span data-ttu-id="2083f-116">Имя группы для восстановления базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2083f-116">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="2083f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2083f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2083f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2083f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2083f-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2083f-119">-ServerName</span></span>
<span data-ttu-id="2083f-120">Имя сервера базы данных SQL Azure, из которого требуется получить группу для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="2083f-120">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="2083f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2083f-121">-DefaultProfile</span></span>
<span data-ttu-id="2083f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2083f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2083f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2083f-123">CommonParameters</span></span>
<span data-ttu-id="2083f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2083f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2083f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2083f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2083f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2083f-126">INPUTS</span></span>

### <span data-ttu-id="2083f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2083f-127">System.String</span></span>

## <span data-ttu-id="2083f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2083f-128">OUTPUTS</span></span>

### <span data-ttu-id="2083f-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="2083f-129">System.Object</span></span>

## <span data-ttu-id="2083f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2083f-130">NOTES</span></span>

## <span data-ttu-id="2083f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2083f-131">RELATED LINKS</span></span>

[<span data-ttu-id="2083f-132">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2083f-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2083f-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="2083f-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="2083f-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2083f-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2083f-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2083f-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2083f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
