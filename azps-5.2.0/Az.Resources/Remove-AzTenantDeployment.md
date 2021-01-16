---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407660"
---
# <span data-ttu-id="0f243-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0f243-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="0f243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f243-102">SYNOPSIS</span></span>
<span data-ttu-id="0f243-103">Удаление развертывания в клиенте и всех связанных с ним операций</span><span class="sxs-lookup"><span data-stu-id="0f243-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="0f243-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f243-104">SYNTAX</span></span>

### <span data-ttu-id="0f243-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f243-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f243-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0f243-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f243-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f243-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f243-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f243-108">DESCRIPTION</span></span>
<span data-ttu-id="0f243-109">При **этом развертывание Azure** удаляется из текущей области клиента и всех связанных с ним операций.</span><span class="sxs-lookup"><span data-stu-id="0f243-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="0f243-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f243-110">EXAMPLES</span></span>

### <span data-ttu-id="0f243-111">Пример 1. Удаление развертывания с заданным именем</span><span class="sxs-lookup"><span data-stu-id="0f243-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="0f243-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="0f243-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="0f243-113">Пример 2. Получить и удалить развертывание</span><span class="sxs-lookup"><span data-stu-id="0f243-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="0f243-114">Эта команда получает "RolesDeployment" развертывания в текущей области клиента и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="0f243-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="0f243-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f243-115">PARAMETERS</span></span>

### <span data-ttu-id="0f243-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f243-116">-AsJob</span></span>
<span data-ttu-id="0f243-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0f243-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f243-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f243-118">-DefaultProfile</span></span>
<span data-ttu-id="0f243-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f243-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f243-120">-Id</span><span class="sxs-lookup"><span data-stu-id="0f243-120">-Id</span></span>
<span data-ttu-id="0f243-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="0f243-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0f243-122">пример: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0f243-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0f243-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f243-123">-InputObject</span></span>
<span data-ttu-id="0f243-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f243-124">The deployment object.</span></span>

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

### <span data-ttu-id="0f243-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0f243-125">-Name</span></span>
<span data-ttu-id="0f243-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f243-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="0f243-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f243-127">-PassThru</span></span>
<span data-ttu-id="0f243-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0f243-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0f243-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f243-129">-Pre</span></span>
<span data-ttu-id="0f243-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="0f243-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0f243-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f243-131">-Confirm</span></span>
<span data-ttu-id="0f243-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f243-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f243-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f243-133">-WhatIf</span></span>
<span data-ttu-id="0f243-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f243-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f243-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0f243-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f243-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f243-136">CommonParameters</span></span>
<span data-ttu-id="0f243-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f243-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f243-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f243-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f243-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f243-139">INPUTS</span></span>

### <span data-ttu-id="0f243-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="0f243-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0f243-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f243-141">OUTPUTS</span></span>

### <span data-ttu-id="0f243-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f243-142">System.Boolean</span></span>

## <span data-ttu-id="0f243-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f243-143">NOTES</span></span>

## <span data-ttu-id="0f243-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f243-144">RELATED LINKS</span></span>
