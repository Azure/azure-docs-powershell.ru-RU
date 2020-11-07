---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904673"
---
# <span data-ttu-id="f785f-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="f785f-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="f785f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f785f-102">SYNOPSIS</span></span>
<span data-ttu-id="f785f-103">Создание группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f785f-103">Creates a computer group.</span></span>

## <span data-ttu-id="f785f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f785f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f785f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f785f-105">DESCRIPTION</span></span>
<span data-ttu-id="f785f-106">Командлет **New-AzOperationalInsightsComputerGroup** создает группу компьютеров в группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="f785f-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="f785f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f785f-107">EXAMPLES</span></span>

## <span data-ttu-id="f785f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f785f-108">PARAMETERS</span></span>

### <span data-ttu-id="f785f-109">-Категория</span><span class="sxs-lookup"><span data-stu-id="f785f-109">-Category</span></span>
<span data-ttu-id="f785f-110">Указывает категорию группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f785f-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f785f-111">-DefaultProfile</span></span>
<span data-ttu-id="f785f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f785f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f785f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f785f-113">-DisplayName</span></span>
<span data-ttu-id="f785f-114">Указывает отображаемое имя группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f785f-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f785f-115">-Force</span></span>
<span data-ttu-id="f785f-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f785f-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-117">-Query</span><span class="sxs-lookup"><span data-stu-id="f785f-117">-Query</span></span>
<span data-ttu-id="f785f-118">Указывает запрос группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f785f-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f785f-119">-ResourceGroupName</span></span>
<span data-ttu-id="f785f-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f785f-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f785f-121">Командлет создаст группу компьютеров в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f785f-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="f785f-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f785f-122">-SavedSearchId</span></span>
<span data-ttu-id="f785f-123">Указывает идентификатор группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f785f-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-124">-Version</span><span class="sxs-lookup"><span data-stu-id="f785f-124">-Version</span></span>
<span data-ttu-id="f785f-125">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="f785f-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f785f-126">-WorkspaceName</span></span>
<span data-ttu-id="f785f-127">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f785f-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f785f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f785f-128">-Confirm</span></span>
<span data-ttu-id="f785f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f785f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f785f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f785f-130">-WhatIf</span></span>
<span data-ttu-id="f785f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f785f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f785f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f785f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f785f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f785f-133">CommonParameters</span></span>
<span data-ttu-id="f785f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f785f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f785f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f785f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f785f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f785f-136">INPUTS</span></span>

### <span data-ttu-id="f785f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f785f-137">System.String</span></span>

### <span data-ttu-id="f785f-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f785f-138">System.Int64</span></span>

## <span data-ttu-id="f785f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f785f-139">OUTPUTS</span></span>

### <span data-ttu-id="f785f-140">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f785f-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f785f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f785f-141">NOTES</span></span>

## <span data-ttu-id="f785f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f785f-142">RELATED LINKS</span></span>
