---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407655"
---
# <span data-ttu-id="9d432-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d432-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="9d432-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d432-102">SYNOPSIS</span></span>
<span data-ttu-id="9d432-103">Отмена развертывания в группе управления</span><span class="sxs-lookup"><span data-stu-id="9d432-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="9d432-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d432-104">SYNTAX</span></span>

### <span data-ttu-id="9d432-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d432-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d432-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9d432-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d432-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d432-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d432-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d432-108">DESCRIPTION</span></span>
<span data-ttu-id="9d432-109">Выполнение **команды Stop-AzManagementGroupDeployment** отменяет развертывание, которое началось, но не завершено в группе управления.</span><span class="sxs-lookup"><span data-stu-id="9d432-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="9d432-110">Чтобы завершить развертывание, необходимо иметь неполное состояние подготовка, например подготовка, а не завершалось состояние, например "Подготовка" или "Сбой".</span><span class="sxs-lookup"><span data-stu-id="9d432-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="9d432-111">Чтобы создать развертывание в группе управления, воспользуйтесь New-AzManagementGroupDeployment управления.</span><span class="sxs-lookup"><span data-stu-id="9d432-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="9d432-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d432-112">EXAMPLES</span></span>

### <span data-ttu-id="9d432-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9d432-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="9d432-114">Эта команда отменяет развертывание "deployment01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="9d432-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="9d432-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9d432-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="9d432-116">Эта команда получает "deployment01" в группе управления MyMG и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="9d432-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="9d432-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d432-117">PARAMETERS</span></span>

### <span data-ttu-id="9d432-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d432-118">-DefaultProfile</span></span>
<span data-ttu-id="9d432-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d432-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d432-120">-Id</span><span class="sxs-lookup"><span data-stu-id="9d432-120">-Id</span></span>
<span data-ttu-id="9d432-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="9d432-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="9d432-122">пример: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="9d432-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="9d432-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d432-123">-InputObject</span></span>
<span data-ttu-id="9d432-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d432-124">The deployment object.</span></span>

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

### <span data-ttu-id="9d432-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9d432-125">-ManagementGroupId</span></span>
<span data-ttu-id="9d432-126">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="9d432-126">The management group id.</span></span>

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

### <span data-ttu-id="9d432-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9d432-127">-Name</span></span>
<span data-ttu-id="9d432-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d432-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="9d432-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d432-129">-PassThru</span></span>
<span data-ttu-id="9d432-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="9d432-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9d432-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d432-131">-Pre</span></span>
<span data-ttu-id="9d432-132">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="9d432-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9d432-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d432-133">-Confirm</span></span>
<span data-ttu-id="9d432-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d432-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d432-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d432-135">-WhatIf</span></span>
<span data-ttu-id="9d432-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d432-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d432-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d432-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d432-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d432-138">CommonParameters</span></span>
<span data-ttu-id="9d432-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d432-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d432-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d432-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d432-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d432-141">INPUTS</span></span>

### <span data-ttu-id="9d432-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="9d432-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9d432-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d432-143">OUTPUTS</span></span>

### <span data-ttu-id="9d432-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d432-144">System.Boolean</span></span>

## <span data-ttu-id="9d432-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d432-145">NOTES</span></span>

## <span data-ttu-id="9d432-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d432-146">RELATED LINKS</span></span>
