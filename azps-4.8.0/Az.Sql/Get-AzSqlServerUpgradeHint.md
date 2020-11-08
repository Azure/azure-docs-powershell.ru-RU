---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078664"
---
# <span data-ttu-id="60762-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="60762-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="60762-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60762-102">SYNOPSIS</span></span>
<span data-ttu-id="60762-103">Получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60762-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="60762-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60762-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60762-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60762-105">DESCRIPTION</span></span>
<span data-ttu-id="60762-106">Командлет **Get-AzSqlServerUpgradeHint** получает подсказки ценовой категории для обновления сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60762-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="60762-107">Подсказки могут содержать пул эластичных баз данных и отдельные подсказки для базы данных.</span><span class="sxs-lookup"><span data-stu-id="60762-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="60762-108">Базы данных, которые все еще находятся на веб-сайте и корпоративными категориями, получают подсказку к обновлению до новой базовой, стандартной или расширенной ценовой категории, а также для перехода в пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="60762-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="60762-109">Этот командлет возвращает подсказки для всех баз данных, размещенных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="60762-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="60762-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60762-110">EXAMPLES</span></span>

### <span data-ttu-id="60762-111">Пример 1: получение комбинированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="60762-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="60762-112">Эта команда получает Объединенные рекомендации для всех баз данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="60762-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="60762-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60762-113">PARAMETERS</span></span>

### <span data-ttu-id="60762-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60762-114">-DefaultProfile</span></span>
<span data-ttu-id="60762-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="60762-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60762-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="60762-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="60762-117">Указывает, должны ли возвращаться базы данных, включенные в пулы эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="60762-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="60762-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60762-118">-ResourceGroupName</span></span>
<span data-ttu-id="60762-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="60762-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="60762-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="60762-120">-ServerName</span></span>
<span data-ttu-id="60762-121">Указывает имя сервера, для которого этот командлет получает подсказку по обновлению.</span><span class="sxs-lookup"><span data-stu-id="60762-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="60762-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60762-122">-Confirm</span></span>
<span data-ttu-id="60762-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60762-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60762-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60762-124">-WhatIf</span></span>
<span data-ttu-id="60762-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60762-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60762-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60762-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60762-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60762-127">CommonParameters</span></span>
<span data-ttu-id="60762-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60762-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60762-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60762-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60762-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60762-130">INPUTS</span></span>

### <span data-ttu-id="60762-131">System. String</span><span class="sxs-lookup"><span data-stu-id="60762-131">System.String</span></span>

### <span data-ttu-id="60762-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60762-132">System.Boolean</span></span>

## <span data-ttu-id="60762-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60762-133">OUTPUTS</span></span>

### <span data-ttu-id="60762-134">Microsoft. Azure. Commands. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="60762-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="60762-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="60762-135">NOTES</span></span>

## <span data-ttu-id="60762-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60762-136">RELATED LINKS</span></span>

[<span data-ttu-id="60762-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="60762-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="60762-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="60762-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="60762-139">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="60762-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

