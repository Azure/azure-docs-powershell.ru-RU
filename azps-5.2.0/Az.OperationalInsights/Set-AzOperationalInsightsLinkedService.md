---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403215"
---
# <span data-ttu-id="b2c7e-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2c7e-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="b2c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c7e-103">link service for workspace</span><span class="sxs-lookup"><span data-stu-id="b2c7e-103">link service for workspace</span></span>

## <span data-ttu-id="b2c7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2c7e-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c7e-106">link service for workspace</span><span class="sxs-lookup"><span data-stu-id="b2c7e-106">link service for workspace</span></span>

## <span data-ttu-id="b2c7e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c7e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2c7e-108">Example 1</span></span>
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

<span data-ttu-id="b2c7e-109">Кластер связей для рабочей области</span><span class="sxs-lookup"><span data-stu-id="b2c7e-109">link cluster for workspace</span></span>

## <span data-ttu-id="b2c7e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c7e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2c7e-111">-AsJob</span></span>
<span data-ttu-id="b2c7e-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b2c7e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2c7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c7e-113">-DefaultProfile</span></span>
<span data-ttu-id="b2c7e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c7e-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b2c7e-115">-LinkedServiceName</span></span>
<span data-ttu-id="b2c7e-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-116">The Workspace name.</span></span>

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

### <span data-ttu-id="b2c7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2c7e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-118">The resource group name.</span></span>

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

### <span data-ttu-id="b2c7e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2c7e-119">-ResourceId</span></span>
<span data-ttu-id="b2c7e-120">ИД ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="b2c7e-121">Он должен использоваться для связывания ресурсов, для которых требуется доступ для чтения</span><span class="sxs-lookup"><span data-stu-id="b2c7e-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="b2c7e-122">-Теги</span><span class="sxs-lookup"><span data-stu-id="b2c7e-122">-Tags</span></span>
<span data-ttu-id="b2c7e-123">Теги.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-123">Tags.</span></span>

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

### <span data-ttu-id="b2c7e-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b2c7e-124">-WorkspaceName</span></span>
<span data-ttu-id="b2c7e-125">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-125">The Workspace name.</span></span>

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

### <span data-ttu-id="b2c7e-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="b2c7e-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="b2c7e-127">ИД ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="b2c7e-128">Он должен использоваться для связывания ресурсов, для которых требуется доступ к записи.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="b2c7e-129">Кластер должен иметь состояние подготовка "Успешно" и действительные свойства keyvault.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="b2c7e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2c7e-130">-Confirm</span></span>
<span data-ttu-id="b2c7e-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c7e-132">-WhatIf</span></span>
<span data-ttu-id="b2c7e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c7e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c7e-135">CommonParameters</span></span>
<span data-ttu-id="b2c7e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c7e-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2c7e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c7e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c7e-138">INPUTS</span></span>

### <span data-ttu-id="b2c7e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b2c7e-139">System.String</span></span>

## <span data-ttu-id="b2c7e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c7e-140">OUTPUTS</span></span>

### <span data-ttu-id="b2c7e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2c7e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="b2c7e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2c7e-142">NOTES</span></span>

## <span data-ttu-id="b2c7e-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2c7e-143">RELATED LINKS</span></span>
