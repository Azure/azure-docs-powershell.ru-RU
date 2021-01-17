---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419327"
---
# <span data-ttu-id="c2531-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2531-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="c2531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2531-102">SYNOPSIS</span></span>
<span data-ttu-id="c2531-103">Возвращает рекомендуемые операции индекса для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2531-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="c2531-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2531-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2531-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2531-105">DESCRIPTION</span></span>
<span data-ttu-id="c2531-106">Для сервера базы данных или базы данных Azure SQL рекомендуется использовать операций индексирования **для get-AzSqlDatabaseIndexRecommendation.**</span><span class="sxs-lookup"><span data-stu-id="c2531-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="c2531-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2531-107">EXAMPLES</span></span>

### <span data-ttu-id="c2531-108">Пример 1. Получите рекомендации по индексу для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="c2531-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c2531-109">Эта команда возвращает рекомендации по индексу для всех баз данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="c2531-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="c2531-110">Пример 2. Получить рекомендации по индексу для конкретной базы данных</span><span class="sxs-lookup"><span data-stu-id="c2531-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c2531-111">Эта команда возвращает рекомендации по индексу для конкретной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2531-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="c2531-112">Пример 3. Получить единую рекомендацию по индексу по имени</span><span class="sxs-lookup"><span data-stu-id="c2531-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c2531-113">Эта команда возвращает рекомендацию по одному индексу по имени.</span><span class="sxs-lookup"><span data-stu-id="c2531-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="c2531-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2531-114">PARAMETERS</span></span>

### <span data-ttu-id="c2531-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2531-115">-DatabaseName</span></span>
<span data-ttu-id="c2531-116">Имя базы данных, для которой этот cmdlet получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="c2531-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="c2531-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2531-117">-DefaultProfile</span></span>
<span data-ttu-id="c2531-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2531-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2531-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c2531-119">-IndexRecommendationName</span></span>
<span data-ttu-id="c2531-120">Указывает имя рекомендации по индексу, которая возвращается этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="c2531-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2531-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2531-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2531-122">Имя группы ресурсов, назначенной серверу.</span><span class="sxs-lookup"><span data-stu-id="c2531-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="c2531-123">Этот cmdlet получает рекомендации по индексу для базы данных, которая содержится на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="c2531-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="c2531-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c2531-124">-ServerName</span></span>
<span data-ttu-id="c2531-125">Сервер, на котором размещена база данных, для которой этот cmdlet получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="c2531-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="c2531-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="c2531-126">-TableName</span></span>
<span data-ttu-id="c2531-127">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c2531-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="c2531-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2531-128">-Confirm</span></span>
<span data-ttu-id="c2531-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2531-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2531-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2531-130">-WhatIf</span></span>
<span data-ttu-id="c2531-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2531-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2531-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2531-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2531-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2531-133">CommonParameters</span></span>
<span data-ttu-id="c2531-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2531-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2531-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2531-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2531-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2531-136">INPUTS</span></span>

### <span data-ttu-id="c2531-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c2531-137">System.String</span></span>

## <span data-ttu-id="c2531-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2531-138">OUTPUTS</span></span>

### <span data-ttu-id="c2531-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2531-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="c2531-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2531-140">NOTES</span></span>

## <span data-ttu-id="c2531-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2531-141">RELATED LINKS</span></span>

[<span data-ttu-id="c2531-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2531-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c2531-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2531-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
