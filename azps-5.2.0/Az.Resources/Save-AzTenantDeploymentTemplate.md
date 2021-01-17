---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405631"
---
# <span data-ttu-id="9498f-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9498f-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="9498f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9498f-102">SYNOPSIS</span></span>
<span data-ttu-id="9498f-103">Сохранение шаблона развертывания в файл.</span><span class="sxs-lookup"><span data-stu-id="9498f-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="9498f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9498f-104">SYNTAX</span></span>

### <span data-ttu-id="9498f-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9498f-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9498f-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9498f-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9498f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9498f-107">DESCRIPTION</span></span>
<span data-ttu-id="9498f-108">Для развертывания в области клиента шаблон развертывания сохраняется в файле JSON с использованием cmdlet **Save-AzTenantDeploymentTemplate.**</span><span class="sxs-lookup"><span data-stu-id="9498f-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="9498f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9498f-109">EXAMPLES</span></span>

### <span data-ttu-id="9498f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9498f-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="9498f-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его как файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="9498f-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="9498f-112">Пример 2. Получите развертывание и сохраните его шаблон</span><span class="sxs-lookup"><span data-stu-id="9498f-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="9498f-113">Эта команда получает развертывание "RolesDeployment" в текущей области клиента и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="9498f-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="9498f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9498f-114">PARAMETERS</span></span>

### <span data-ttu-id="9498f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9498f-115">-DefaultProfile</span></span>
<span data-ttu-id="9498f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9498f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9498f-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9498f-117">-DeploymentName</span></span>
<span data-ttu-id="9498f-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="9498f-118">The deployment name.</span></span>

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

### <span data-ttu-id="9498f-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9498f-119">-DeploymentObject</span></span>
<span data-ttu-id="9498f-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="9498f-120">The deployment object.</span></span>

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

### <span data-ttu-id="9498f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9498f-121">-Force</span></span>
<span data-ttu-id="9498f-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9498f-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9498f-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9498f-123">-Path</span></span>
<span data-ttu-id="9498f-124">Выходной путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="9498f-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="9498f-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="9498f-125">-Pre</span></span>
<span data-ttu-id="9498f-126">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="9498f-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9498f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9498f-127">-Confirm</span></span>
<span data-ttu-id="9498f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9498f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9498f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9498f-129">-WhatIf</span></span>
<span data-ttu-id="9498f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9498f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9498f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9498f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9498f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9498f-132">CommonParameters</span></span>
<span data-ttu-id="9498f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9498f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9498f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9498f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9498f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9498f-135">INPUTS</span></span>

### <span data-ttu-id="9498f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="9498f-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9498f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9498f-137">OUTPUTS</span></span>

### <span data-ttu-id="9498f-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="9498f-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="9498f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9498f-139">NOTES</span></span>

## <span data-ttu-id="9498f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9498f-140">RELATED LINKS</span></span>
