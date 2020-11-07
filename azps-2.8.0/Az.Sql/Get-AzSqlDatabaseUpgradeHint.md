---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906201"
---
# <span data-ttu-id="6dcca-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="6dcca-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="6dcca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dcca-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcca-103">Получение подсказок ценовой категории для базы данных.</span><span class="sxs-lookup"><span data-stu-id="6dcca-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="6dcca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dcca-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dcca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dcca-105">DESCRIPTION</span></span>
<span data-ttu-id="6dcca-106">Командлет **Get-AzSqlDatabaseUpgradeHint** получает подсказки по ценовым категориям для обновления базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcca-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="6dcca-107">Базы данных, которые все еще находятся в ценовой категории веб-и бизнес-цен, получают подсказку для обновления до новой базовой, стандартной или расширенной ценовой категории.</span><span class="sxs-lookup"><span data-stu-id="6dcca-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="6dcca-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcca-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6dcca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dcca-109">EXAMPLES</span></span>

### <span data-ttu-id="6dcca-110">Пример 1: получение рекомендаций для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="6dcca-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="6dcca-111">Эта команда возвращает подсказки обновления для всех баз данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="6dcca-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="6dcca-112">Пример 2: получение рекомендаций для определенной базы данных</span><span class="sxs-lookup"><span data-stu-id="6dcca-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6dcca-113">Эта команда возвращает подсказки для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="6dcca-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="6dcca-114">Пример 3: получение рекомендаций для всех баз данных, которые не находятся в пуле эластичных баз данных</span><span class="sxs-lookup"><span data-stu-id="6dcca-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="6dcca-115">Эта команда возвращает подсказки обновления для всех баз данных, которые не находятся в пуле эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6dcca-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="6dcca-116">Пример 4: получение рекомендаций для всех баз данных на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="6dcca-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="6dcca-117">Эта команда возвращает подсказки для всех баз данных на сервере с именем Server01, начиная с "Database".</span><span class="sxs-lookup"><span data-stu-id="6dcca-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="6dcca-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dcca-118">PARAMETERS</span></span>

### <span data-ttu-id="6dcca-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dcca-119">-DatabaseName</span></span>
<span data-ttu-id="6dcca-120">Указывает имя базы данных SQL, для которой этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="6dcca-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="6dcca-121">Если не указать базу данных, этот командлет получает подсказки для всех баз данных на логическом сервере.</span><span class="sxs-lookup"><span data-stu-id="6dcca-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6dcca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcca-122">-DefaultProfile</span></span>
<span data-ttu-id="6dcca-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6dcca-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dcca-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="6dcca-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="6dcca-125">Указывает, исключаются ли базы данных в пулах эластичной базы данных из возвращенных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="6dcca-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="6dcca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dcca-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dcca-127">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="6dcca-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6dcca-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6dcca-128">-ServerName</span></span>
<span data-ttu-id="6dcca-129">Указывает имя сервера, на котором размещена база данных, для которой этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="6dcca-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="6dcca-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dcca-130">-Confirm</span></span>
<span data-ttu-id="6dcca-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6dcca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dcca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dcca-132">-WhatIf</span></span>
<span data-ttu-id="6dcca-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6dcca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dcca-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6dcca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dcca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcca-135">CommonParameters</span></span>
<span data-ttu-id="6dcca-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dcca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcca-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dcca-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcca-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dcca-138">INPUTS</span></span>

### <span data-ttu-id="6dcca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6dcca-139">System.String</span></span>

### <span data-ttu-id="6dcca-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dcca-140">System.Boolean</span></span>

## <span data-ttu-id="6dcca-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dcca-141">OUTPUTS</span></span>

### <span data-ttu-id="6dcca-142">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="6dcca-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="6dcca-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dcca-143">NOTES</span></span>

## <span data-ttu-id="6dcca-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dcca-144">RELATED LINKS</span></span>

[<span data-ttu-id="6dcca-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6dcca-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="6dcca-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="6dcca-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


