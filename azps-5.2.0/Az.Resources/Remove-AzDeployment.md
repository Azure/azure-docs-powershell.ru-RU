---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408172"
---
# <span data-ttu-id="2cf72-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2cf72-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="2cf72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf72-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf72-103">Удаление развертывания и всех связанных с ним операций</span><span class="sxs-lookup"><span data-stu-id="2cf72-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="2cf72-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2cf72-104">SYNTAX</span></span>

### <span data-ttu-id="2cf72-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cf72-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf72-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2cf72-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf72-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2cf72-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf72-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cf72-108">DESCRIPTION</span></span>
<span data-ttu-id="2cf72-109">С **его использованием** развертывание Azure удаляется из области действия подписки и связанных с ней операций.</span><span class="sxs-lookup"><span data-stu-id="2cf72-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="2cf72-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2cf72-110">EXAMPLES</span></span>

### <span data-ttu-id="2cf72-111">Пример 1. Удаление развертывания с заданным именем</span><span class="sxs-lookup"><span data-stu-id="2cf72-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="2cf72-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="2cf72-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="2cf72-113">Пример 2. Получить и удалить развертывание</span><span class="sxs-lookup"><span data-stu-id="2cf72-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="2cf72-114">Эта команда получает "RolesDeployment" для развертывания в текущей области действия подписки и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="2cf72-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="2cf72-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cf72-115">PARAMETERS</span></span>

### <span data-ttu-id="2cf72-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cf72-116">-AsJob</span></span>
<span data-ttu-id="2cf72-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2cf72-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cf72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf72-118">-DefaultProfile</span></span>
<span data-ttu-id="2cf72-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf72-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf72-120">-Id</span><span class="sxs-lookup"><span data-stu-id="2cf72-120">-Id</span></span>
<span data-ttu-id="2cf72-121">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="2cf72-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2cf72-122">пример: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2cf72-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="2cf72-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf72-123">-InputObject</span></span>
<span data-ttu-id="2cf72-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="2cf72-124">The deployment object.</span></span>

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

### <span data-ttu-id="2cf72-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2cf72-125">-Name</span></span>
<span data-ttu-id="2cf72-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="2cf72-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="2cf72-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cf72-127">-PassThru</span></span>
<span data-ttu-id="2cf72-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2cf72-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2cf72-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="2cf72-129">-Pre</span></span>
<span data-ttu-id="2cf72-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="2cf72-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2cf72-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cf72-131">-Confirm</span></span>
<span data-ttu-id="2cf72-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2cf72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf72-133">-WhatIf</span></span>
<span data-ttu-id="2cf72-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf72-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2cf72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf72-136">CommonParameters</span></span>
<span data-ttu-id="2cf72-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf72-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cf72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf72-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cf72-139">INPUTS</span></span>

### <span data-ttu-id="2cf72-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="2cf72-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2cf72-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2cf72-141">OUTPUTS</span></span>

### <span data-ttu-id="2cf72-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2cf72-142">System.Boolean</span></span>

## <span data-ttu-id="2cf72-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2cf72-143">NOTES</span></span>

## <span data-ttu-id="2cf72-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cf72-144">RELATED LINKS</span></span>
