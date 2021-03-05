---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 141723a0e920f18aed9808ed3c5f205534c48185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989733"
---
# <span data-ttu-id="06003-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="06003-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="06003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06003-102">SYNOPSIS</span></span>
<span data-ttu-id="06003-103">link service for workspace</span><span class="sxs-lookup"><span data-stu-id="06003-103">link service for workspace</span></span>

## <span data-ttu-id="06003-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06003-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06003-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06003-105">DESCRIPTION</span></span>
<span data-ttu-id="06003-106">link service for workspace</span><span class="sxs-lookup"><span data-stu-id="06003-106">link service for workspace</span></span>

## <span data-ttu-id="06003-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06003-107">EXAMPLES</span></span>

### <span data-ttu-id="06003-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06003-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="06003-109">Кластер связей для рабочей области</span><span class="sxs-lookup"><span data-stu-id="06003-109">link cluster for workspace</span></span>

## <span data-ttu-id="06003-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06003-110">PARAMETERS</span></span>

### <span data-ttu-id="06003-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06003-111">-AsJob</span></span>
<span data-ttu-id="06003-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="06003-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06003-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06003-113">-DefaultProfile</span></span>
<span data-ttu-id="06003-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06003-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06003-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="06003-115">-LinkedServiceName</span></span>
<span data-ttu-id="06003-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="06003-116">The Workspace name.</span></span>

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

### <span data-ttu-id="06003-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06003-117">-ResourceGroupName</span></span>
<span data-ttu-id="06003-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06003-118">The resource group name.</span></span>

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

### <span data-ttu-id="06003-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06003-119">-ResourceId</span></span>
<span data-ttu-id="06003-120">ИД ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="06003-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="06003-121">Он должен использоваться для связывания ресурсов, для которых требуется доступ для чтения</span><span class="sxs-lookup"><span data-stu-id="06003-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06003-122">-Теги</span><span class="sxs-lookup"><span data-stu-id="06003-122">-Tags</span></span>
<span data-ttu-id="06003-123">Теги.</span><span class="sxs-lookup"><span data-stu-id="06003-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06003-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06003-124">-WorkspaceName</span></span>
<span data-ttu-id="06003-125">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="06003-125">The Workspace name.</span></span>

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

### <span data-ttu-id="06003-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="06003-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="06003-127">ИД ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="06003-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="06003-128">Он должен использоваться для связывания ресурсов, для которых требуется доступ к записи.</span><span class="sxs-lookup"><span data-stu-id="06003-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="06003-129">Кластер должен иметь состояние подготовка "Успешно" и действительные свойства keyvault.</span><span class="sxs-lookup"><span data-stu-id="06003-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06003-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06003-130">-Confirm</span></span>
<span data-ttu-id="06003-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06003-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06003-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06003-132">-WhatIf</span></span>
<span data-ttu-id="06003-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06003-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06003-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06003-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06003-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06003-135">CommonParameters</span></span>
<span data-ttu-id="06003-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06003-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06003-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06003-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06003-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06003-138">INPUTS</span></span>

### <span data-ttu-id="06003-139">System.String</span><span class="sxs-lookup"><span data-stu-id="06003-139">System.String</span></span>

## <span data-ttu-id="06003-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06003-140">OUTPUTS</span></span>

### <span data-ttu-id="06003-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="06003-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="06003-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06003-142">NOTES</span></span>

## <span data-ttu-id="06003-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06003-143">RELATED LINKS</span></span>
