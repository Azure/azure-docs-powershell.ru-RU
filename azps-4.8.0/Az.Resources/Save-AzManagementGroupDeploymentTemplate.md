---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: 536d8f0d7f92e4ca880998293d74d0fc2f1617f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235398"
---
# <span data-ttu-id="f59f2-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f59f2-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="f59f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f59f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f59f2-103">Сохранение шаблона развертывания в файле.</span><span class="sxs-lookup"><span data-stu-id="f59f2-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="f59f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f59f2-104">SYNTAX</span></span>

### <span data-ttu-id="f59f2-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f59f2-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f59f2-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f59f2-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f59f2-107">DESCRIPTION</span></span>
<span data-ttu-id="f59f2-108">Командлет **Save-AzManagementGroupDeploymentTemplate**  сохраняет шаблон развертывания в JSON-файл для развертывания в группе управления.</span><span class="sxs-lookup"><span data-stu-id="f59f2-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="f59f2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f59f2-109">EXAMPLES</span></span>

### <span data-ttu-id="f59f2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f59f2-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="f59f2-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="f59f2-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="f59f2-112">Пример 2: получение развертывания и сохранение шаблона</span><span class="sxs-lookup"><span data-stu-id="f59f2-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="f59f2-113">Эта команда получает развертывание "RolesDeployment" в группе управления "myMG" и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="f59f2-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="f59f2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f59f2-114">PARAMETERS</span></span>

### <span data-ttu-id="f59f2-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f59f2-115">-ApiVersion</span></span>
<span data-ttu-id="f59f2-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f59f2-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f59f2-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="f59f2-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f59f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59f2-118">-DefaultProfile</span></span>
<span data-ttu-id="f59f2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f59f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59f2-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f59f2-120">-DeploymentName</span></span>
<span data-ttu-id="f59f2-121">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="f59f2-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59f2-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f59f2-122">-DeploymentObject</span></span>
<span data-ttu-id="f59f2-123">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="f59f2-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59f2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f59f2-124">-Force</span></span>
<span data-ttu-id="f59f2-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f59f2-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f59f2-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f59f2-126">-ManagementGroupId</span></span>
<span data-ttu-id="f59f2-127">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="f59f2-127">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59f2-128">-Path</span><span class="sxs-lookup"><span data-stu-id="f59f2-128">-Path</span></span>
<span data-ttu-id="f59f2-129">Путь к выходному файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="f59f2-129">The output path of the template file.</span></span>

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

### <span data-ttu-id="f59f2-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="f59f2-130">-Pre</span></span>
<span data-ttu-id="f59f2-131">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="f59f2-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f59f2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f59f2-132">-Confirm</span></span>
<span data-ttu-id="f59f2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f59f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59f2-134">-WhatIf</span></span>
<span data-ttu-id="f59f2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f59f2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59f2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f59f2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59f2-137">CommonParameters</span></span>
<span data-ttu-id="f59f2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f59f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59f2-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59f2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f59f2-140">INPUTS</span></span>

### <span data-ttu-id="f59f2-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f59f2-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f59f2-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f59f2-142">OUTPUTS</span></span>

### <span data-ttu-id="f59f2-143">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="f59f2-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="f59f2-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f59f2-144">NOTES</span></span>

## <span data-ttu-id="f59f2-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f59f2-145">RELATED LINKS</span></span>
