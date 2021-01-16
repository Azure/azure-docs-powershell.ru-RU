---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402135"
---
# <span data-ttu-id="602e8-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="602e8-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="602e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="602e8-102">SYNOPSIS</span></span>
<span data-ttu-id="602e8-103">Получает подсказки о ценах на обновление сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="602e8-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="602e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="602e8-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="602e8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="602e8-105">DESCRIPTION</span></span>
<span data-ttu-id="602e8-106">Для этого можно получить советы по обновлению сервера базы данных Azure SQL **AzSqlServerUpgradeHint.**</span><span class="sxs-lookup"><span data-stu-id="602e8-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="602e8-107">Подсказки могут содержать эластичный пул баз данных и автономные подсказки базы данных.</span><span class="sxs-lookup"><span data-stu-id="602e8-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="602e8-108">Базы данных, которые все еще находятся на уровнях цен на веб-сайты и бизнес, по-прежнему могут перейти на новые уровни цен на базовый, стандартный или премиум либо перейти в эластичный пул баз данных.</span><span class="sxs-lookup"><span data-stu-id="602e8-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="602e8-109">Этот cmdlet возвращает подсказки для всех баз данных, которые были на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="602e8-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="602e8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="602e8-110">EXAMPLES</span></span>

### <span data-ttu-id="602e8-111">Пример 1. Получить объединенные рекомендации</span><span class="sxs-lookup"><span data-stu-id="602e8-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="602e8-112">Эта команда получает объединенные рекомендации для всех баз данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="602e8-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="602e8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="602e8-113">PARAMETERS</span></span>

### <span data-ttu-id="602e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="602e8-114">-DefaultProfile</span></span>
<span data-ttu-id="602e8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="602e8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="602e8-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="602e8-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="602e8-117">Указывает на то, следует ли возвращать базы данных, включенные в пулы эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="602e8-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="602e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="602e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="602e8-119">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="602e8-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="602e8-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="602e8-120">-ServerName</span></span>
<span data-ttu-id="602e8-121">Имя сервера, для которого этот cmdlet получает подсказку об обновлении.</span><span class="sxs-lookup"><span data-stu-id="602e8-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="602e8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="602e8-122">-Confirm</span></span>
<span data-ttu-id="602e8-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="602e8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="602e8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="602e8-124">-WhatIf</span></span>
<span data-ttu-id="602e8-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="602e8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="602e8-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="602e8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="602e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602e8-127">CommonParameters</span></span>
<span data-ttu-id="602e8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="602e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602e8-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="602e8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602e8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="602e8-130">INPUTS</span></span>

### <span data-ttu-id="602e8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="602e8-131">System.String</span></span>

### <span data-ttu-id="602e8-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="602e8-132">System.Boolean</span></span>

## <span data-ttu-id="602e8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="602e8-133">OUTPUTS</span></span>

### <span data-ttu-id="602e8-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="602e8-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="602e8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="602e8-135">NOTES</span></span>

## <span data-ttu-id="602e8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="602e8-136">RELATED LINKS</span></span>

[<span data-ttu-id="602e8-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="602e8-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="602e8-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="602e8-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="602e8-139">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="602e8-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

