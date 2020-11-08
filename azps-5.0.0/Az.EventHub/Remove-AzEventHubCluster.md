---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245458"
---
# <span data-ttu-id="17e2c-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="17e2c-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="17e2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="17e2c-103">Удаляет указанный выделенный кластер Eventhub из области "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="17e2c-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="17e2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17e2c-104">SYNTAX</span></span>

### <span data-ttu-id="17e2c-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17e2c-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e2c-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17e2c-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e2c-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17e2c-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e2c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="17e2c-109">Командлет Remove-AzEventHubCluster удаляет указанное имя кластера eventhub из заданной области ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17e2c-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="17e2c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="17e2c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17e2c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="17e2c-112">Удаляет кластер Eventhub-Cluster-5557 из RSG-Cluster27651 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="17e2c-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="17e2c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="17e2c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17e2c-114">-AsJob</span></span>
<span data-ttu-id="17e2c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="17e2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17e2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e2c-116">-DefaultProfile</span></span>
<span data-ttu-id="17e2c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17e2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e2c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e2c-118">-InputObject</span></span>
<span data-ttu-id="17e2c-119">Объект Cluster</span><span class="sxs-lookup"><span data-stu-id="17e2c-119">Cluster Object</span></span>

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

### <span data-ttu-id="17e2c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17e2c-120">-Name</span></span>
<span data-ttu-id="17e2c-121">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="17e2c-121">Cluster Name</span></span>

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

### <span data-ttu-id="17e2c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17e2c-122">-PassThru</span></span>
<span data-ttu-id="17e2c-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="17e2c-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="17e2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="17e2c-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="17e2c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="17e2c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e2c-126">-ResourceId</span></span>
<span data-ttu-id="17e2c-127">Идентификатор ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="17e2c-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="17e2c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e2c-128">-Confirm</span></span>
<span data-ttu-id="17e2c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17e2c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e2c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e2c-130">-WhatIf</span></span>
<span data-ttu-id="17e2c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17e2c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e2c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17e2c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e2c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e2c-133">CommonParameters</span></span>
<span data-ttu-id="17e2c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17e2c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e2c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17e2c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e2c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17e2c-136">INPUTS</span></span>

### <span data-ttu-id="17e2c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="17e2c-137">System.String</span></span>

### <span data-ttu-id="17e2c-138">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="17e2c-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="17e2c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e2c-139">OUTPUTS</span></span>

### <span data-ttu-id="17e2c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17e2c-140">System.Boolean</span></span>

## <span data-ttu-id="17e2c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="17e2c-141">NOTES</span></span>

## <span data-ttu-id="17e2c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17e2c-142">RELATED LINKS</span></span>
