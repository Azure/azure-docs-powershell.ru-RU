---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247026"
---
# <span data-ttu-id="857ac-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="857ac-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="857ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="857ac-102">SYNOPSIS</span></span>
<span data-ttu-id="857ac-103">Отмена выполняющегося развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="857ac-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="857ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="857ac-104">SYNTAX</span></span>

### <span data-ttu-id="857ac-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="857ac-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="857ac-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="857ac-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="857ac-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="857ac-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="857ac-108">DESCRIPTION</span></span>
<span data-ttu-id="857ac-109">Командлет **Stop-AzTenantDeployment** отменяет развертывание, которое началось, но не завершено в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="857ac-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="857ac-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="857ac-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="857ac-111">Чтобы создать развертывание в области клиента, используйте командлет New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="857ac-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="857ac-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="857ac-112">EXAMPLES</span></span>

### <span data-ttu-id="857ac-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="857ac-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="857ac-114">Эта команда отменяет запущенное развертывание "deployment01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="857ac-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="857ac-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="857ac-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="857ac-116">Эта команда получает развертывание "deployment01" в текущей области клиента и отменяет его.</span><span class="sxs-lookup"><span data-stu-id="857ac-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="857ac-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="857ac-117">PARAMETERS</span></span>

### <span data-ttu-id="857ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857ac-118">-DefaultProfile</span></span>
<span data-ttu-id="857ac-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="857ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857ac-120">-ID</span><span class="sxs-lookup"><span data-stu-id="857ac-120">-Id</span></span>
<span data-ttu-id="857ac-121">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="857ac-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="857ac-122">Пример:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="857ac-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="857ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="857ac-123">-InputObject</span></span>
<span data-ttu-id="857ac-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="857ac-124">The deployment object.</span></span>

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

### <span data-ttu-id="857ac-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="857ac-125">-Name</span></span>
<span data-ttu-id="857ac-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="857ac-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="857ac-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="857ac-127">-PassThru</span></span>
<span data-ttu-id="857ac-128">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="857ac-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="857ac-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="857ac-129">-Pre</span></span>
<span data-ttu-id="857ac-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="857ac-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="857ac-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="857ac-131">-Confirm</span></span>
<span data-ttu-id="857ac-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="857ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857ac-133">-WhatIf</span></span>
<span data-ttu-id="857ac-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="857ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857ac-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="857ac-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857ac-136">CommonParameters</span></span>
<span data-ttu-id="857ac-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="857ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857ac-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="857ac-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857ac-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="857ac-139">INPUTS</span></span>

### <span data-ttu-id="857ac-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="857ac-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="857ac-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="857ac-141">OUTPUTS</span></span>

### <span data-ttu-id="857ac-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="857ac-142">System.Boolean</span></span>

## <span data-ttu-id="857ac-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="857ac-143">NOTES</span></span>

## <span data-ttu-id="857ac-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="857ac-144">RELATED LINKS</span></span>