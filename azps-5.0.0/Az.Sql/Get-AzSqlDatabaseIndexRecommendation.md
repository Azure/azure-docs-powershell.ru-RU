---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245669"
---
# <span data-ttu-id="7fdd2-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7fdd2-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="7fdd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fdd2-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdd2-103">Получает рекомендованные операции с индексами для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="7fdd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fdd2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fdd2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fdd2-105">DESCRIPTION</span></span>
<span data-ttu-id="7fdd2-106">Командлет **Get-AzSqlDatabaseIndexRecommendation** получает рекомендованные операции с индексами для сервера базы данных SQL Azure или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="7fdd2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fdd2-107">EXAMPLES</span></span>

### <span data-ttu-id="7fdd2-108">Пример 1: получение рекомендаций по индексам для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="7fdd2-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7fdd2-109">Эта команда возвращает рекомендации по индексам для всех баз данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="7fdd2-110">Пример 2: получение рекомендаций по индексу для определенной базы данных</span><span class="sxs-lookup"><span data-stu-id="7fdd2-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7fdd2-111">Эта команда возвращает рекомендации по индексированию для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="7fdd2-112">Пример 3: получение одной рекомендации по индексу по имени</span><span class="sxs-lookup"><span data-stu-id="7fdd2-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="7fdd2-113">Эта команда возвращает один совет по индексу по имени.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="7fdd2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fdd2-114">PARAMETERS</span></span>

### <span data-ttu-id="7fdd2-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fdd2-115">-DatabaseName</span></span>
<span data-ttu-id="7fdd2-116">Указывает имя базы данных, для которой этот командлет получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdd2-117">-DefaultProfile</span></span>
<span data-ttu-id="7fdd2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7fdd2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fdd2-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="7fdd2-119">-IndexRecommendationName</span></span>
<span data-ttu-id="7fdd2-120">Указывает имя рекомендации по индексированию, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="7fdd2-122">Указывает имя группы ресурсов, для которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="7fdd2-123">Этот командлет получает рекомендации по индексу для базы данных, размещенной на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="7fdd2-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7fdd2-124">-ServerName</span></span>
<span data-ttu-id="7fdd2-125">Указывает сервер, на котором размещена база данных, для которой этот командлет получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdd2-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="7fdd2-126">-TableName</span></span>
<span data-ttu-id="7fdd2-127">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdd2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fdd2-128">-Confirm</span></span>
<span data-ttu-id="7fdd2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fdd2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fdd2-130">-WhatIf</span></span>
<span data-ttu-id="7fdd2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fdd2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fdd2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdd2-133">CommonParameters</span></span>
<span data-ttu-id="7fdd2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdd2-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fdd2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdd2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fdd2-136">INPUTS</span></span>

### <span data-ttu-id="7fdd2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7fdd2-137">System.String</span></span>

## <span data-ttu-id="7fdd2-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fdd2-138">OUTPUTS</span></span>

### <span data-ttu-id="7fdd2-139">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7fdd2-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="7fdd2-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fdd2-140">NOTES</span></span>

## <span data-ttu-id="7fdd2-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fdd2-141">RELATED LINKS</span></span>

[<span data-ttu-id="7fdd2-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7fdd2-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="7fdd2-143">Остановить-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7fdd2-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
