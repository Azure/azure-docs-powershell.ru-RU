---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 2fbe6f707fe76e83591fe23c71b4de29a8bbf91c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242897"
---
# <span data-ttu-id="64633-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="64633-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="64633-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64633-102">SYNOPSIS</span></span>
<span data-ttu-id="64633-103">Удаление развертывания и связанных с ней операций</span><span class="sxs-lookup"><span data-stu-id="64633-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="64633-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64633-104">SYNTAX</span></span>

### <span data-ttu-id="64633-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64633-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64633-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="64633-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64633-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="64633-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64633-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64633-108">DESCRIPTION</span></span>
<span data-ttu-id="64633-109">Командлет **Remove-AzDeployment** удаляет развертывание Azure в области подписок и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="64633-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="64633-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64633-110">EXAMPLES</span></span>

### <span data-ttu-id="64633-111">Пример 1: Удаление развертывания с указанным именем</span><span class="sxs-lookup"><span data-stu-id="64633-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="64633-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="64633-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="64633-113">Пример 2: получение развертывания и его удаление</span><span class="sxs-lookup"><span data-stu-id="64633-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="64633-114">Эта команда получает развертывание "RolesDeployment" в текущей области подписки и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="64633-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="64633-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64633-115">PARAMETERS</span></span>

### <span data-ttu-id="64633-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="64633-116">-ApiVersion</span></span>
<span data-ttu-id="64633-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64633-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="64633-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="64633-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64633-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64633-119">-AsJob</span></span>
<span data-ttu-id="64633-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="64633-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64633-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64633-121">-DefaultProfile</span></span>
<span data-ttu-id="64633-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64633-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64633-123">-ID</span><span class="sxs-lookup"><span data-stu-id="64633-123">-Id</span></span>
<span data-ttu-id="64633-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="64633-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="64633-125">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="64633-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="64633-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64633-126">-InputObject</span></span>
<span data-ttu-id="64633-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="64633-127">The deployment object.</span></span>

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

### <span data-ttu-id="64633-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64633-128">-Name</span></span>
<span data-ttu-id="64633-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="64633-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="64633-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64633-130">-PassThru</span></span>
<span data-ttu-id="64633-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="64633-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="64633-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="64633-132">-Pre</span></span>
<span data-ttu-id="64633-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="64633-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="64633-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64633-134">-Confirm</span></span>
<span data-ttu-id="64633-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64633-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64633-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64633-136">-WhatIf</span></span>
<span data-ttu-id="64633-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64633-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64633-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64633-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64633-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64633-139">CommonParameters</span></span>
<span data-ttu-id="64633-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64633-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64633-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64633-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64633-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64633-142">INPUTS</span></span>

### <span data-ttu-id="64633-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="64633-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="64633-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64633-144">OUTPUTS</span></span>

### <span data-ttu-id="64633-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64633-145">System.Boolean</span></span>

## <span data-ttu-id="64633-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="64633-146">NOTES</span></span>

## <span data-ttu-id="64633-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64633-147">RELATED LINKS</span></span>
