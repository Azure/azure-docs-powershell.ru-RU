---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912929"
---
# <span data-ttu-id="bfa53-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="bfa53-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="bfa53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfa53-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa53-103">Получение рекомендаций пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bfa53-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="bfa53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfa53-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfa53-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa53-106">Командлет **Get-AzSqlElasticPoolRecommendation** получает рекомендации пула эластичных БД для сервера.</span><span class="sxs-lookup"><span data-stu-id="bfa53-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="bfa53-107">Эти рекомендации включают следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bfa53-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="bfa53-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="bfa53-108">DatabaseCollection.</span></span> <span data-ttu-id="bfa53-109">Коллекция имен баз данных, которые принадлежат пулу.</span><span class="sxs-lookup"><span data-stu-id="bfa53-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="bfa53-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="bfa53-110">DatabaseDtuMin.</span></span> <span data-ttu-id="bfa53-111">Гарантируется наличие модуля передачи данных (DTU) для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bfa53-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="bfa53-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="bfa53-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="bfa53-113">Ограничение DTU для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bfa53-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="bfa53-114">Дополнительную.</span><span class="sxs-lookup"><span data-stu-id="bfa53-114">Dtu.</span></span> <span data-ttu-id="bfa53-115">Гарантия DTU для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bfa53-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="bfa53-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="bfa53-116">StorageMb.</span></span> <span data-ttu-id="bfa53-117">Хранилище в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bfa53-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="bfa53-118">Ознакомитель.</span><span class="sxs-lookup"><span data-stu-id="bfa53-118">Edition.</span></span> <span data-ttu-id="bfa53-119">Выпуск для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bfa53-119">Edition for the elastic pool.</span></span> <span data-ttu-id="bfa53-120">Допустимые значения этого параметра: Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="bfa53-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="bfa53-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="bfa53-121">IncludeAllDatabases.</span></span> <span data-ttu-id="bfa53-122">Указывает, должны ли возвращаться все базы данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bfa53-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="bfa53-123">Псевдоним.</span><span class="sxs-lookup"><span data-stu-id="bfa53-123">Name.</span></span> <span data-ttu-id="bfa53-124">Имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bfa53-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="bfa53-125">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfa53-125">EXAMPLES</span></span>

### <span data-ttu-id="bfa53-126">Пример 1: получение рекомендаций для сервера</span><span class="sxs-lookup"><span data-stu-id="bfa53-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="bfa53-127">Эта команда получает рекомендации пула эластичных БД для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="bfa53-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="bfa53-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfa53-128">PARAMETERS</span></span>

### <span data-ttu-id="bfa53-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa53-129">-DefaultProfile</span></span>
<span data-ttu-id="bfa53-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfa53-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfa53-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa53-131">-ResourceGroupName</span></span>
<span data-ttu-id="bfa53-132">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="bfa53-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bfa53-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bfa53-133">-ServerName</span></span>
<span data-ttu-id="bfa53-134">Указывает имя сервера, для которого этот командлет получает рекомендации.</span><span class="sxs-lookup"><span data-stu-id="bfa53-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="bfa53-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa53-135">-Confirm</span></span>
<span data-ttu-id="bfa53-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfa53-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa53-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa53-137">-WhatIf</span></span>
<span data-ttu-id="bfa53-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfa53-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa53-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfa53-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa53-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa53-140">CommonParameters</span></span>
<span data-ttu-id="bfa53-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfa53-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa53-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfa53-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa53-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfa53-143">INPUTS</span></span>

### <span data-ttu-id="bfa53-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bfa53-144">System.String</span></span>

## <span data-ttu-id="bfa53-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfa53-145">OUTPUTS</span></span>

### <span data-ttu-id="bfa53-146">Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="bfa53-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="bfa53-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfa53-147">NOTES</span></span>

## <span data-ttu-id="bfa53-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfa53-148">RELATED LINKS</span></span>
