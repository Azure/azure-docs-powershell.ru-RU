---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406551"
---
# <span data-ttu-id="f0f2f-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="f0f2f-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="f0f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f0f2f-103">Удаление указанного кластера "Выделенный Евартub" из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0f2f-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="f0f2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0f2f-104">SYNTAX</span></span>

### <span data-ttu-id="f0f2f-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0f2f-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0f2f-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0f2f-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0f2f-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0f2f-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0f2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0f2f-108">DESCRIPTION</span></span>
<span data-ttu-id="f0f2f-109">Этот Remove-AzEventHubCluster удаляет имя выделенного кластера ересюба из данной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="f0f2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0f2f-110">EXAMPLES</span></span>

### <span data-ttu-id="f0f2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0f2f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="f0f2f-112">Удаляет кластер Eventhub-Cluster-5557 из RSG-Cluster27651 групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0f2f-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="f0f2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0f2f-113">PARAMETERS</span></span>

### <span data-ttu-id="f0f2f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0f2f-114">-AsJob</span></span>
<span data-ttu-id="f0f2f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f0f2f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0f2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0f2f-116">-DefaultProfile</span></span>
<span data-ttu-id="f0f2f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0f2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0f2f-118">-InputObject</span></span>
<span data-ttu-id="f0f2f-119">Объект Cluster</span><span class="sxs-lookup"><span data-stu-id="f0f2f-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f0f2f-120">-Name</span></span>
<span data-ttu-id="f0f2f-121">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="f0f2f-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0f2f-122">-PassThru</span></span>
<span data-ttu-id="f0f2f-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="f0f2f-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f0f2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0f2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0f2f-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0f2f-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0f2f-126">-ResourceId</span></span>
<span data-ttu-id="f0f2f-127">ИД ресурсов кластера</span><span class="sxs-lookup"><span data-stu-id="f0f2f-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0f2f-128">-Confirm</span></span>
<span data-ttu-id="f0f2f-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0f2f-130">-WhatIf</span></span>
<span data-ttu-id="f0f2f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0f2f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0f2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0f2f-133">CommonParameters</span></span>
<span data-ttu-id="f0f2f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0f2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0f2f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0f2f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0f2f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0f2f-136">INPUTS</span></span>

### <span data-ttu-id="f0f2f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f0f2f-137">System.String</span></span>

### <span data-ttu-id="f0f2f-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f0f2f-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="f0f2f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0f2f-139">OUTPUTS</span></span>

### <span data-ttu-id="f0f2f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0f2f-140">System.Boolean</span></span>

## <span data-ttu-id="f0f2f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0f2f-141">NOTES</span></span>

## <span data-ttu-id="f0f2f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0f2f-142">RELATED LINKS</span></span>
