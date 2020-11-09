---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249820"
---
# <span data-ttu-id="9e800-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="9e800-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="9e800-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e800-102">SYNOPSIS</span></span>
<span data-ttu-id="9e800-103">Сохранение журнала выполнения сценария развертывания на диске.</span><span class="sxs-lookup"><span data-stu-id="9e800-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="9e800-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e800-104">SYNTAX</span></span>

### <span data-ttu-id="9e800-105">SaveDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e800-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e800-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e800-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e800-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e800-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e800-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e800-108">DESCRIPTION</span></span>
<span data-ttu-id="9e800-109">**AzDeploymentScriptLog Save (сохранить данные)** сохраняет журнал выполнения сценария развертывания на диск.</span><span class="sxs-lookup"><span data-stu-id="9e800-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="9e800-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e800-110">EXAMPLES</span></span>

### <span data-ttu-id="9e800-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e800-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="9e800-112">Сохранение журнала сценария развертывания с заданными именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e800-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="9e800-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e800-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="9e800-114">Сохраняет последние 3 строки журнала сценария развертывания с заданными именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e800-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="9e800-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e800-115">PARAMETERS</span></span>

### <span data-ttu-id="9e800-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e800-116">-DefaultProfile</span></span>
<span data-ttu-id="9e800-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e800-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e800-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="9e800-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="9e800-119">Объект PowerShell для сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e800-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="9e800-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="9e800-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="9e800-121">Полный идентификатор ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e800-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="9e800-122">Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="9e800-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="9e800-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9e800-123">-Force</span></span>
<span data-ttu-id="9e800-124">Принудительная перезапись существующего файла.</span><span class="sxs-lookup"><span data-stu-id="9e800-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="9e800-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e800-125">-Name</span></span>
<span data-ttu-id="9e800-126">Имя скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e800-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="9e800-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="9e800-127">-OutputPath</span></span>
<span data-ttu-id="9e800-128">Путь к каталогу для сохранения журнала сценариев развертывания.</span><span class="sxs-lookup"><span data-stu-id="9e800-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="9e800-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e800-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e800-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e800-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e800-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="9e800-131">-Tail</span></span>
<span data-ttu-id="9e800-132">Ограничить вывод на последние n строк</span><span class="sxs-lookup"><span data-stu-id="9e800-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="9e800-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e800-133">-Confirm</span></span>
<span data-ttu-id="9e800-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e800-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e800-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e800-135">-WhatIf</span></span>
<span data-ttu-id="9e800-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e800-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e800-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e800-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e800-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e800-138">CommonParameters</span></span>
<span data-ttu-id="9e800-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e800-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e800-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e800-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e800-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e800-141">INPUTS</span></span>

### <span data-ttu-id="9e800-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9e800-142">System.String</span></span>

## <span data-ttu-id="9e800-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e800-143">OUTPUTS</span></span>

### <span data-ttu-id="9e800-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="9e800-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="9e800-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e800-145">NOTES</span></span>

## <span data-ttu-id="9e800-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e800-146">RELATED LINKS</span></span>