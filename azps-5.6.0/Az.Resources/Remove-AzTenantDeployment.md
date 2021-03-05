---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979400"
---
# <span data-ttu-id="8ab08-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8ab08-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="8ab08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ab08-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab08-103">Развертывание в области клиента и все связанные с ним операции удаляются.</span><span class="sxs-lookup"><span data-stu-id="8ab08-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="8ab08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ab08-104">SYNTAX</span></span>

### <span data-ttu-id="8ab08-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ab08-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab08-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8ab08-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab08-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ab08-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab08-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ab08-108">DESCRIPTION</span></span>
<span data-ttu-id="8ab08-109">При **этом развертывание Azure** удаляется из текущей области клиента и всех связанных с ним операций.</span><span class="sxs-lookup"><span data-stu-id="8ab08-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="8ab08-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ab08-110">EXAMPLES</span></span>

### <span data-ttu-id="8ab08-111">Пример 1. Удаление развертывания с заданным именем</span><span class="sxs-lookup"><span data-stu-id="8ab08-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="8ab08-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="8ab08-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="8ab08-113">Пример 2. Получить и удалить развертывание</span><span class="sxs-lookup"><span data-stu-id="8ab08-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="8ab08-114">Эта команда получает "RolesDeployment" для развертывания в текущей области клиента и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="8ab08-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="8ab08-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ab08-115">PARAMETERS</span></span>

### <span data-ttu-id="8ab08-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ab08-116">-AsJob</span></span>
<span data-ttu-id="8ab08-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8ab08-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ab08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab08-118">-DefaultProfile</span></span>
<span data-ttu-id="8ab08-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ab08-120">-Id</span><span class="sxs-lookup"><span data-stu-id="8ab08-120">-Id</span></span>
<span data-ttu-id="8ab08-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="8ab08-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="8ab08-122">пример: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="8ab08-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="8ab08-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ab08-123">-InputObject</span></span>
<span data-ttu-id="8ab08-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ab08-124">The deployment object.</span></span>

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

### <span data-ttu-id="8ab08-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8ab08-125">-Name</span></span>
<span data-ttu-id="8ab08-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ab08-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab08-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ab08-127">-PassThru</span></span>
<span data-ttu-id="8ab08-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="8ab08-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8ab08-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ab08-129">-Pre</span></span>
<span data-ttu-id="8ab08-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="8ab08-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ab08-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ab08-131">-Confirm</span></span>
<span data-ttu-id="8ab08-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab08-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab08-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab08-133">-WhatIf</span></span>
<span data-ttu-id="8ab08-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab08-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab08-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ab08-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab08-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab08-136">CommonParameters</span></span>
<span data-ttu-id="8ab08-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab08-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab08-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ab08-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab08-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ab08-139">INPUTS</span></span>

### <span data-ttu-id="8ab08-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="8ab08-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8ab08-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ab08-141">OUTPUTS</span></span>

### <span data-ttu-id="8ab08-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ab08-142">System.Boolean</span></span>

## <span data-ttu-id="8ab08-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ab08-143">NOTES</span></span>

## <span data-ttu-id="8ab08-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ab08-144">RELATED LINKS</span></span>
