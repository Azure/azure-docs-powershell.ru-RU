---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995207"
---
# <span data-ttu-id="f4a57-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f4a57-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f4a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a57-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a57-103">Сохраняет журнал выполнения сценария развертывания на диск.</span><span class="sxs-lookup"><span data-stu-id="f4a57-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="f4a57-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4a57-104">SYNTAX</span></span>

### <span data-ttu-id="f4a57-105">SaveDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4a57-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4a57-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a57-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a57-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f4a57-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a57-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4a57-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a57-109">Журнал **Save-AzDeploymentScriptLog** сохраняет журнал выполнения сценария развертывания на диск.</span><span class="sxs-lookup"><span data-stu-id="f4a57-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="f4a57-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4a57-110">EXAMPLES</span></span>

### <span data-ttu-id="f4a57-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4a57-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="f4a57-112">Сохраняет журнал сценария развертывания с заданным именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4a57-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="f4a57-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f4a57-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="f4a57-114">Сохранение последних 3 строк журнала сценария развертывания с заданным именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4a57-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="f4a57-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4a57-115">PARAMETERS</span></span>

### <span data-ttu-id="f4a57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a57-116">-DefaultProfile</span></span>
<span data-ttu-id="f4a57-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a57-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a57-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f4a57-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="f4a57-119">Объект PowerShell сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="f4a57-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a57-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f4a57-121">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="f4a57-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f4a57-122">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f4a57-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f4a57-123">-Force</span></span>
<span data-ttu-id="f4a57-124">Переописывание существующего файла.</span><span class="sxs-lookup"><span data-stu-id="f4a57-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="f4a57-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f4a57-125">-Name</span></span>
<span data-ttu-id="f4a57-126">Имя сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="f4a57-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f4a57-127">-OutputPath</span></span>
<span data-ttu-id="f4a57-128">Путь к каталогу для сохранения журнала сценариев развертывания.</span><span class="sxs-lookup"><span data-stu-id="f4a57-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a57-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4a57-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4a57-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="f4a57-131">-Tail</span></span>
<span data-ttu-id="f4a57-132">Ограничение вывода последними n строками</span><span class="sxs-lookup"><span data-stu-id="f4a57-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a57-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4a57-133">-Confirm</span></span>
<span data-ttu-id="f4a57-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f4a57-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a57-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a57-135">-WhatIf</span></span>
<span data-ttu-id="f4a57-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4a57-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a57-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4a57-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a57-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a57-138">CommonParameters</span></span>
<span data-ttu-id="f4a57-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a57-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a57-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4a57-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a57-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4a57-141">INPUTS</span></span>

### <span data-ttu-id="f4a57-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f4a57-142">System.String</span></span>

## <span data-ttu-id="f4a57-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4a57-143">OUTPUTS</span></span>

### <span data-ttu-id="f4a57-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="f4a57-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="f4a57-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4a57-145">NOTES</span></span>

## <span data-ttu-id="f4a57-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4a57-146">RELATED LINKS</span></span>
