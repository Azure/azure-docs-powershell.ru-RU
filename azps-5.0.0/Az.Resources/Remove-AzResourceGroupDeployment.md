---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249829"
---
# <span data-ttu-id="30636-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30636-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="30636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30636-102">SYNOPSIS</span></span>
<span data-ttu-id="30636-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="30636-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="30636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30636-104">SYNTAX</span></span>

### <span data-ttu-id="30636-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30636-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30636-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="30636-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30636-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30636-107">DESCRIPTION</span></span>

<span data-ttu-id="30636-108">Командлет **Remove-AzResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="30636-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="30636-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30636-109">EXAMPLES</span></span>

### <span data-ttu-id="30636-110">Пример 1: Удаление развертывания группы ресурсов с ResourceId</span><span class="sxs-lookup"><span data-stu-id="30636-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="30636-111">Эта команда удаляет развертывание группы ресурсов с полным идентификатором ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="30636-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="30636-112">Успешное удаление возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="30636-112">Successful removal returns true.</span></span>

### <span data-ttu-id="30636-113">Пример 2: Удаление развертывания группы ресурсов с ResourceGroupName и ResourceName</span><span class="sxs-lookup"><span data-stu-id="30636-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="30636-114">Эта команда удаляет развертывание группы ресурсов с предоставленными ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="30636-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="30636-115">Успешное удаление возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="30636-115">Successful removal returns true.</span></span>

## <span data-ttu-id="30636-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30636-116">PARAMETERS</span></span>

### <span data-ttu-id="30636-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30636-117">-DefaultProfile</span></span>
<span data-ttu-id="30636-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30636-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30636-119">-ID</span><span class="sxs-lookup"><span data-stu-id="30636-119">-Id</span></span>
<span data-ttu-id="30636-120">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30636-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="30636-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30636-121">-Name</span></span>
<span data-ttu-id="30636-122">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30636-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="30636-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="30636-123">-Pre</span></span>
<span data-ttu-id="30636-124">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="30636-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="30636-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30636-125">-ResourceGroupName</span></span>
<span data-ttu-id="30636-126">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30636-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="30636-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30636-127">-Confirm</span></span>
<span data-ttu-id="30636-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30636-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30636-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30636-129">-WhatIf</span></span>
<span data-ttu-id="30636-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30636-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30636-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30636-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30636-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30636-132">CommonParameters</span></span>
<span data-ttu-id="30636-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30636-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30636-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30636-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30636-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30636-135">INPUTS</span></span>

### <span data-ttu-id="30636-136">System. String</span><span class="sxs-lookup"><span data-stu-id="30636-136">System.String</span></span>

## <span data-ttu-id="30636-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30636-137">OUTPUTS</span></span>

### <span data-ttu-id="30636-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30636-138">System.Boolean</span></span>

## <span data-ttu-id="30636-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="30636-139">NOTES</span></span>

## <span data-ttu-id="30636-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30636-140">RELATED LINKS</span></span>

[<span data-ttu-id="30636-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30636-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="30636-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30636-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="30636-143">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30636-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="30636-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="30636-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


