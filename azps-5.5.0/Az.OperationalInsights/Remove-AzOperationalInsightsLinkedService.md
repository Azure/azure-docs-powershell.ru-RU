---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220780"
---
# <span data-ttu-id="8789d-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="8789d-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="8789d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8789d-102">SYNOPSIS</span></span>
<span data-ttu-id="8789d-103">Unlink service for workspace</span><span class="sxs-lookup"><span data-stu-id="8789d-103">Unlink service for workspace</span></span>

## <span data-ttu-id="8789d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8789d-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8789d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8789d-105">DESCRIPTION</span></span>
<span data-ttu-id="8789d-106">Unlink service for workspace</span><span class="sxs-lookup"><span data-stu-id="8789d-106">Unlink service for workspace</span></span>

## <span data-ttu-id="8789d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8789d-107">EXAMPLES</span></span>

### <span data-ttu-id="8789d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8789d-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="8789d-109">Unlink linked service for workspace</span><span class="sxs-lookup"><span data-stu-id="8789d-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="8789d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8789d-110">PARAMETERS</span></span>

### <span data-ttu-id="8789d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8789d-111">-AsJob</span></span>
<span data-ttu-id="8789d-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8789d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8789d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8789d-113">-DefaultProfile</span></span>
<span data-ttu-id="8789d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8789d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8789d-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="8789d-115">-LinkedServiceName</span></span>
<span data-ttu-id="8789d-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8789d-116">The Workspace name.</span></span>

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

### <span data-ttu-id="8789d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8789d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8789d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8789d-118">The resource group name.</span></span>

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

### <span data-ttu-id="8789d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8789d-119">-WorkspaceName</span></span>
<span data-ttu-id="8789d-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8789d-120">The Workspace name.</span></span>

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

### <span data-ttu-id="8789d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8789d-121">-Confirm</span></span>
<span data-ttu-id="8789d-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8789d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8789d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8789d-123">-WhatIf</span></span>
<span data-ttu-id="8789d-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8789d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8789d-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8789d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8789d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8789d-126">CommonParameters</span></span>
<span data-ttu-id="8789d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8789d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8789d-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8789d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8789d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8789d-129">INPUTS</span></span>

### <span data-ttu-id="8789d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8789d-130">System.String</span></span>

## <span data-ttu-id="8789d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8789d-131">OUTPUTS</span></span>

### <span data-ttu-id="8789d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8789d-132">System.Boolean</span></span>

## <span data-ttu-id="8789d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8789d-133">NOTES</span></span>

## <span data-ttu-id="8789d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8789d-134">RELATED LINKS</span></span>
