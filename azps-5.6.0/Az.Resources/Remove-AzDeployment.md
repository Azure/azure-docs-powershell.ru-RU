---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 9aeba4d3d7b716910ddab1e63713bd6ef2bce17a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003107"
---
# <span data-ttu-id="d9807-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d9807-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="d9807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9807-102">SYNOPSIS</span></span>
<span data-ttu-id="d9807-103">Удаление развертывания и всех связанных с ним операций</span><span class="sxs-lookup"><span data-stu-id="d9807-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="d9807-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9807-104">SYNTAX</span></span>

### <span data-ttu-id="d9807-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9807-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9807-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d9807-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9807-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9807-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9807-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9807-108">DESCRIPTION</span></span>
<span data-ttu-id="d9807-109">При **этом развертывание Azure удаляется** из области действия подписки и связанных с ней операций.</span><span class="sxs-lookup"><span data-stu-id="d9807-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="d9807-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9807-110">EXAMPLES</span></span>

### <span data-ttu-id="d9807-111">Пример 1. Удаление развертывания с заданным именем</span><span class="sxs-lookup"><span data-stu-id="d9807-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="d9807-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="d9807-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="d9807-113">Пример 2. Получить и удалить развертывание</span><span class="sxs-lookup"><span data-stu-id="d9807-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="d9807-114">Эта команда получает "RolesDeployment" для развертывания в текущей области действия подписки и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="d9807-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="d9807-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9807-115">PARAMETERS</span></span>

### <span data-ttu-id="d9807-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9807-116">-AsJob</span></span>
<span data-ttu-id="d9807-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d9807-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9807-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9807-118">-DefaultProfile</span></span>
<span data-ttu-id="d9807-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9807-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9807-120">-Id</span><span class="sxs-lookup"><span data-stu-id="d9807-120">-Id</span></span>
<span data-ttu-id="d9807-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="d9807-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d9807-122">пример: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d9807-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="d9807-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9807-123">-InputObject</span></span>
<span data-ttu-id="d9807-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="d9807-124">The deployment object.</span></span>

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

### <span data-ttu-id="d9807-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d9807-125">-Name</span></span>
<span data-ttu-id="d9807-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="d9807-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="d9807-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9807-127">-PassThru</span></span>
<span data-ttu-id="d9807-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d9807-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d9807-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9807-129">-Pre</span></span>
<span data-ttu-id="d9807-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="d9807-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9807-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9807-131">-Confirm</span></span>
<span data-ttu-id="d9807-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9807-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9807-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9807-133">-WhatIf</span></span>
<span data-ttu-id="d9807-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9807-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9807-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d9807-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9807-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9807-136">CommonParameters</span></span>
<span data-ttu-id="d9807-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9807-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9807-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9807-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9807-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9807-139">INPUTS</span></span>

### <span data-ttu-id="d9807-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="d9807-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d9807-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9807-141">OUTPUTS</span></span>

### <span data-ttu-id="d9807-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9807-142">System.Boolean</span></span>

## <span data-ttu-id="d9807-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9807-143">NOTES</span></span>

## <span data-ttu-id="d9807-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9807-144">RELATED LINKS</span></span>
