---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568220"
---
# <span data-ttu-id="57585-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="57585-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="57585-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57585-102">SYNOPSIS</span></span>
<span data-ttu-id="57585-103">Создание группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="57585-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57585-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57585-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57585-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57585-105">DESCRIPTION</span></span>
<span data-ttu-id="57585-106">Командлет **New-AzureRmOperationalInsightsComputerGroup** создает группу компьютеров в группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="57585-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="57585-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57585-107">EXAMPLES</span></span>

## <span data-ttu-id="57585-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57585-108">PARAMETERS</span></span>

### <span data-ttu-id="57585-109">-Категория</span><span class="sxs-lookup"><span data-stu-id="57585-109">-Category</span></span>
<span data-ttu-id="57585-110">Указывает категорию группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="57585-110">Specifies the category of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57585-111">-DefaultProfile</span></span>
<span data-ttu-id="57585-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="57585-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57585-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57585-113">-DisplayName</span></span>
<span data-ttu-id="57585-114">Указывает отображаемое имя группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="57585-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-115">-Force</span><span class="sxs-lookup"><span data-stu-id="57585-115">-Force</span></span>
<span data-ttu-id="57585-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="57585-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57585-117">-Query</span><span class="sxs-lookup"><span data-stu-id="57585-117">-Query</span></span>
<span data-ttu-id="57585-118">Указывает запрос группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="57585-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57585-119">-ResourceGroupName</span></span>
<span data-ttu-id="57585-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="57585-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="57585-121">Командлет создаст группу компьютеров в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57585-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="57585-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="57585-122">-SavedSearchId</span></span>
<span data-ttu-id="57585-123">Указывает идентификатор группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="57585-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-124">-Version</span><span class="sxs-lookup"><span data-stu-id="57585-124">-Version</span></span>
<span data-ttu-id="57585-125">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="57585-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57585-126">-WorkspaceName</span></span>
<span data-ttu-id="57585-127">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="57585-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57585-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57585-128">-Confirm</span></span>
<span data-ttu-id="57585-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57585-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57585-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57585-130">-WhatIf</span></span>
<span data-ttu-id="57585-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57585-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57585-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57585-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57585-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57585-133">CommonParameters</span></span>
<span data-ttu-id="57585-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57585-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57585-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57585-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57585-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57585-136">INPUTS</span></span>

### <span data-ttu-id="57585-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="57585-137">None</span></span>
<span data-ttu-id="57585-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="57585-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57585-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57585-139">OUTPUTS</span></span>

## <span data-ttu-id="57585-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="57585-140">NOTES</span></span>

## <span data-ttu-id="57585-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57585-141">RELATED LINKS</span></span>

