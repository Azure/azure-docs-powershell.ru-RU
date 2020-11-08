---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235414"
---
# <span data-ttu-id="eee74-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eee74-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="eee74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eee74-102">SYNOPSIS</span></span>
<span data-ttu-id="eee74-103">Удаляет развертывание группы ресурсов и связанные с ней операции.</span><span class="sxs-lookup"><span data-stu-id="eee74-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="eee74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eee74-104">SYNTAX</span></span>

### <span data-ttu-id="eee74-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eee74-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee74-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="eee74-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee74-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee74-107">DESCRIPTION</span></span>

<span data-ttu-id="eee74-108">Командлет **Remove-AzResourceGroupDeployment** удаляет развертывание группы ресурсов Azure и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="eee74-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="eee74-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eee74-109">EXAMPLES</span></span>

### <span data-ttu-id="eee74-110">Пример 1: Удаление развертывания группы ресурсов с ResourceId</span><span class="sxs-lookup"><span data-stu-id="eee74-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="eee74-111">Эта команда удаляет развертывание группы ресурсов с полным идентификатором ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="eee74-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="eee74-112">Успешное удаление возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="eee74-112">Successful removal returns true.</span></span>

### <span data-ttu-id="eee74-113">Пример 2: Удаление развертывания группы ресурсов с ResourceGroupName и ResourceName</span><span class="sxs-lookup"><span data-stu-id="eee74-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="eee74-114">Эта команда удаляет развертывание группы ресурсов с предоставленными ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="eee74-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="eee74-115">Успешное удаление возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="eee74-115">Successful removal returns true.</span></span>

## <span data-ttu-id="eee74-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eee74-116">PARAMETERS</span></span>

### <span data-ttu-id="eee74-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eee74-117">-ApiVersion</span></span>
<span data-ttu-id="eee74-118">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee74-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="eee74-119">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eee74-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee74-120">-DefaultProfile</span></span>
<span data-ttu-id="eee74-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eee74-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eee74-122">-ID</span><span class="sxs-lookup"><span data-stu-id="eee74-122">-Id</span></span>
<span data-ttu-id="eee74-123">Указывает идентификатор развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eee74-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="eee74-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eee74-124">-Name</span></span>
<span data-ttu-id="eee74-125">Указывает имя развертывания группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eee74-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="eee74-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="eee74-126">-Pre</span></span>
<span data-ttu-id="eee74-127">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="eee74-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eee74-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee74-128">-ResourceGroupName</span></span>
<span data-ttu-id="eee74-129">Указывает имя удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee74-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="eee74-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee74-130">-Confirm</span></span>
<span data-ttu-id="eee74-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eee74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee74-132">-WhatIf</span></span>
<span data-ttu-id="eee74-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eee74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee74-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eee74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee74-135">CommonParameters</span></span>
<span data-ttu-id="eee74-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eee74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee74-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eee74-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee74-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eee74-138">INPUTS</span></span>

### <span data-ttu-id="eee74-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eee74-139">System.String</span></span>

## <span data-ttu-id="eee74-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee74-140">OUTPUTS</span></span>

### <span data-ttu-id="eee74-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eee74-141">System.Boolean</span></span>

## <span data-ttu-id="eee74-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eee74-142">NOTES</span></span>

## <span data-ttu-id="eee74-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eee74-143">RELATED LINKS</span></span>

[<span data-ttu-id="eee74-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eee74-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="eee74-145">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eee74-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="eee74-146">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eee74-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="eee74-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="eee74-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


