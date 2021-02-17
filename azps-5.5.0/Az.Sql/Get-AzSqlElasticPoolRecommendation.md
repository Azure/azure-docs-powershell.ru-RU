---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222164"
---
# <span data-ttu-id="9f061-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="9f061-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="9f061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f061-102">SYNOPSIS</span></span>
<span data-ttu-id="9f061-103">Получает рекомендации по эластичности пула.</span><span class="sxs-lookup"><span data-stu-id="9f061-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="9f061-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f061-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f061-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f061-105">DESCRIPTION</span></span>
<span data-ttu-id="9f061-106">**Cmdlet Get-AzSqlElasticPoolRecommendation** получает рекомендации по эластичности пула для сервера.</span><span class="sxs-lookup"><span data-stu-id="9f061-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="9f061-107">Эти рекомендации включают следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f061-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="9f061-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="9f061-108">DatabaseCollection.</span></span> <span data-ttu-id="9f061-109">Набор имен баз данных, которые относятся к пулу.</span><span class="sxs-lookup"><span data-stu-id="9f061-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="9f061-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="9f061-110">DatabaseDtuMin.</span></span> <span data-ttu-id="9f061-111">Гарантия передачи данных (DTU) для баз данных в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="9f061-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="9f061-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="9f061-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="9f061-113">DTU cap для баз данных в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="9f061-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="9f061-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="9f061-114">Dtu.</span></span> <span data-ttu-id="9f061-115">Гарантия DTU для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="9f061-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="9f061-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="9f061-116">StorageMb.</span></span> <span data-ttu-id="9f061-117">Хранилище в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="9f061-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="9f061-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="9f061-118">Edition.</span></span> <span data-ttu-id="9f061-119">Выпуск для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="9f061-119">Edition for the elastic pool.</span></span> <span data-ttu-id="9f061-120">Допустимые значения для этого параметра: Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="9f061-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="9f061-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="9f061-121">IncludeAllDatabases.</span></span> <span data-ttu-id="9f061-122">Указывает, должны ли возвращаться все базы данных в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="9f061-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="9f061-123">Имя.</span><span class="sxs-lookup"><span data-stu-id="9f061-123">Name.</span></span> <span data-ttu-id="9f061-124">Имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="9f061-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="9f061-125">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f061-125">EXAMPLES</span></span>

### <span data-ttu-id="9f061-126">Пример 1. Получить рекомендации для сервера</span><span class="sxs-lookup"><span data-stu-id="9f061-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="9f061-127">Эта команда получает рекомендации по эластичности пула для сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="9f061-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="9f061-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f061-128">PARAMETERS</span></span>

### <span data-ttu-id="9f061-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f061-129">-DefaultProfile</span></span>
<span data-ttu-id="9f061-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f061-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f061-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f061-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f061-132">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="9f061-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9f061-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f061-133">-ServerName</span></span>
<span data-ttu-id="9f061-134">Указывает имя сервера, для которого этот cmdlet получает рекомендации.</span><span class="sxs-lookup"><span data-stu-id="9f061-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="9f061-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f061-135">-Confirm</span></span>
<span data-ttu-id="9f061-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f061-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f061-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f061-137">-WhatIf</span></span>
<span data-ttu-id="9f061-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f061-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f061-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f061-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f061-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f061-140">CommonParameters</span></span>
<span data-ttu-id="9f061-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f061-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f061-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f061-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f061-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f061-143">INPUTS</span></span>

### <span data-ttu-id="9f061-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9f061-144">System.String</span></span>

## <span data-ttu-id="9f061-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f061-145">OUTPUTS</span></span>

### <span data-ttu-id="9f061-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="9f061-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="9f061-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f061-147">NOTES</span></span>

## <span data-ttu-id="9f061-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f061-148">RELATED LINKS</span></span>
