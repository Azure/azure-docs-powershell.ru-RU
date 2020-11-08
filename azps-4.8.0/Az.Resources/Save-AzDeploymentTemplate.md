---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: aa34157f556de3fe0acc5d8197caaa1a14dc364d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235400"
---
# <span data-ttu-id="3cc4c-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3cc4c-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="3cc4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc4c-103">Сохранение шаблона развертывания в файле.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="3cc4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cc4c-104">SYNTAX</span></span>

### <span data-ttu-id="3cc4c-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3cc4c-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc4c-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3cc4c-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc4c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cc4c-107">DESCRIPTION</span></span>
<span data-ttu-id="3cc4c-108">Командлет **Save-AzDeploymentTemplate**  сохраняет шаблон развертывания в JSON-файл.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="3cc4c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cc4c-109">EXAMPLES</span></span>

### <span data-ttu-id="3cc4c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3cc4c-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="3cc4c-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="3cc4c-112">Пример 2: получение развертывания и сохранение шаблона</span><span class="sxs-lookup"><span data-stu-id="3cc4c-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="3cc4c-113">Эта команда получает развертывание "RolesDeployment" в текущей области подписки и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="3cc4c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cc4c-114">PARAMETERS</span></span>

### <span data-ttu-id="3cc4c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3cc4c-115">-ApiVersion</span></span>
<span data-ttu-id="3cc4c-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3cc4c-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3cc4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc4c-118">-DefaultProfile</span></span>
<span data-ttu-id="3cc4c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc4c-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3cc4c-120">-DeploymentName</span></span>
<span data-ttu-id="3cc4c-121">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-121">The deployment name.</span></span>

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

### <span data-ttu-id="3cc4c-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3cc4c-122">-DeploymentObject</span></span>
<span data-ttu-id="3cc4c-123">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-123">The deployment object.</span></span>

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

### <span data-ttu-id="3cc4c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3cc4c-124">-Force</span></span>
<span data-ttu-id="3cc4c-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3cc4c-126">-Path</span><span class="sxs-lookup"><span data-stu-id="3cc4c-126">-Path</span></span>
<span data-ttu-id="3cc4c-127">Путь к выходному файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="3cc4c-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="3cc4c-128">-Pre</span></span>
<span data-ttu-id="3cc4c-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3cc4c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cc4c-130">-Confirm</span></span>
<span data-ttu-id="3cc4c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc4c-132">-WhatIf</span></span>
<span data-ttu-id="3cc4c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc4c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc4c-135">CommonParameters</span></span>
<span data-ttu-id="3cc4c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cc4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc4c-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cc4c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc4c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cc4c-138">INPUTS</span></span>

### <span data-ttu-id="3cc4c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3cc4c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3cc4c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cc4c-140">OUTPUTS</span></span>

### <span data-ttu-id="3cc4c-141">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="3cc4c-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="3cc4c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cc4c-142">NOTES</span></span>

## <span data-ttu-id="3cc4c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cc4c-143">RELATED LINKS</span></span>
