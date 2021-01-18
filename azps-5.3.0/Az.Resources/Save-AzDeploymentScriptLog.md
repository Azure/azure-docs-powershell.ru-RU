---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505158"
---
# <span data-ttu-id="11566-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="11566-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="11566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11566-102">SYNOPSIS</span></span>
<span data-ttu-id="11566-103">Сохраняет журнал выполнения сценария развертывания на диск.</span><span class="sxs-lookup"><span data-stu-id="11566-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="11566-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11566-104">SYNTAX</span></span>

### <span data-ttu-id="11566-105">SaveDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11566-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11566-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="11566-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11566-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="11566-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11566-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11566-108">DESCRIPTION</span></span>
<span data-ttu-id="11566-109">Журнал **Save-AzDeploymentScriptLog** сохраняет журнал выполнения сценария развертывания на диск.</span><span class="sxs-lookup"><span data-stu-id="11566-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="11566-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11566-110">EXAMPLES</span></span>

### <span data-ttu-id="11566-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11566-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="11566-112">Сохраняет журнал сценария развертывания с заданным именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11566-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="11566-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="11566-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="11566-114">Сохранение последних 3 строк журнала сценария развертывания с заданным именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11566-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="11566-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11566-115">PARAMETERS</span></span>

### <span data-ttu-id="11566-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11566-116">-DefaultProfile</span></span>
<span data-ttu-id="11566-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11566-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11566-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="11566-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="11566-119">Объект PowerShell сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="11566-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="11566-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="11566-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="11566-121">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="11566-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="11566-122">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="11566-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="11566-123">-Force</span><span class="sxs-lookup"><span data-stu-id="11566-123">-Force</span></span>
<span data-ttu-id="11566-124">Переописывание существующего файла.</span><span class="sxs-lookup"><span data-stu-id="11566-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="11566-125">-Name</span><span class="sxs-lookup"><span data-stu-id="11566-125">-Name</span></span>
<span data-ttu-id="11566-126">Имя сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="11566-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="11566-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="11566-127">-OutputPath</span></span>
<span data-ttu-id="11566-128">Путь к каталогу для сохранения журнала сценариев развертывания.</span><span class="sxs-lookup"><span data-stu-id="11566-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="11566-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11566-129">-ResourceGroupName</span></span>
<span data-ttu-id="11566-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11566-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="11566-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="11566-131">-Tail</span></span>
<span data-ttu-id="11566-132">Ограничение вывода последними n строками</span><span class="sxs-lookup"><span data-stu-id="11566-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="11566-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11566-133">-Confirm</span></span>
<span data-ttu-id="11566-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11566-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11566-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11566-135">-WhatIf</span></span>
<span data-ttu-id="11566-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11566-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11566-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11566-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11566-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11566-138">CommonParameters</span></span>
<span data-ttu-id="11566-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11566-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11566-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11566-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11566-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11566-141">INPUTS</span></span>

### <span data-ttu-id="11566-142">System.String</span><span class="sxs-lookup"><span data-stu-id="11566-142">System.String</span></span>

## <span data-ttu-id="11566-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11566-143">OUTPUTS</span></span>

### <span data-ttu-id="11566-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="11566-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="11566-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11566-145">NOTES</span></span>

## <span data-ttu-id="11566-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11566-146">RELATED LINKS</span></span>
