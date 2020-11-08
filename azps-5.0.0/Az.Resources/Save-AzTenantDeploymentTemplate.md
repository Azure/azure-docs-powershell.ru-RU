---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249810"
---
# <span data-ttu-id="24dbd-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="24dbd-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="24dbd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="24dbd-103">Сохранение шаблона развертывания в файле.</span><span class="sxs-lookup"><span data-stu-id="24dbd-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="24dbd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24dbd-104">SYNTAX</span></span>

### <span data-ttu-id="24dbd-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24dbd-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24dbd-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="24dbd-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24dbd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24dbd-107">DESCRIPTION</span></span>
<span data-ttu-id="24dbd-108">Командлет **Save-AzTenantDeploymentTemplate**  сохраняет шаблон развертывания в JSON-файл для развертывания в области клиента.</span><span class="sxs-lookup"><span data-stu-id="24dbd-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="24dbd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24dbd-109">EXAMPLES</span></span>

### <span data-ttu-id="24dbd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24dbd-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="24dbd-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="24dbd-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="24dbd-112">Пример 2: получение развертывания и сохранение шаблона</span><span class="sxs-lookup"><span data-stu-id="24dbd-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="24dbd-113">Эта команда получает развертывание "RolesDeployment" в текущей области клиента и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="24dbd-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="24dbd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24dbd-114">PARAMETERS</span></span>

### <span data-ttu-id="24dbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24dbd-115">-DefaultProfile</span></span>
<span data-ttu-id="24dbd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24dbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24dbd-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="24dbd-117">-DeploymentName</span></span>
<span data-ttu-id="24dbd-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="24dbd-118">The deployment name.</span></span>

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

### <span data-ttu-id="24dbd-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="24dbd-119">-DeploymentObject</span></span>
<span data-ttu-id="24dbd-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="24dbd-120">The deployment object.</span></span>

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

### <span data-ttu-id="24dbd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="24dbd-121">-Force</span></span>
<span data-ttu-id="24dbd-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="24dbd-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24dbd-123">-Path</span><span class="sxs-lookup"><span data-stu-id="24dbd-123">-Path</span></span>
<span data-ttu-id="24dbd-124">Путь к выходному файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="24dbd-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="24dbd-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="24dbd-125">-Pre</span></span>
<span data-ttu-id="24dbd-126">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="24dbd-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="24dbd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24dbd-127">-Confirm</span></span>
<span data-ttu-id="24dbd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24dbd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24dbd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24dbd-129">-WhatIf</span></span>
<span data-ttu-id="24dbd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24dbd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24dbd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24dbd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24dbd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24dbd-132">CommonParameters</span></span>
<span data-ttu-id="24dbd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24dbd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24dbd-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24dbd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24dbd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24dbd-135">INPUTS</span></span>

### <span data-ttu-id="24dbd-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="24dbd-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="24dbd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24dbd-137">OUTPUTS</span></span>

### <span data-ttu-id="24dbd-138">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="24dbd-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="24dbd-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="24dbd-139">NOTES</span></span>

## <span data-ttu-id="24dbd-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24dbd-140">RELATED LINKS</span></span>
