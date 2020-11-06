---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562028"
---
# <span data-ttu-id="62c63-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="62c63-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="62c63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62c63-102">SYNOPSIS</span></span>
<span data-ttu-id="62c63-103">Получение рекомендаций пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="62c63-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62c63-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c63-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c63-105">DESCRIPTION</span></span>
<span data-ttu-id="62c63-106">Командлет **Get-AzureRmSqlElasticPoolRecommendation** получает рекомендации пула эластичных БД для сервера.</span><span class="sxs-lookup"><span data-stu-id="62c63-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="62c63-107">Эти рекомендации включают следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62c63-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="62c63-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="62c63-108">DatabaseCollection.</span></span> <span data-ttu-id="62c63-109">Коллекция имен баз данных, которые принадлежат пулу.</span><span class="sxs-lookup"><span data-stu-id="62c63-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="62c63-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="62c63-110">DatabaseDtuMin.</span></span> <span data-ttu-id="62c63-111">Гарантируется наличие модуля передачи данных (DTU) для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="62c63-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="62c63-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="62c63-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="62c63-113">Ограничение DTU для баз данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="62c63-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="62c63-114">Дополнительную.</span><span class="sxs-lookup"><span data-stu-id="62c63-114">Dtu.</span></span> <span data-ttu-id="62c63-115">Гарантия DTU для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="62c63-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="62c63-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="62c63-116">StorageMb.</span></span> <span data-ttu-id="62c63-117">Хранилище в мегабайтах для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="62c63-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="62c63-118">Ознакомитель.</span><span class="sxs-lookup"><span data-stu-id="62c63-118">Edition.</span></span> <span data-ttu-id="62c63-119">Выпуск для пула эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="62c63-119">Edition for the elastic pool.</span></span> <span data-ttu-id="62c63-120">Допустимые значения этого параметра: Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="62c63-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="62c63-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="62c63-121">IncludeAllDatabases.</span></span> <span data-ttu-id="62c63-122">Указывает, должны ли возвращаться все базы данных в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="62c63-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="62c63-123">Псевдоним.</span><span class="sxs-lookup"><span data-stu-id="62c63-123">Name.</span></span> <span data-ttu-id="62c63-124">Имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="62c63-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="62c63-125">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62c63-125">EXAMPLES</span></span>

### <span data-ttu-id="62c63-126">Пример 1: получение рекомендаций для сервера</span><span class="sxs-lookup"><span data-stu-id="62c63-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="62c63-127">Эта команда получает рекомендации пула эластичных БД для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="62c63-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="62c63-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62c63-128">PARAMETERS</span></span>

### <span data-ttu-id="62c63-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c63-129">-ResourceGroupName</span></span>
<span data-ttu-id="62c63-130">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="62c63-130">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="62c63-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="62c63-131">-ServerName</span></span>
<span data-ttu-id="62c63-132">Указывает имя сервера, для которого этот командлет получает рекомендации.</span><span class="sxs-lookup"><span data-stu-id="62c63-132">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="62c63-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62c63-133">-Confirm</span></span>
<span data-ttu-id="62c63-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62c63-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c63-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c63-135">-WhatIf</span></span>
<span data-ttu-id="62c63-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62c63-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c63-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62c63-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c63-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c63-138">-DefaultProfile</span></span>
<span data-ttu-id="62c63-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62c63-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c63-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c63-140">CommonParameters</span></span>
<span data-ttu-id="62c63-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62c63-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c63-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c63-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c63-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62c63-143">INPUTS</span></span>

## <span data-ttu-id="62c63-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62c63-144">OUTPUTS</span></span>

## <span data-ttu-id="62c63-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="62c63-145">NOTES</span></span>

## <span data-ttu-id="62c63-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62c63-146">RELATED LINKS</span></span>

