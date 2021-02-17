---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212577"
---
# <span data-ttu-id="bcacb-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="bcacb-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="bcacb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcacb-102">SYNOPSIS</span></span>
<span data-ttu-id="bcacb-103">Получает подсказки о ценах на уровень для базы данных.</span><span class="sxs-lookup"><span data-stu-id="bcacb-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="bcacb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcacb-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcacb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcacb-105">DESCRIPTION</span></span>
<span data-ttu-id="bcacb-106">На **основе cmdlet Get-AzSqlDataUpgradeHint** можно получить подсказки о ценах на обновление базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="bcacb-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="bcacb-107">Базы данных, которые все еще находятся на уровнях цен на веб-сайты и бизнес, могут перейти на новые уровни цен "Базовый", "Стандартный" и "Премиум".</span><span class="sxs-lookup"><span data-stu-id="bcacb-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="bcacb-108">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="bcacb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bcacb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcacb-109">EXAMPLES</span></span>

### <span data-ttu-id="bcacb-110">Пример 1. Получить рекомендации для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="bcacb-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="bcacb-111">Эта команда возвращает подсказки об обновлении для всех баз данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="bcacb-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="bcacb-112">Пример 2. Получить рекомендации для конкретной базы данных</span><span class="sxs-lookup"><span data-stu-id="bcacb-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bcacb-113">Эта команда возвращает подсказки об обновлении для конкретной базы данных.</span><span class="sxs-lookup"><span data-stu-id="bcacb-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="bcacb-114">Пример 3. Получить рекомендации для всех баз данных, которые не находятся в эластичном пуле баз данных</span><span class="sxs-lookup"><span data-stu-id="bcacb-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="bcacb-115">Эта команда возвращает подсказки об обновлении для всех баз данных, которые не находятся в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="bcacb-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="bcacb-116">Пример 4. Получить рекомендации для всех баз данных на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="bcacb-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="bcacb-117">Эта команда возвращает подсказки об обновлении для всех баз данных на сервере Server01, которые начинаются с "Database".</span><span class="sxs-lookup"><span data-stu-id="bcacb-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="bcacb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcacb-118">PARAMETERS</span></span>

### <span data-ttu-id="bcacb-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bcacb-119">-DatabaseName</span></span>
<span data-ttu-id="bcacb-120">Указывает имя базы данных SQL, для которой этот cmdlet получает подсказку об обновлении.</span><span class="sxs-lookup"><span data-stu-id="bcacb-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="bcacb-121">Если база данных не указана, этот cmdlet будет подсказок для всех баз данных на логическом сервере.</span><span class="sxs-lookup"><span data-stu-id="bcacb-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="bcacb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcacb-122">-DefaultProfile</span></span>
<span data-ttu-id="bcacb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bcacb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcacb-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="bcacb-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="bcacb-125">Указывает на то, исключены ли базы данных из пула эластичных баз данных из возвращаемой рекомендации.</span><span class="sxs-lookup"><span data-stu-id="bcacb-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcacb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcacb-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcacb-127">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="bcacb-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bcacb-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bcacb-128">-ServerName</span></span>
<span data-ttu-id="bcacb-129">Указывает имя сервера, на котором размещена база данных, для которой этот cmdlet получает подсказку об обновлении.</span><span class="sxs-lookup"><span data-stu-id="bcacb-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="bcacb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcacb-130">-Confirm</span></span>
<span data-ttu-id="bcacb-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bcacb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcacb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcacb-132">-WhatIf</span></span>
<span data-ttu-id="bcacb-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcacb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcacb-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bcacb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcacb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcacb-135">CommonParameters</span></span>
<span data-ttu-id="bcacb-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcacb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcacb-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcacb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcacb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcacb-138">INPUTS</span></span>

### <span data-ttu-id="bcacb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bcacb-139">System.String</span></span>

### <span data-ttu-id="bcacb-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bcacb-140">System.Boolean</span></span>

## <span data-ttu-id="bcacb-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcacb-141">OUTPUTS</span></span>

### <span data-ttu-id="bcacb-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="bcacb-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="bcacb-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcacb-143">NOTES</span></span>

## <span data-ttu-id="bcacb-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcacb-144">RELATED LINKS</span></span>

[<span data-ttu-id="bcacb-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="bcacb-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="bcacb-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="bcacb-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


