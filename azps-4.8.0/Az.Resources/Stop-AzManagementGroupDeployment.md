---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234775"
---
# <span data-ttu-id="2398d-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2398d-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2398d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2398d-102">SYNOPSIS</span></span>
<span data-ttu-id="2398d-103">Отмена выполняющегося развертывания в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="2398d-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="2398d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2398d-104">SYNTAX</span></span>

### <span data-ttu-id="2398d-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2398d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2398d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2398d-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2398d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="2398d-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2398d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2398d-108">DESCRIPTION</span></span>
<span data-ttu-id="2398d-109">Командлет **Stop-AzManagementGroupDeployment** отменяет развертывание, которое было начато, но не завершено в группе управления.</span><span class="sxs-lookup"><span data-stu-id="2398d-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="2398d-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="2398d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="2398d-111">Чтобы создать развертывание в группе управления, используйте командлет New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2398d-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="2398d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2398d-112">EXAMPLES</span></span>

### <span data-ttu-id="2398d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2398d-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="2398d-114">Эта команда отменяет запущенное развертывание "deployment01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="2398d-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="2398d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2398d-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="2398d-116">Эта команда получает развертывание "deployment01" в группе управления "myMG" и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="2398d-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="2398d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2398d-117">PARAMETERS</span></span>

### <span data-ttu-id="2398d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2398d-118">-ApiVersion</span></span>
<span data-ttu-id="2398d-119">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2398d-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2398d-120">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="2398d-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2398d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2398d-121">-DefaultProfile</span></span>
<span data-ttu-id="2398d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2398d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2398d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="2398d-123">-Id</span></span>
<span data-ttu-id="2398d-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="2398d-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2398d-125">Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2398d-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2398d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2398d-126">-InputObject</span></span>
<span data-ttu-id="2398d-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="2398d-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2398d-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2398d-128">-ManagementGroupId</span></span>
<span data-ttu-id="2398d-129">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="2398d-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2398d-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2398d-130">-Name</span></span>
<span data-ttu-id="2398d-131">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="2398d-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2398d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2398d-132">-PassThru</span></span>
<span data-ttu-id="2398d-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="2398d-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2398d-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="2398d-134">-Pre</span></span>
<span data-ttu-id="2398d-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="2398d-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2398d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2398d-136">-Confirm</span></span>
<span data-ttu-id="2398d-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2398d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2398d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2398d-138">-WhatIf</span></span>
<span data-ttu-id="2398d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2398d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2398d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2398d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2398d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2398d-141">CommonParameters</span></span>
<span data-ttu-id="2398d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2398d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2398d-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2398d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2398d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2398d-144">INPUTS</span></span>

### <span data-ttu-id="2398d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2398d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2398d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2398d-146">OUTPUTS</span></span>

### <span data-ttu-id="2398d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2398d-147">System.Boolean</span></span>

## <span data-ttu-id="2398d-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2398d-148">NOTES</span></span>

## <span data-ttu-id="2398d-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2398d-149">RELATED LINKS</span></span>
