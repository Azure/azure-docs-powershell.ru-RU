---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423663"
---
# <span data-ttu-id="1d88c-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d88c-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="1d88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d88c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d88c-103">Сохранение шаблона развертывания в файл.</span><span class="sxs-lookup"><span data-stu-id="1d88c-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="1d88c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d88c-104">SYNTAX</span></span>

### <span data-ttu-id="1d88c-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d88c-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d88c-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1d88c-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d88c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d88c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d88c-108">При этом шаблон развертывания сохраняется в **JSON-файле**  для развертывания в группе управления.</span><span class="sxs-lookup"><span data-stu-id="1d88c-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="1d88c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d88c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d88c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d88c-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="1d88c-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его как файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="1d88c-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="1d88c-112">Пример 2. Получите развертывание и сохраните его шаблон</span><span class="sxs-lookup"><span data-stu-id="1d88c-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="1d88c-113">Эта команда получает "RolesDeployment" в группе управления MyMG и сохраняет ее шаблон.</span><span class="sxs-lookup"><span data-stu-id="1d88c-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="1d88c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d88c-114">PARAMETERS</span></span>

### <span data-ttu-id="1d88c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d88c-115">-DefaultProfile</span></span>
<span data-ttu-id="1d88c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d88c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d88c-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1d88c-117">-DeploymentName</span></span>
<span data-ttu-id="1d88c-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="1d88c-118">The deployment name.</span></span>

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

### <span data-ttu-id="1d88c-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1d88c-119">-DeploymentObject</span></span>
<span data-ttu-id="1d88c-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="1d88c-120">The deployment object.</span></span>

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

### <span data-ttu-id="1d88c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1d88c-121">-Force</span></span>
<span data-ttu-id="1d88c-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1d88c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1d88c-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1d88c-123">-ManagementGroupId</span></span>
<span data-ttu-id="1d88c-124">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="1d88c-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d88c-125">-Path</span><span class="sxs-lookup"><span data-stu-id="1d88c-125">-Path</span></span>
<span data-ttu-id="1d88c-126">Выходной путь файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="1d88c-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="1d88c-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d88c-127">-Pre</span></span>
<span data-ttu-id="1d88c-128">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="1d88c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1d88c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d88c-129">-Confirm</span></span>
<span data-ttu-id="1d88c-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d88c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d88c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d88c-131">-WhatIf</span></span>
<span data-ttu-id="1d88c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d88c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d88c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d88c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d88c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d88c-134">CommonParameters</span></span>
<span data-ttu-id="1d88c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d88c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d88c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d88c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d88c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d88c-137">INPUTS</span></span>

### <span data-ttu-id="1d88c-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="1d88c-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1d88c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d88c-139">OUTPUTS</span></span>

### <span data-ttu-id="1d88c-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="1d88c-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="1d88c-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d88c-141">NOTES</span></span>

## <span data-ttu-id="1d88c-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d88c-142">RELATED LINKS</span></span>
