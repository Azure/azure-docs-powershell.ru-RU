---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235937"
---
# <span data-ttu-id="38efb-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38efb-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="38efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38efb-102">SYNOPSIS</span></span>
<span data-ttu-id="38efb-103">Удаление развертывания в группе управления и всех связанных с ней операций</span><span class="sxs-lookup"><span data-stu-id="38efb-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="38efb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38efb-104">SYNTAX</span></span>

### <span data-ttu-id="38efb-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38efb-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38efb-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="38efb-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38efb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="38efb-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38efb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38efb-108">DESCRIPTION</span></span>
<span data-ttu-id="38efb-109">При этом развертывание Azure в группе управления и все связанные с ней операции удаляются с использованием команды **Remove-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="38efb-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="38efb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38efb-110">EXAMPLES</span></span>

### <span data-ttu-id="38efb-111">Пример 1. Удаление развертывания с заданным именем</span><span class="sxs-lookup"><span data-stu-id="38efb-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="38efb-112">Эта команда удаляет развертывание "RolesDeployment" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="38efb-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="38efb-113">Пример 2. Получить и удалить развертывание</span><span class="sxs-lookup"><span data-stu-id="38efb-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="38efb-114">Эта команда получает "RolesDeployment" в группе управления myMG и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="38efb-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="38efb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38efb-115">PARAMETERS</span></span>

### <span data-ttu-id="38efb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38efb-116">-AsJob</span></span>
<span data-ttu-id="38efb-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="38efb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38efb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38efb-118">-DefaultProfile</span></span>
<span data-ttu-id="38efb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38efb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38efb-120">-Id</span><span class="sxs-lookup"><span data-stu-id="38efb-120">-Id</span></span>
<span data-ttu-id="38efb-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="38efb-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="38efb-122">пример: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="38efb-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38efb-123">-InputObject</span></span>
<span data-ttu-id="38efb-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="38efb-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38efb-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="38efb-125">-ManagementGroupId</span></span>
<span data-ttu-id="38efb-126">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="38efb-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="38efb-127">-Name</span></span>
<span data-ttu-id="38efb-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="38efb-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38efb-129">-PassThru</span></span>
<span data-ttu-id="38efb-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="38efb-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="38efb-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="38efb-131">-Pre</span></span>
<span data-ttu-id="38efb-132">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="38efb-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="38efb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38efb-133">-Confirm</span></span>
<span data-ttu-id="38efb-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="38efb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38efb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38efb-135">-WhatIf</span></span>
<span data-ttu-id="38efb-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38efb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38efb-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38efb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38efb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38efb-138">CommonParameters</span></span>
<span data-ttu-id="38efb-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38efb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38efb-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38efb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38efb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38efb-141">INPUTS</span></span>

### <span data-ttu-id="38efb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="38efb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="38efb-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38efb-143">OUTPUTS</span></span>

### <span data-ttu-id="38efb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38efb-144">System.Boolean</span></span>

## <span data-ttu-id="38efb-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38efb-145">NOTES</span></span>

## <span data-ttu-id="38efb-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38efb-146">RELATED LINKS</span></span>
