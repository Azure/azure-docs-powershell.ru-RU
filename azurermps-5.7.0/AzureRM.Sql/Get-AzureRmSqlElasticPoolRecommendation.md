---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 6ebf76e339b90ab40576262807f85b85897284d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566077"
---
# <span data-ttu-id="7754d-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="7754d-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="7754d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7754d-102">SYNOPSIS</span></span>
<span data-ttu-id="7754d-103">Получение рекомендаций пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7754d-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7754d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7754d-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7754d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7754d-105">DESCRIPTION</span></span>
<span data-ttu-id="7754d-106">Командлет **Get-AzureRmSqlElasticPoolRecommendation** получает рекомендации пула эластичных БД для сервера.</span><span class="sxs-lookup"><span data-stu-id="7754d-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="7754d-107">Эти рекомендации включают следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7754d-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="7754d-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="7754d-108">DatabaseCollection.</span></span> <span data-ttu-id="7754d-109">Коллекция имен баз данных, которые принадлежат пулу.</span><span class="sxs-lookup"><span data-stu-id="7754d-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="7754d-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="7754d-110">DatabaseDtuMin.</span></span> <span data-ttu-id="7754d-111">Гарантируется наличие модуля передачи данных (DTU) для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7754d-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="7754d-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="7754d-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="7754d-113">Ограничение DTU для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7754d-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="7754d-114">Дополнительную.</span><span class="sxs-lookup"><span data-stu-id="7754d-114">Dtu.</span></span> <span data-ttu-id="7754d-115">Гарантия DTU для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="7754d-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="7754d-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="7754d-116">StorageMb.</span></span> <span data-ttu-id="7754d-117">Хранилище в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="7754d-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="7754d-118">Ознакомитель.</span><span class="sxs-lookup"><span data-stu-id="7754d-118">Edition.</span></span> <span data-ttu-id="7754d-119">Выпуск для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7754d-119">Edition for the elastic pool.</span></span> <span data-ttu-id="7754d-120">Допустимые значения этого параметра: Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="7754d-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="7754d-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="7754d-121">IncludeAllDatabases.</span></span> <span data-ttu-id="7754d-122">Указывает, должны ли возвращаться все базы данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7754d-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="7754d-123">Псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7754d-123">Name.</span></span> <span data-ttu-id="7754d-124">Имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="7754d-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="7754d-125">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7754d-125">EXAMPLES</span></span>

### <span data-ttu-id="7754d-126">Пример 1: получение рекомендаций для сервера</span><span class="sxs-lookup"><span data-stu-id="7754d-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7754d-127">Эта команда получает рекомендации пула эластичных БД для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="7754d-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="7754d-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7754d-128">PARAMETERS</span></span>

### <span data-ttu-id="7754d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7754d-129">-DefaultProfile</span></span>
<span data-ttu-id="7754d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7754d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7754d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7754d-131">-ResourceGroupName</span></span>
<span data-ttu-id="7754d-132">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="7754d-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7754d-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7754d-133">-ServerName</span></span>
<span data-ttu-id="7754d-134">Указывает имя сервера, для которого этот командлет получает рекомендации.</span><span class="sxs-lookup"><span data-stu-id="7754d-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="7754d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7754d-135">-Confirm</span></span>
<span data-ttu-id="7754d-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7754d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7754d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7754d-137">-WhatIf</span></span>
<span data-ttu-id="7754d-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7754d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7754d-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7754d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7754d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7754d-140">CommonParameters</span></span>
<span data-ttu-id="7754d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7754d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7754d-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7754d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7754d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7754d-143">INPUTS</span></span>

### <span data-ttu-id="7754d-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="7754d-144">None</span></span>
<span data-ttu-id="7754d-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7754d-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7754d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7754d-146">OUTPUTS</span></span>

## <span data-ttu-id="7754d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="7754d-147">NOTES</span></span>

## <span data-ttu-id="7754d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7754d-148">RELATED LINKS</span></span>
