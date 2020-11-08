---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247573"
---
# <span data-ttu-id="c36ce-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="c36ce-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="c36ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c36ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c36ce-103">Несвязанная служба для рабочей области</span><span class="sxs-lookup"><span data-stu-id="c36ce-103">Unlink service for workspace</span></span>

## <span data-ttu-id="c36ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c36ce-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c36ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c36ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c36ce-106">Несвязанная служба для рабочей области</span><span class="sxs-lookup"><span data-stu-id="c36ce-106">Unlink service for workspace</span></span>

## <span data-ttu-id="c36ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c36ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c36ce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c36ce-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="c36ce-109">Отсоединение связанной службы для рабочей области</span><span class="sxs-lookup"><span data-stu-id="c36ce-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="c36ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c36ce-110">PARAMETERS</span></span>

### <span data-ttu-id="c36ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c36ce-111">-AsJob</span></span>
<span data-ttu-id="c36ce-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c36ce-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c36ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36ce-113">-DefaultProfile</span></span>
<span data-ttu-id="c36ce-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c36ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c36ce-115">-LinkedServiceName</span></span>
<span data-ttu-id="c36ce-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c36ce-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="c36ce-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c36ce-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c36ce-119">-WorkspaceName</span></span>
<span data-ttu-id="c36ce-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c36ce-120">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c36ce-121">-Confirm</span></span>
<span data-ttu-id="c36ce-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c36ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c36ce-123">-WhatIf</span></span>
<span data-ttu-id="c36ce-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c36ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c36ce-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c36ce-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36ce-126">CommonParameters</span></span>
<span data-ttu-id="c36ce-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c36ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36ce-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c36ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36ce-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c36ce-129">INPUTS</span></span>

### <span data-ttu-id="c36ce-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c36ce-130">System.String</span></span>

## <span data-ttu-id="c36ce-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c36ce-131">OUTPUTS</span></span>

### <span data-ttu-id="c36ce-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c36ce-132">System.Boolean</span></span>

## <span data-ttu-id="c36ce-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c36ce-133">NOTES</span></span>

## <span data-ttu-id="c36ce-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c36ce-134">RELATED LINKS</span></span>
