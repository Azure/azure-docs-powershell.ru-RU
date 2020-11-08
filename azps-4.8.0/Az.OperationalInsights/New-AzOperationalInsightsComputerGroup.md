---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: 1f9afcd9e7a46110970785d9888f4b4efc4b0b70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242950"
---
# <span data-ttu-id="c226e-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="c226e-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="c226e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c226e-102">SYNOPSIS</span></span>
<span data-ttu-id="c226e-103">Создание группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-103">Creates a computer group.</span></span>

## <span data-ttu-id="c226e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c226e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c226e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c226e-105">DESCRIPTION</span></span>
<span data-ttu-id="c226e-106">Командлет **New-AzOperationalInsightsComputerGroup** создает группу компьютеров в группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="c226e-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="c226e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c226e-107">EXAMPLES</span></span>

### <span data-ttu-id="c226e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c226e-108">Example 1</span></span>

<span data-ttu-id="c226e-109">Создание группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-109">Creates a computer group.</span></span> <span data-ttu-id="c226e-110">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="c226e-110">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzOperationalInsightsComputerGroup -Category 'ContosoSavedSearchCategory' -DisplayName 'ContosoSavedSearchDisplayName' -Query 'Type=Event' -ResourceGroupName myresourcegroup -SavedSearchId 'ContosoSavedSearchId' -Version 1 -WorkspaceName <String>
```

## <span data-ttu-id="c226e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c226e-111">PARAMETERS</span></span>

### <span data-ttu-id="c226e-112">-Категория</span><span class="sxs-lookup"><span data-stu-id="c226e-112">-Category</span></span>
<span data-ttu-id="c226e-113">Указывает категорию группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-113">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="c226e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c226e-114">-DefaultProfile</span></span>
<span data-ttu-id="c226e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c226e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c226e-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c226e-116">-DisplayName</span></span>
<span data-ttu-id="c226e-117">Указывает отображаемое имя группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-117">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="c226e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c226e-118">-Force</span></span>
<span data-ttu-id="c226e-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c226e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c226e-120">-Query</span><span class="sxs-lookup"><span data-stu-id="c226e-120">-Query</span></span>
<span data-ttu-id="c226e-121">Указывает запрос группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-121">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="c226e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c226e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c226e-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c226e-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c226e-124">Командлет создаст группу компьютеров в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c226e-124">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="c226e-125">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c226e-125">-SavedSearchId</span></span>
<span data-ttu-id="c226e-126">Указывает идентификатор группы компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c226e-126">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="c226e-127">-Version</span><span class="sxs-lookup"><span data-stu-id="c226e-127">-Version</span></span>
<span data-ttu-id="c226e-128">Указывает версию.</span><span class="sxs-lookup"><span data-stu-id="c226e-128">Specifies the version.</span></span>

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

### <span data-ttu-id="c226e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c226e-129">-WorkspaceName</span></span>
<span data-ttu-id="c226e-130">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c226e-130">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c226e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c226e-131">-Confirm</span></span>
<span data-ttu-id="c226e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c226e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c226e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c226e-133">-WhatIf</span></span>
<span data-ttu-id="c226e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c226e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c226e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c226e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c226e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c226e-136">CommonParameters</span></span>
<span data-ttu-id="c226e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c226e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c226e-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c226e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c226e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c226e-139">INPUTS</span></span>

### <span data-ttu-id="c226e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c226e-140">System.String</span></span>

### <span data-ttu-id="c226e-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="c226e-141">System.Int64</span></span>

## <span data-ttu-id="c226e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c226e-142">OUTPUTS</span></span>

### <span data-ttu-id="c226e-143">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="c226e-143">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="c226e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c226e-144">NOTES</span></span>

## <span data-ttu-id="c226e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c226e-145">RELATED LINKS</span></span>