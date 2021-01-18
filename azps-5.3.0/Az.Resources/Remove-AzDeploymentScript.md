---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505172"
---
# <span data-ttu-id="34a4c-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="34a4c-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="34a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="34a4c-103">Удаляет сценарий развертывания и связанные с ним ресурсы.</span><span class="sxs-lookup"><span data-stu-id="34a4c-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="34a4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34a4c-104">SYNTAX</span></span>

### <span data-ttu-id="34a4c-105">RemoveDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34a4c-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a4c-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="34a4c-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a4c-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="34a4c-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a4c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34a4c-108">DESCRIPTION</span></span>
<span data-ttu-id="34a4c-109">Для удаления сценария развертывания и связанных с ним ресурсов удаляется **cmdlet Remove-AzDeploymentScript.**</span><span class="sxs-lookup"><span data-stu-id="34a4c-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="34a4c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34a4c-110">EXAMPLES</span></span>

### <span data-ttu-id="34a4c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34a4c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="34a4c-112">Удаляет сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="34a4c-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="34a4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a4c-113">PARAMETERS</span></span>

### <span data-ttu-id="34a4c-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34a4c-114">-Confirm</span></span>
<span data-ttu-id="34a4c-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34a4c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a4c-116">-DefaultProfile</span></span>
<span data-ttu-id="34a4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34a4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a4c-118">-Id</span><span class="sxs-lookup"><span data-stu-id="34a4c-118">-Id</span></span>
<span data-ttu-id="34a4c-119">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="34a4c-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="34a4c-120">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="34a4c-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a4c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34a4c-121">-InputObject</span></span>
<span data-ttu-id="34a4c-122">Объект PowerShell сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="34a4c-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34a4c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="34a4c-123">-Name</span></span>
<span data-ttu-id="34a4c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34a4c-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a4c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34a4c-125">-PassThru</span></span>
<span data-ttu-id="34a4c-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="34a4c-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34a4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="34a4c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34a4c-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a4c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a4c-129">-WhatIf</span></span>
<span data-ttu-id="34a4c-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34a4c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a4c-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34a4c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a4c-132">CommonParameters</span></span>
<span data-ttu-id="34a4c-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="34a4c-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a4c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a4c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34a4c-135">INPUTS</span></span>

### <span data-ttu-id="34a4c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="34a4c-136">System.String</span></span>

### <span data-ttu-id="34a4c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="34a4c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="34a4c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34a4c-138">OUTPUTS</span></span>

### <span data-ttu-id="34a4c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="34a4c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="34a4c-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34a4c-140">NOTES</span></span>

## <span data-ttu-id="34a4c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34a4c-141">RELATED LINKS</span></span>