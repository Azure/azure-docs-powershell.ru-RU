---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248078"
---
# <span data-ttu-id="eec5d-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="eec5d-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="eec5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eec5d-102">SYNOPSIS</span></span>
<span data-ttu-id="eec5d-103">Служба Link для рабочей области</span><span class="sxs-lookup"><span data-stu-id="eec5d-103">link service for workspace</span></span>

## <span data-ttu-id="eec5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eec5d-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec5d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eec5d-105">DESCRIPTION</span></span>
<span data-ttu-id="eec5d-106">Служба Link для рабочей области</span><span class="sxs-lookup"><span data-stu-id="eec5d-106">link service for workspace</span></span>

## <span data-ttu-id="eec5d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eec5d-107">EXAMPLES</span></span>

### <span data-ttu-id="eec5d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eec5d-108">Example 1</span></span>
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

<span data-ttu-id="eec5d-109">кластер связей для рабочей области</span><span class="sxs-lookup"><span data-stu-id="eec5d-109">link cluster for workspace</span></span>

## <span data-ttu-id="eec5d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eec5d-110">PARAMETERS</span></span>

### <span data-ttu-id="eec5d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec5d-111">-AsJob</span></span>
<span data-ttu-id="eec5d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eec5d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eec5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec5d-113">-DefaultProfile</span></span>
<span data-ttu-id="eec5d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eec5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec5d-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="eec5d-115">-LinkedServiceName</span></span>
<span data-ttu-id="eec5d-116">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eec5d-116">The Workspace name.</span></span>

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

### <span data-ttu-id="eec5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="eec5d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eec5d-118">The resource group name.</span></span>

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

### <span data-ttu-id="eec5d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eec5d-119">-ResourceId</span></span>
<span data-ttu-id="eec5d-120">Идентификатор ресурса ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="eec5d-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="eec5d-121">Этот способ следует использовать для связывания ресурсов, которым требуется доступ для чтения</span><span class="sxs-lookup"><span data-stu-id="eec5d-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="eec5d-122">-Теги</span><span class="sxs-lookup"><span data-stu-id="eec5d-122">-Tags</span></span>
<span data-ttu-id="eec5d-123">Embed.</span><span class="sxs-lookup"><span data-stu-id="eec5d-123">Tags.</span></span>

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

### <span data-ttu-id="eec5d-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eec5d-124">-WorkspaceName</span></span>
<span data-ttu-id="eec5d-125">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eec5d-125">The Workspace name.</span></span>

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

### <span data-ttu-id="eec5d-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="eec5d-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="eec5d-127">Идентификатор ресурса ресурса, который будет связан с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="eec5d-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="eec5d-128">Этот способ следует использовать для связывания ресурсов, которым требуется доступ на запись.</span><span class="sxs-lookup"><span data-stu-id="eec5d-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="eec5d-129">Кластер должен иметь состояние подготовки "успешно" и допустимые свойства keyvault.</span><span class="sxs-lookup"><span data-stu-id="eec5d-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="eec5d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eec5d-130">-Confirm</span></span>
<span data-ttu-id="eec5d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eec5d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec5d-132">-WhatIf</span></span>
<span data-ttu-id="eec5d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eec5d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec5d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eec5d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec5d-135">CommonParameters</span></span>
<span data-ttu-id="eec5d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eec5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec5d-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eec5d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec5d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eec5d-138">INPUTS</span></span>

### <span data-ttu-id="eec5d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eec5d-139">System.String</span></span>

## <span data-ttu-id="eec5d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eec5d-140">OUTPUTS</span></span>

### <span data-ttu-id="eec5d-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="eec5d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="eec5d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eec5d-142">NOTES</span></span>

## <span data-ttu-id="eec5d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eec5d-143">RELATED LINKS</span></span>
