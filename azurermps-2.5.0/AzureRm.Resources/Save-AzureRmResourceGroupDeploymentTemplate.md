---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: 78ad8ee76aeeec4f57e0d2f2a6b2a1f4d9424d97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913552"
---
# <span data-ttu-id="c8fd9-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c8fd9-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c8fd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fd9-103">Сохранение шаблона развертывания группы ресурсов в файле.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8fd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8fd9-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8fd9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="c8fd9-106">Командлет **Save-AzureRmResourceGroupDeploymentTemplate**  сохраняет шаблон развертывания группы ресурсов в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="c8fd9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8fd9-107">EXAMPLES</span></span>

### <span data-ttu-id="c8fd9-108">Пример 1: сохранение шаблона развертывания</span><span class="sxs-lookup"><span data-stu-id="c8fd9-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c8fd9-109">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="c8fd9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="c8fd9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8fd9-111">-ApiVersion</span></span>
<span data-ttu-id="c8fd9-112">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8fd9-113">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="c8fd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8fd9-114">-DefaultProfile</span></span>
<span data-ttu-id="c8fd9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8fd9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fd9-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c8fd9-116">-DeploymentName</span></span>
<span data-ttu-id="c8fd9-117">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="c8fd9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c8fd9-118">-Force</span></span>
<span data-ttu-id="c8fd9-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8fd9-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8fd9-120">-InformationAction</span></span>
<span data-ttu-id="c8fd9-121">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="c8fd9-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c8fd9-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8fd9-123">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c8fd9-123">Continue</span></span>
- <span data-ttu-id="c8fd9-124">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c8fd9-124">Ignore</span></span>
- <span data-ttu-id="c8fd9-125">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c8fd9-125">Inquire</span></span>
- <span data-ttu-id="c8fd9-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8fd9-126">SilentlyContinue</span></span>
- <span data-ttu-id="c8fd9-127">Остановить</span><span class="sxs-lookup"><span data-stu-id="c8fd9-127">Stop</span></span>
- <span data-ttu-id="c8fd9-128">Рвать</span><span class="sxs-lookup"><span data-stu-id="c8fd9-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fd9-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8fd9-129">-InformationVariable</span></span>
<span data-ttu-id="c8fd9-130">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fd9-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c8fd9-131">-Path</span></span>
<span data-ttu-id="c8fd9-132">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c8fd9-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8fd9-133">-Pre</span></span>
<span data-ttu-id="c8fd9-134">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="c8fd9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8fd9-135">-ResourceGroupName</span></span>
<span data-ttu-id="c8fd9-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8fd9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8fd9-137">-Confirm</span></span>
<span data-ttu-id="c8fd9-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8fd9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8fd9-139">-WhatIf</span></span>
<span data-ttu-id="c8fd9-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8fd9-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8fd9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fd9-142">CommonParameters</span></span>
<span data-ttu-id="c8fd9-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8fd9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fd9-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8fd9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fd9-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8fd9-145">INPUTS</span></span>

## <span data-ttu-id="c8fd9-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8fd9-146">OUTPUTS</span></span>

## <span data-ttu-id="c8fd9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8fd9-147">NOTES</span></span>

## <span data-ttu-id="c8fd9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8fd9-148">RELATED LINKS</span></span>
