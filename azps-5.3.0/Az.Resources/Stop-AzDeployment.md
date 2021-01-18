---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505154"
---
# <span data-ttu-id="6dc8e-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6dc8e-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="6dc8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc8e-103">Отмена запущенного развертывания</span><span class="sxs-lookup"><span data-stu-id="6dc8e-103">Cancel a running deployment</span></span>

## <span data-ttu-id="6dc8e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6dc8e-104">SYNTAX</span></span>

### <span data-ttu-id="6dc8e-105">StopByDeploymentName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6dc8e-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dc8e-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6dc8e-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dc8e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="6dc8e-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc8e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dc8e-108">DESCRIPTION</span></span>
<span data-ttu-id="6dc8e-109">**Из-за настройки Stop-AzDeployment** развертывание отменяется в рамках подписки, которое началось, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="6dc8e-110">Чтобы завершить развертывание, необходимо иметь неполное состояние подготовка, например подготовка, а не завершалось состояние, например "Подготовка" или "Сбой".</span><span class="sxs-lookup"><span data-stu-id="6dc8e-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="6dc8e-111">Чтобы создать развертывание в рамках подписки, воспользуйтесь New-AzDeployment..</span><span class="sxs-lookup"><span data-stu-id="6dc8e-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="6dc8e-112">Этот cmdlet останавливает только одно развертывание.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="6dc8e-113">Используйте параметр *Name,* чтобы остановить определенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="6dc8e-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6dc8e-114">EXAMPLES</span></span>

### <span data-ttu-id="6dc8e-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6dc8e-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="6dc8e-116">Эта команда отменяет развертывание "deployment01" в текущей области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="6dc8e-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6dc8e-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="6dc8e-118">Эта команда получает "deployment01" в текущей области подписки и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="6dc8e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dc8e-119">PARAMETERS</span></span>

### <span data-ttu-id="6dc8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc8e-120">-DefaultProfile</span></span>
<span data-ttu-id="6dc8e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc8e-122">-Id</span><span class="sxs-lookup"><span data-stu-id="6dc8e-122">-Id</span></span>
<span data-ttu-id="6dc8e-123">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6dc8e-124">пример: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6dc8e-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="6dc8e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dc8e-125">-InputObject</span></span>
<span data-ttu-id="6dc8e-126">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-126">The deployment object.</span></span>

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

### <span data-ttu-id="6dc8e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6dc8e-127">-Name</span></span>
<span data-ttu-id="6dc8e-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="6dc8e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dc8e-129">-PassThru</span></span>
<span data-ttu-id="6dc8e-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6dc8e-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6dc8e-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="6dc8e-131">-Pre</span></span>
<span data-ttu-id="6dc8e-132">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6dc8e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dc8e-133">-Confirm</span></span>
<span data-ttu-id="6dc8e-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc8e-135">-WhatIf</span></span>
<span data-ttu-id="6dc8e-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc8e-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc8e-138">CommonParameters</span></span>
<span data-ttu-id="6dc8e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc8e-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dc8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc8e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dc8e-141">INPUTS</span></span>

### <span data-ttu-id="6dc8e-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="6dc8e-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6dc8e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6dc8e-143">OUTPUTS</span></span>

### <span data-ttu-id="6dc8e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6dc8e-144">System.Boolean</span></span>

## <span data-ttu-id="6dc8e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6dc8e-145">NOTES</span></span>

## <span data-ttu-id="6dc8e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dc8e-146">RELATED LINKS</span></span>
