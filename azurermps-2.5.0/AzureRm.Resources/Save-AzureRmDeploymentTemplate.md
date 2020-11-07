---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: d8adaee3e6dacafb4391f350ef567117dc3442c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914677"
---
# <span data-ttu-id="a52c5-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a52c5-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="a52c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a52c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a52c5-103">Сохранение шаблона развертывания в файле.</span><span class="sxs-lookup"><span data-stu-id="a52c5-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a52c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a52c5-104">SYNTAX</span></span>

### <span data-ttu-id="a52c5-105">SaveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a52c5-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a52c5-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a52c5-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a52c5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52c5-107">DESCRIPTION</span></span>
<span data-ttu-id="a52c5-108">Командлет **Save-AzureRmDeploymentTemplate**  сохраняет шаблон развертывания в JSON-файл.</span><span class="sxs-lookup"><span data-stu-id="a52c5-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="a52c5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a52c5-109">EXAMPLES</span></span>

### <span data-ttu-id="a52c5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a52c5-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="a52c5-111">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a52c5-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="a52c5-112">Пример 2: получение развертывания и сохранение шаблона</span><span class="sxs-lookup"><span data-stu-id="a52c5-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="a52c5-113">Эта команда получает развертывание "RolesDeployment" в текущей области подписки и сохраняет его шаблон.</span><span class="sxs-lookup"><span data-stu-id="a52c5-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="a52c5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a52c5-114">PARAMETERS</span></span>

### <span data-ttu-id="a52c5-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a52c5-115">-ApiVersion</span></span>
<span data-ttu-id="a52c5-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a52c5-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a52c5-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="a52c5-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a52c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52c5-118">-DefaultProfile</span></span>
<span data-ttu-id="a52c5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a52c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52c5-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a52c5-120">-DeploymentName</span></span>
<span data-ttu-id="a52c5-121">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="a52c5-121">The deployment name.</span></span>

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

### <span data-ttu-id="a52c5-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a52c5-122">-DeploymentObject</span></span>
<span data-ttu-id="a52c5-123">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="a52c5-123">The deployment object.</span></span>

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

### <span data-ttu-id="a52c5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a52c5-124">-Force</span></span>
<span data-ttu-id="a52c5-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a52c5-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a52c5-126">-Path</span><span class="sxs-lookup"><span data-stu-id="a52c5-126">-Path</span></span>
<span data-ttu-id="a52c5-127">Путь к выходному файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="a52c5-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="a52c5-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="a52c5-128">-Pre</span></span>
<span data-ttu-id="a52c5-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="a52c5-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a52c5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a52c5-130">-Confirm</span></span>
<span data-ttu-id="a52c5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a52c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52c5-132">-WhatIf</span></span>
<span data-ttu-id="a52c5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a52c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52c5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a52c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52c5-135">CommonParameters</span></span>
<span data-ttu-id="a52c5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a52c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52c5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52c5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52c5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a52c5-138">INPUTS</span></span>

### <span data-ttu-id="a52c5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a52c5-139">System.String</span></span>

## <span data-ttu-id="a52c5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52c5-140">OUTPUTS</span></span>

### <span data-ttu-id="a52c5-141">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels</span><span class="sxs-lookup"><span data-stu-id="a52c5-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="a52c5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a52c5-142">NOTES</span></span>

## <span data-ttu-id="a52c5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a52c5-143">RELATED LINKS</span></span>
