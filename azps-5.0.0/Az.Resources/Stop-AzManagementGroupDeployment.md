---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247028"
---
# <span data-ttu-id="00025-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00025-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="00025-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00025-102">SYNOPSIS</span></span>
<span data-ttu-id="00025-103">Отмена выполняющегося развертывания в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="00025-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="00025-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00025-104">SYNTAX</span></span>

### <span data-ttu-id="00025-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00025-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00025-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="00025-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00025-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="00025-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00025-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00025-108">DESCRIPTION</span></span>
<span data-ttu-id="00025-109">Командлет **Stop-AzManagementGroupDeployment** отменяет развертывание, которое было начато, но не завершено в группе управления.</span><span class="sxs-lookup"><span data-stu-id="00025-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="00025-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="00025-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="00025-111">Чтобы создать развертывание в группе управления, используйте командлет New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="00025-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="00025-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00025-112">EXAMPLES</span></span>

### <span data-ttu-id="00025-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00025-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="00025-114">Эта команда отменяет запущенное развертывание "deployment01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="00025-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="00025-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00025-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="00025-116">Эта команда получает развертывание "deployment01" в группе управления "myMG" и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="00025-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="00025-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00025-117">PARAMETERS</span></span>

### <span data-ttu-id="00025-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00025-118">-DefaultProfile</span></span>
<span data-ttu-id="00025-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00025-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00025-120">-ID</span><span class="sxs-lookup"><span data-stu-id="00025-120">-Id</span></span>
<span data-ttu-id="00025-121">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="00025-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="00025-122">Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="00025-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="00025-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00025-123">-InputObject</span></span>
<span data-ttu-id="00025-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="00025-124">The deployment object.</span></span>

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

### <span data-ttu-id="00025-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="00025-125">-ManagementGroupId</span></span>
<span data-ttu-id="00025-126">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="00025-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00025-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00025-127">-Name</span></span>
<span data-ttu-id="00025-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="00025-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00025-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00025-129">-PassThru</span></span>
<span data-ttu-id="00025-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="00025-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="00025-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="00025-131">-Pre</span></span>
<span data-ttu-id="00025-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="00025-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="00025-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00025-133">-Confirm</span></span>
<span data-ttu-id="00025-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00025-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00025-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00025-135">-WhatIf</span></span>
<span data-ttu-id="00025-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00025-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00025-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00025-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00025-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00025-138">CommonParameters</span></span>
<span data-ttu-id="00025-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00025-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00025-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00025-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00025-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00025-141">INPUTS</span></span>

### <span data-ttu-id="00025-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="00025-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="00025-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00025-143">OUTPUTS</span></span>

### <span data-ttu-id="00025-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00025-144">System.Boolean</span></span>

## <span data-ttu-id="00025-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="00025-145">NOTES</span></span>

## <span data-ttu-id="00025-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00025-146">RELATED LINKS</span></span>
