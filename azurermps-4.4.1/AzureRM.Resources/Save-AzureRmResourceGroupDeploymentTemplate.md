---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734780"
---
# <span data-ttu-id="8dedf-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8dedf-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="8dedf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="8dedf-103">Сохранение шаблона развертывания группы ресурсов в файле.</span><span class="sxs-lookup"><span data-stu-id="8dedf-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dedf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dedf-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dedf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dedf-105">DESCRIPTION</span></span>
<span data-ttu-id="8dedf-106">Командлет **Save-AzureRmResourceGroupDeploymentTemplate**  сохраняет шаблон развертывания группы ресурсов в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="8dedf-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="8dedf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dedf-107">EXAMPLES</span></span>

### <span data-ttu-id="8dedf-108">Пример 1: сохранение шаблона развертывания</span><span class="sxs-lookup"><span data-stu-id="8dedf-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="8dedf-109">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="8dedf-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="8dedf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dedf-110">PARAMETERS</span></span>

### <span data-ttu-id="8dedf-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8dedf-111">-ApiVersion</span></span>
<span data-ttu-id="8dedf-112">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dedf-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8dedf-113">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="8dedf-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="8dedf-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8dedf-114">-DeploymentName</span></span>
<span data-ttu-id="8dedf-115">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="8dedf-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="8dedf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8dedf-116">-Force</span></span>
<span data-ttu-id="8dedf-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dedf-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8dedf-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8dedf-118">-InformationAction</span></span>
<span data-ttu-id="8dedf-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8dedf-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8dedf-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8dedf-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8dedf-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8dedf-121">Continue</span></span>
- <span data-ttu-id="8dedf-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8dedf-122">Ignore</span></span>
- <span data-ttu-id="8dedf-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8dedf-123">Inquire</span></span>
- <span data-ttu-id="8dedf-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8dedf-124">SilentlyContinue</span></span>
- <span data-ttu-id="8dedf-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="8dedf-125">Stop</span></span>
- <span data-ttu-id="8dedf-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="8dedf-126">Suspend</span></span>

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

### <span data-ttu-id="8dedf-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8dedf-127">-InformationVariable</span></span>
<span data-ttu-id="8dedf-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8dedf-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8dedf-129">-Path</span><span class="sxs-lookup"><span data-stu-id="8dedf-129">-Path</span></span>
<span data-ttu-id="8dedf-130">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="8dedf-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="8dedf-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="8dedf-131">-Pre</span></span>
<span data-ttu-id="8dedf-132">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="8dedf-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="8dedf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dedf-133">-ResourceGroupName</span></span>
<span data-ttu-id="8dedf-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dedf-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8dedf-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dedf-135">-Confirm</span></span>
<span data-ttu-id="8dedf-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dedf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dedf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dedf-137">-WhatIf</span></span>
<span data-ttu-id="8dedf-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dedf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dedf-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dedf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dedf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dedf-140">-DefaultProfile</span></span>
<span data-ttu-id="8dedf-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dedf-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dedf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dedf-142">CommonParameters</span></span>
<span data-ttu-id="8dedf-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dedf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dedf-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dedf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dedf-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dedf-145">INPUTS</span></span>

## <span data-ttu-id="8dedf-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dedf-146">OUTPUTS</span></span>

### <span data-ttu-id="8dedf-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8dedf-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8dedf-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dedf-148">NOTES</span></span>

## <span data-ttu-id="8dedf-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dedf-149">RELATED LINKS</span></span>

