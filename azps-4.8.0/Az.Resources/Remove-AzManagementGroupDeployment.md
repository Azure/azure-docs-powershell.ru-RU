---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077650"
---
# <span data-ttu-id="ffa04-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffa04-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ffa04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffa04-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa04-103">Удаляет развертывание в группе управления и любых связанных с ней операций.</span><span class="sxs-lookup"><span data-stu-id="ffa04-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="ffa04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffa04-104">SYNTAX</span></span>

### <span data-ttu-id="ffa04-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffa04-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffa04-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ffa04-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa04-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ffa04-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa04-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa04-108">DESCRIPTION</span></span>
<span data-ttu-id="ffa04-109">Командлет **Remove-AzManagementGroupDeployment** удаляет развертывание Azure из группы управления и каких-либо связанных операций.</span><span class="sxs-lookup"><span data-stu-id="ffa04-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="ffa04-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffa04-110">EXAMPLES</span></span>

### <span data-ttu-id="ffa04-111">Пример 1: Удаление развертывания с указанным именем</span><span class="sxs-lookup"><span data-stu-id="ffa04-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="ffa04-112">Эта команда удаляет развертывание "RolesDeployment" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="ffa04-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="ffa04-113">Пример 2: получение развертывания и его удаление</span><span class="sxs-lookup"><span data-stu-id="ffa04-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="ffa04-114">Эта команда получает развертывание "RolesDeployment" в группе управления "myMG" и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="ffa04-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="ffa04-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffa04-115">PARAMETERS</span></span>

### <span data-ttu-id="ffa04-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ffa04-116">-ApiVersion</span></span>
<span data-ttu-id="ffa04-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffa04-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ffa04-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="ffa04-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa04-119">-AsJob</span></span>
<span data-ttu-id="ffa04-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ffa04-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa04-121">-DefaultProfile</span></span>
<span data-ttu-id="ffa04-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa04-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-123">-ID</span><span class="sxs-lookup"><span data-stu-id="ffa04-123">-Id</span></span>
<span data-ttu-id="ffa04-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="ffa04-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ffa04-125">Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ffa04-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa04-126">-InputObject</span></span>
<span data-ttu-id="ffa04-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="ffa04-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ffa04-128">-ManagementGroupId</span></span>
<span data-ttu-id="ffa04-129">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="ffa04-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffa04-130">-Name</span></span>
<span data-ttu-id="ffa04-131">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="ffa04-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffa04-132">-PassThru</span></span>
<span data-ttu-id="ffa04-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ffa04-133">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="ffa04-134">-Pre</span></span>
<span data-ttu-id="ffa04-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="ffa04-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffa04-136">-Confirm</span></span>
<span data-ttu-id="ffa04-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffa04-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa04-138">-WhatIf</span></span>
<span data-ttu-id="ffa04-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffa04-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa04-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffa04-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa04-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa04-141">CommonParameters</span></span>
<span data-ttu-id="ffa04-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffa04-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa04-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa04-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa04-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffa04-144">INPUTS</span></span>

### <span data-ttu-id="ffa04-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ffa04-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ffa04-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa04-146">OUTPUTS</span></span>

### <span data-ttu-id="ffa04-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffa04-147">System.Boolean</span></span>

## <span data-ttu-id="ffa04-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffa04-148">NOTES</span></span>

## <span data-ttu-id="ffa04-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffa04-149">RELATED LINKS</span></span>