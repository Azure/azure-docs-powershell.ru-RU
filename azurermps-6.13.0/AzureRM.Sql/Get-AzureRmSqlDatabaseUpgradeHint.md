---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733429"
---
# <span data-ttu-id="ad46f-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="ad46f-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="ad46f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad46f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad46f-103">Получение подсказок ценовой категории для базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad46f-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad46f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad46f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad46f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad46f-105">DESCRIPTION</span></span>
<span data-ttu-id="ad46f-106">Командлет **Get-AzureRmSqlDatabaseUpgradeHint** получает подсказки по ценовым категориям для обновления базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad46f-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="ad46f-107">Базы данных, которые все еще находятся в ценовой категории веб-и бизнес-цен, получают подсказку для обновления до новой базовой, стандартной или расширенной ценовой категории.</span><span class="sxs-lookup"><span data-stu-id="ad46f-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="ad46f-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="ad46f-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ad46f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad46f-109">EXAMPLES</span></span>

### <span data-ttu-id="ad46f-110">Пример 1: получение рекомендаций для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="ad46f-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ad46f-111">Эта команда возвращает подсказки обновления для всех баз данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ad46f-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="ad46f-112">Пример 2: получение рекомендаций для определенной базы данных</span><span class="sxs-lookup"><span data-stu-id="ad46f-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ad46f-113">Эта команда возвращает подсказки для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad46f-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="ad46f-114">Пример 3: получение рекомендаций для всех баз данных, которые не находятся в пуле эластичных баз данных</span><span class="sxs-lookup"><span data-stu-id="ad46f-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="ad46f-115">Эта команда возвращает подсказки обновления для всех баз данных, которые не находятся в пуле эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="ad46f-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="ad46f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad46f-116">PARAMETERS</span></span>

### <span data-ttu-id="ad46f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad46f-117">-DatabaseName</span></span>
<span data-ttu-id="ad46f-118">Указывает имя базы данных SQL, для которой этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="ad46f-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="ad46f-119">Если не указать базу данных, этот командлет получает подсказки для всех баз данных на логическом сервере.</span><span class="sxs-lookup"><span data-stu-id="ad46f-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="ad46f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad46f-120">-DefaultProfile</span></span>
<span data-ttu-id="ad46f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad46f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad46f-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="ad46f-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="ad46f-123">Указывает, исключаются ли базы данных в пулах эластичной базы данных из возвращенных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="ad46f-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="ad46f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad46f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad46f-125">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="ad46f-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ad46f-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ad46f-126">-ServerName</span></span>
<span data-ttu-id="ad46f-127">Указывает имя сервера, на котором размещена база данных, для которой этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="ad46f-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="ad46f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad46f-128">-Confirm</span></span>
<span data-ttu-id="ad46f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad46f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad46f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad46f-130">-WhatIf</span></span>
<span data-ttu-id="ad46f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad46f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad46f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad46f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad46f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad46f-133">CommonParameters</span></span>
<span data-ttu-id="ad46f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad46f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad46f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad46f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad46f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad46f-136">INPUTS</span></span>

### <span data-ttu-id="ad46f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad46f-137">System.String</span></span>

### <span data-ttu-id="ad46f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad46f-138">System.Boolean</span></span>

## <span data-ttu-id="ad46f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad46f-139">OUTPUTS</span></span>

### <span data-ttu-id="ad46f-140">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="ad46f-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="ad46f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad46f-141">NOTES</span></span>

## <span data-ttu-id="ad46f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad46f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad46f-143">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ad46f-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="ad46f-144">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad46f-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


