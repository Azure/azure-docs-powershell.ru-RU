---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407687"
---
# <span data-ttu-id="8d192-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d192-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="8d192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d192-102">SYNOPSIS</span></span>
<span data-ttu-id="8d192-103">Отмена запущенного развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="8d192-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="8d192-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d192-104">SYNTAX</span></span>

### <span data-ttu-id="8d192-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d192-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d192-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8d192-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d192-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d192-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d192-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d192-108">DESCRIPTION</span></span>
<span data-ttu-id="8d192-109">С **его использованием** можно отменить развертывание, которое было запущено, но не завершено в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="8d192-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="8d192-110">Чтобы завершить развертывание, необходимо иметь неполное состояние подготовка, например подготовка, а не завершалось состояние, например "Подготовка" или "Сбой".</span><span class="sxs-lookup"><span data-stu-id="8d192-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="8d192-111">Чтобы создать развертывание в области клиента, используйте New-AzTenantDeployment управления.</span><span class="sxs-lookup"><span data-stu-id="8d192-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="8d192-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d192-112">EXAMPLES</span></span>

### <span data-ttu-id="8d192-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d192-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="8d192-114">Эта команда отменяет развертывание "deployment01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="8d192-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="8d192-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d192-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="8d192-116">Эта команда получает "deployment01" в текущей области клиента и отменяет его.</span><span class="sxs-lookup"><span data-stu-id="8d192-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="8d192-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d192-117">PARAMETERS</span></span>

### <span data-ttu-id="8d192-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d192-118">-DefaultProfile</span></span>
<span data-ttu-id="8d192-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d192-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d192-120">-Id</span><span class="sxs-lookup"><span data-stu-id="8d192-120">-Id</span></span>
<span data-ttu-id="8d192-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="8d192-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="8d192-122">пример: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="8d192-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="8d192-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d192-123">-InputObject</span></span>
<span data-ttu-id="8d192-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="8d192-124">The deployment object.</span></span>

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

### <span data-ttu-id="8d192-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8d192-125">-Name</span></span>
<span data-ttu-id="8d192-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="8d192-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="8d192-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d192-127">-PassThru</span></span>
<span data-ttu-id="8d192-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="8d192-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8d192-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="8d192-129">-Pre</span></span>
<span data-ttu-id="8d192-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="8d192-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8d192-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d192-131">-Confirm</span></span>
<span data-ttu-id="8d192-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8d192-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d192-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d192-133">-WhatIf</span></span>
<span data-ttu-id="8d192-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d192-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d192-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d192-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d192-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d192-136">CommonParameters</span></span>
<span data-ttu-id="8d192-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d192-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d192-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d192-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d192-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d192-139">INPUTS</span></span>

### <span data-ttu-id="8d192-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="8d192-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8d192-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d192-141">OUTPUTS</span></span>

### <span data-ttu-id="8d192-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d192-142">System.Boolean</span></span>

## <span data-ttu-id="8d192-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d192-143">NOTES</span></span>

## <span data-ttu-id="8d192-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d192-144">RELATED LINKS</span></span>
