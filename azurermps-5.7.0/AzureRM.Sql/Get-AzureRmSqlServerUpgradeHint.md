---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 8516cbecac3cb4c741bb7aea1e93c10f25222b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567872"
---
# <span data-ttu-id="ea42a-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="ea42a-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="ea42a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea42a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea42a-103">Получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ea42a-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea42a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea42a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea42a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea42a-105">DESCRIPTION</span></span>
<span data-ttu-id="ea42a-106">Командлет **Get-AzureRmSqlServerUpgradeHint** получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ea42a-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="ea42a-107">Подсказки могут содержать пул эластичных баз данных и отдельные подсказки для базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea42a-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="ea42a-108">Базы данных, которые все еще находятся на веб-сайте и корпоративными категориями, получают подсказку к обновлению до новой базовой, стандартной или расширенной ценовой категории, а также для перехода в пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea42a-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="ea42a-109">Этот командлет возвращает подсказки для всех баз данных, размещенных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="ea42a-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="ea42a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea42a-110">EXAMPLES</span></span>

### <span data-ttu-id="ea42a-111">Пример 1: получение комбинированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="ea42a-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="ea42a-112">Эта команда получает Объединенные рекомендации для всех баз данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ea42a-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="ea42a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea42a-113">PARAMETERS</span></span>

### <span data-ttu-id="ea42a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea42a-114">-DefaultProfile</span></span>
<span data-ttu-id="ea42a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ea42a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="ea42a-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="ea42a-117">Указывает, должны ли возвращаться базы данных, включенные в пулы эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="ea42a-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea42a-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea42a-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="ea42a-119">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ea42a-120">-ServerName</span></span>
<span data-ttu-id="ea42a-121">Указывает имя сервера, для которого этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="ea42a-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea42a-122">-Confirm</span></span>
<span data-ttu-id="ea42a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea42a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea42a-124">-WhatIf</span></span>
<span data-ttu-id="ea42a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea42a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea42a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea42a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea42a-127">CommonParameters</span></span>
<span data-ttu-id="ea42a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea42a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea42a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea42a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea42a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea42a-130">INPUTS</span></span>

### <span data-ttu-id="ea42a-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea42a-131">None</span></span>
<span data-ttu-id="ea42a-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ea42a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea42a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea42a-133">OUTPUTS</span></span>

## <span data-ttu-id="ea42a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea42a-134">NOTES</span></span>

## <span data-ttu-id="ea42a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea42a-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea42a-136">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ea42a-136">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="ea42a-137">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea42a-137">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="ea42a-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ea42a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


