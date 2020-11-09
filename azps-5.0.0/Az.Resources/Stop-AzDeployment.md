---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247034"
---
# <span data-ttu-id="f8100-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f8100-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="f8100-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8100-102">SYNOPSIS</span></span>
<span data-ttu-id="f8100-103">Отмена выполняющегося развертывания</span><span class="sxs-lookup"><span data-stu-id="f8100-103">Cancel a running deployment</span></span>

## <span data-ttu-id="f8100-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8100-104">SYNTAX</span></span>

### <span data-ttu-id="f8100-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8100-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8100-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f8100-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8100-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="f8100-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8100-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8100-108">DESCRIPTION</span></span>
<span data-ttu-id="f8100-109">Командлет **Stop-AzDeployment** отменяет развертывание в области подписки, которая была запущена, но не завершена.</span><span class="sxs-lookup"><span data-stu-id="f8100-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="f8100-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="f8100-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="f8100-111">Чтобы создать развертывание в области подписки, используйте командлет New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="f8100-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="f8100-112">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="f8100-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="f8100-113">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="f8100-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="f8100-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8100-114">EXAMPLES</span></span>

### <span data-ttu-id="f8100-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8100-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="f8100-116">Эта команда отменяет запущенное развертывание "deployment01" в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="f8100-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="f8100-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f8100-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="f8100-118">Эта команда получает развертывание "deployment01" в текущей области подписки и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="f8100-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="f8100-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8100-119">PARAMETERS</span></span>

### <span data-ttu-id="f8100-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8100-120">-DefaultProfile</span></span>
<span data-ttu-id="f8100-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8100-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8100-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f8100-122">-Id</span></span>
<span data-ttu-id="f8100-123">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f8100-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f8100-124">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f8100-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8100-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8100-125">-InputObject</span></span>
<span data-ttu-id="f8100-126">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="f8100-126">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8100-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8100-127">-Name</span></span>
<span data-ttu-id="f8100-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="f8100-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8100-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8100-129">-PassThru</span></span>
<span data-ttu-id="f8100-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="f8100-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f8100-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f8100-131">-Pre</span></span>
<span data-ttu-id="f8100-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="f8100-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f8100-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8100-133">-Confirm</span></span>
<span data-ttu-id="f8100-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8100-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8100-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8100-135">-WhatIf</span></span>
<span data-ttu-id="f8100-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8100-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8100-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8100-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8100-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8100-138">CommonParameters</span></span>
<span data-ttu-id="f8100-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8100-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8100-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8100-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8100-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8100-141">INPUTS</span></span>

### <span data-ttu-id="f8100-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f8100-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f8100-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8100-143">OUTPUTS</span></span>

### <span data-ttu-id="f8100-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8100-144">System.Boolean</span></span>

## <span data-ttu-id="f8100-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8100-145">NOTES</span></span>

## <span data-ttu-id="f8100-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8100-146">RELATED LINKS</span></span>