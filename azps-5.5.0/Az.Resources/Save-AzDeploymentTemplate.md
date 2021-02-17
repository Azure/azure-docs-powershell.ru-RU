---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223268"
---
# <span data-ttu-id="bb1af-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bb1af-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="bb1af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1af-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1af-103">Сохранение шаблона развертывания в файл.</span><span class="sxs-lookup"><span data-stu-id="bb1af-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="bb1af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb1af-104">SYNTAX</span></span>

### <span data-ttu-id="bb1af-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb1af-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb1af-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bb1af-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb1af-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb1af-107">DESCRIPTION</span></span>
<span data-ttu-id="bb1af-108">При **этом шаблон**  развертывания сохраняется в файле JSON.</span><span class="sxs-lookup"><span data-stu-id="bb1af-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="bb1af-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb1af-109">EXAMPLES</span></span>

### <span data-ttu-id="bb1af-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb1af-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="bb1af-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его как файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="bb1af-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="bb1af-112">Пример 2. Получите развертывание и сохраните его шаблон</span><span class="sxs-lookup"><span data-stu-id="bb1af-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="bb1af-113">Эта команда получает развертывание "RolesDeployment" в текущей области действия подписки и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="bb1af-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="bb1af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb1af-114">PARAMETERS</span></span>

### <span data-ttu-id="bb1af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1af-115">-DefaultProfile</span></span>
<span data-ttu-id="bb1af-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1af-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bb1af-117">-DeploymentName</span></span>
<span data-ttu-id="bb1af-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="bb1af-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1af-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bb1af-119">-DeploymentObject</span></span>
<span data-ttu-id="bb1af-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="bb1af-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1af-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bb1af-121">-Force</span></span>
<span data-ttu-id="bb1af-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bb1af-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bb1af-123">-Path</span><span class="sxs-lookup"><span data-stu-id="bb1af-123">-Path</span></span>
<span data-ttu-id="bb1af-124">Выходной путь файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="bb1af-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="bb1af-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="bb1af-125">-Pre</span></span>
<span data-ttu-id="bb1af-126">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="bb1af-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bb1af-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb1af-127">-Confirm</span></span>
<span data-ttu-id="bb1af-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bb1af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb1af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1af-129">-WhatIf</span></span>
<span data-ttu-id="bb1af-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1af-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1af-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bb1af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb1af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1af-132">CommonParameters</span></span>
<span data-ttu-id="bb1af-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1af-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb1af-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1af-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb1af-135">INPUTS</span></span>

### <span data-ttu-id="bb1af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="bb1af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="bb1af-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb1af-137">OUTPUTS</span></span>

### <span data-ttu-id="bb1af-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="bb1af-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="bb1af-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb1af-139">NOTES</span></span>

## <span data-ttu-id="bb1af-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb1af-140">RELATED LINKS</span></span>
