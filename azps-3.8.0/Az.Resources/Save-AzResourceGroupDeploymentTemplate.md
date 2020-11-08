---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 7d5d5ecc0f8facf03be72f952722ea30b56fa9ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066211"
---
# <span data-ttu-id="d30b5-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d30b5-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="d30b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d30b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d30b5-103">Сохранение шаблона развертывания группы ресурсов в файле.</span><span class="sxs-lookup"><span data-stu-id="d30b5-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="d30b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d30b5-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d30b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d30b5-105">DESCRIPTION</span></span>
<span data-ttu-id="d30b5-106">Командлет **Save-AzResourceGroupDeploymentTemplate**  сохраняет шаблон развертывания группы ресурсов в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="d30b5-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="d30b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d30b5-107">EXAMPLES</span></span>

### <span data-ttu-id="d30b5-108">Пример 1: сохранение шаблона развертывания</span><span class="sxs-lookup"><span data-stu-id="d30b5-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="d30b5-109">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="d30b5-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="d30b5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d30b5-110">PARAMETERS</span></span>

### <span data-ttu-id="d30b5-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d30b5-111">-ApiVersion</span></span>
<span data-ttu-id="d30b5-112">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d30b5-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d30b5-113">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="d30b5-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="d30b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30b5-114">-DefaultProfile</span></span>
<span data-ttu-id="d30b5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d30b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d30b5-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d30b5-116">-DeploymentName</span></span>
<span data-ttu-id="d30b5-117">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="d30b5-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d30b5-118">-Force</span></span>
<span data-ttu-id="d30b5-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d30b5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d30b5-120">-Path</span><span class="sxs-lookup"><span data-stu-id="d30b5-120">-Path</span></span>
<span data-ttu-id="d30b5-121">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="d30b5-121">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b5-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="d30b5-122">-Pre</span></span>
<span data-ttu-id="d30b5-123">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="d30b5-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="d30b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="d30b5-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d30b5-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30b5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d30b5-126">-Confirm</span></span>
<span data-ttu-id="d30b5-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d30b5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30b5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d30b5-128">-WhatIf</span></span>
<span data-ttu-id="d30b5-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d30b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d30b5-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d30b5-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30b5-131">CommonParameters</span></span>
<span data-ttu-id="d30b5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d30b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30b5-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d30b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30b5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d30b5-134">INPUTS</span></span>

### <span data-ttu-id="d30b5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d30b5-135">System.String</span></span>

## <span data-ttu-id="d30b5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d30b5-136">OUTPUTS</span></span>

### <span data-ttu-id="d30b5-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d30b5-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d30b5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d30b5-138">NOTES</span></span>

## <span data-ttu-id="d30b5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d30b5-139">RELATED LINKS</span></span>
