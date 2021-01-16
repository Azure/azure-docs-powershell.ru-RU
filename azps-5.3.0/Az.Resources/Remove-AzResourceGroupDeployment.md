---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506697"
---
# <span data-ttu-id="ec15e-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec15e-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ec15e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec15e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec15e-103">Удаляет развертывание группы ресурсов и все связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="ec15e-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ec15e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec15e-104">SYNTAX</span></span>

### <span data-ttu-id="ec15e-105">RemoveByResourceGroupName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec15e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec15e-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ec15e-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec15e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec15e-107">DESCRIPTION</span></span>

<span data-ttu-id="ec15e-108">Из-за выполнения всех связанных операций развертывание группы ресурсов Azure удаляется с использованием **cmdlet Remove-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="ec15e-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ec15e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec15e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec15e-110">Пример 1. Удаление развертывания группы ресурсов с помощью ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec15e-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="ec15e-111">Эта команда удаляет развертывание группы ресурсов с ее полного ИД.</span><span class="sxs-lookup"><span data-stu-id="ec15e-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ec15e-112">Успешное удаление возвращает результат "Истина".</span><span class="sxs-lookup"><span data-stu-id="ec15e-112">Successful removal returns true.</span></span>

### <span data-ttu-id="ec15e-113">Пример 2. Удаляет развертывание группы ресурсов с помощью resourceGroupName и ResourceName</span><span class="sxs-lookup"><span data-stu-id="ec15e-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="ec15e-114">Эта команда удаляет развертывание группы ресурсов с предоставленными resourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ec15e-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="ec15e-115">Успешное удаление возвращает результат "Истина".</span><span class="sxs-lookup"><span data-stu-id="ec15e-115">Successful removal returns true.</span></span>

## <span data-ttu-id="ec15e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec15e-116">PARAMETERS</span></span>

### <span data-ttu-id="ec15e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec15e-117">-DefaultProfile</span></span>
<span data-ttu-id="ec15e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ec15e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec15e-119">-Id</span><span class="sxs-lookup"><span data-stu-id="ec15e-119">-Id</span></span>
<span data-ttu-id="ec15e-120">Определяет ИД развертывания группы ресурсов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ec15e-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec15e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ec15e-121">-Name</span></span>
<span data-ttu-id="ec15e-122">Имя развертывания группы ресурсов, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ec15e-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec15e-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec15e-123">-Pre</span></span>
<span data-ttu-id="ec15e-124">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="ec15e-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ec15e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec15e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec15e-126">Имя группы ресурсов, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="ec15e-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec15e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec15e-127">-Confirm</span></span>
<span data-ttu-id="ec15e-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ec15e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec15e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec15e-129">-WhatIf</span></span>
<span data-ttu-id="ec15e-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec15e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec15e-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ec15e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec15e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec15e-132">CommonParameters</span></span>
<span data-ttu-id="ec15e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec15e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec15e-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec15e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec15e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec15e-135">INPUTS</span></span>

### <span data-ttu-id="ec15e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ec15e-136">System.String</span></span>

## <span data-ttu-id="ec15e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec15e-137">OUTPUTS</span></span>

### <span data-ttu-id="ec15e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec15e-138">System.Boolean</span></span>

## <span data-ttu-id="ec15e-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec15e-139">NOTES</span></span>

## <span data-ttu-id="ec15e-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec15e-140">RELATED LINKS</span></span>

[<span data-ttu-id="ec15e-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec15e-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec15e-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec15e-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec15e-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec15e-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ec15e-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ec15e-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

