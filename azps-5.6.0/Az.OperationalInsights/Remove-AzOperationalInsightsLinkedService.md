---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989848"
---
# <span data-ttu-id="fbc53-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="fbc53-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="fbc53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbc53-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc53-103">Unlink service for workspace</span><span class="sxs-lookup"><span data-stu-id="fbc53-103">Unlink service for workspace</span></span>

## <span data-ttu-id="fbc53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fbc53-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbc53-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbc53-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc53-106">Unlink service for workspace</span><span class="sxs-lookup"><span data-stu-id="fbc53-106">Unlink service for workspace</span></span>

## <span data-ttu-id="fbc53-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fbc53-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc53-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbc53-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="fbc53-109">Unlink linked service for workspace</span><span class="sxs-lookup"><span data-stu-id="fbc53-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="fbc53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbc53-110">PARAMETERS</span></span>

### <span data-ttu-id="fbc53-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbc53-111">-AsJob</span></span>
<span data-ttu-id="fbc53-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fbc53-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbc53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc53-113">-DefaultProfile</span></span>
<span data-ttu-id="fbc53-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbc53-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="fbc53-115">-LinkedServiceName</span></span>
<span data-ttu-id="fbc53-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fbc53-116">The Workspace name.</span></span>

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

### <span data-ttu-id="fbc53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc53-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbc53-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbc53-118">The resource group name.</span></span>

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

### <span data-ttu-id="fbc53-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbc53-119">-WorkspaceName</span></span>
<span data-ttu-id="fbc53-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fbc53-120">The Workspace name.</span></span>

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

### <span data-ttu-id="fbc53-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbc53-121">-Confirm</span></span>
<span data-ttu-id="fbc53-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc53-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc53-123">-WhatIf</span></span>
<span data-ttu-id="fbc53-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc53-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc53-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fbc53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc53-126">CommonParameters</span></span>
<span data-ttu-id="fbc53-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc53-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbc53-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc53-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbc53-129">INPUTS</span></span>

### <span data-ttu-id="fbc53-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fbc53-130">System.String</span></span>

## <span data-ttu-id="fbc53-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fbc53-131">OUTPUTS</span></span>

### <span data-ttu-id="fbc53-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbc53-132">System.Boolean</span></span>

## <span data-ttu-id="fbc53-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fbc53-133">NOTES</span></span>

## <span data-ttu-id="fbc53-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbc53-134">RELATED LINKS</span></span>
