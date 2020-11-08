---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: 79a60294126a990d191e4838a91c0f6554bea43b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066210"
---
# <span data-ttu-id="65683-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="65683-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="65683-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65683-102">SYNOPSIS</span></span>
<span data-ttu-id="65683-103">Сохранение шаблона развертывания в файле.</span><span class="sxs-lookup"><span data-stu-id="65683-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="65683-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65683-104">SYNTAX</span></span>

### <span data-ttu-id="65683-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65683-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65683-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="65683-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65683-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65683-107">DESCRIPTION</span></span>
<span data-ttu-id="65683-108">Командлет **Save-AzTenantDeploymentTemplate**  сохраняет шаблон развертывания в JSON-файл для развертывания в области клиента.</span><span class="sxs-lookup"><span data-stu-id="65683-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="65683-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65683-109">EXAMPLES</span></span>

### <span data-ttu-id="65683-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65683-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="65683-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="65683-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="65683-112">Пример 2: получение развертывания и сохранение шаблона</span><span class="sxs-lookup"><span data-stu-id="65683-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="65683-113">Эта команда получает развертывание "RolesDeployment" в текущей области клиента и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="65683-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="65683-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65683-114">PARAMETERS</span></span>

### <span data-ttu-id="65683-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65683-115">-ApiVersion</span></span>
<span data-ttu-id="65683-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65683-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="65683-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="65683-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="65683-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65683-118">-DefaultProfile</span></span>
<span data-ttu-id="65683-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65683-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65683-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="65683-120">-DeploymentName</span></span>
<span data-ttu-id="65683-121">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="65683-121">The deployment name.</span></span>

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

### <span data-ttu-id="65683-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="65683-122">-DeploymentObject</span></span>
<span data-ttu-id="65683-123">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="65683-123">The deployment object.</span></span>

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

### <span data-ttu-id="65683-124">-Force</span><span class="sxs-lookup"><span data-stu-id="65683-124">-Force</span></span>
<span data-ttu-id="65683-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="65683-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65683-126">-Path</span><span class="sxs-lookup"><span data-stu-id="65683-126">-Path</span></span>
<span data-ttu-id="65683-127">Путь к выходному файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="65683-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="65683-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="65683-128">-Pre</span></span>
<span data-ttu-id="65683-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="65683-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="65683-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65683-130">-Confirm</span></span>
<span data-ttu-id="65683-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65683-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65683-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65683-132">-WhatIf</span></span>
<span data-ttu-id="65683-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65683-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65683-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65683-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65683-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65683-135">CommonParameters</span></span>
<span data-ttu-id="65683-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65683-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65683-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65683-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65683-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65683-138">INPUTS</span></span>

### <span data-ttu-id="65683-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="65683-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="65683-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65683-140">OUTPUTS</span></span>

### <span data-ttu-id="65683-141">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="65683-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="65683-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="65683-142">NOTES</span></span>

## <span data-ttu-id="65683-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65683-143">RELATED LINKS</span></span>
