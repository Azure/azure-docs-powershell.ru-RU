---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 18dcc69746e46ba75c01cb3aeb935bdd6b25d3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559479"
---
# <span data-ttu-id="6902e-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="6902e-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="6902e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6902e-102">SYNOPSIS</span></span>
<span data-ttu-id="6902e-103">Получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6902e-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6902e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6902e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6902e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6902e-105">DESCRIPTION</span></span>
<span data-ttu-id="6902e-106">Командлет **Get-AzureRmSqlServerUpgradeHint** получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6902e-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="6902e-107">Подсказки могут содержать пул эластичных баз данных и отдельные подсказки для базы данных.</span><span class="sxs-lookup"><span data-stu-id="6902e-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="6902e-108">Базы данных, которые все еще находятся на веб-сайте и корпоративными категориями, получают подсказку к обновлению до новой базовой, стандартной или расширенной ценовой категории, а также для перехода в пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6902e-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="6902e-109">Этот командлет возвращает подсказки для всех баз данных, размещенных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="6902e-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="6902e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6902e-110">EXAMPLES</span></span>

### <span data-ttu-id="6902e-111">Пример 1: получение комбинированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="6902e-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="6902e-112">Эта команда получает Объединенные рекомендации для всех баз данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="6902e-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="6902e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6902e-113">PARAMETERS</span></span>

### <span data-ttu-id="6902e-114">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="6902e-114">-ExcludeElasticPools</span></span>
<span data-ttu-id="6902e-115">Указывает, должны ли возвращаться базы данных, включенные в пулы эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6902e-115">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="6902e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6902e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6902e-117">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="6902e-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6902e-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6902e-118">-ServerName</span></span>
<span data-ttu-id="6902e-119">Указывает имя сервера, для которого этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="6902e-119">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="6902e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6902e-120">-Confirm</span></span>
<span data-ttu-id="6902e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6902e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6902e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6902e-122">-WhatIf</span></span>
<span data-ttu-id="6902e-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6902e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6902e-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6902e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6902e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6902e-125">-DefaultProfile</span></span>
<span data-ttu-id="6902e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6902e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6902e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6902e-127">CommonParameters</span></span>
<span data-ttu-id="6902e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6902e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6902e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6902e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6902e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6902e-130">INPUTS</span></span>

## <span data-ttu-id="6902e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6902e-131">OUTPUTS</span></span>

## <span data-ttu-id="6902e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6902e-132">NOTES</span></span>

## <span data-ttu-id="6902e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6902e-133">RELATED LINKS</span></span>

[<span data-ttu-id="6902e-134">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6902e-134">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="6902e-135">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="6902e-135">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="6902e-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6902e-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


