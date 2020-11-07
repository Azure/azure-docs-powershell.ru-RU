---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 2be6deeca64a8d167231cf7afe3b84b60f6e6c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734004"
---
# <span data-ttu-id="a7713-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a7713-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="a7713-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7713-102">SYNOPSIS</span></span>
<span data-ttu-id="a7713-103">Сохранение шаблона развертывания группы ресурсов в файле.</span><span class="sxs-lookup"><span data-stu-id="a7713-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7713-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7713-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7713-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7713-105">DESCRIPTION</span></span>
<span data-ttu-id="a7713-106">Командлет **Save-AzureRmResourceGroupDeploymentTemplate**  сохраняет шаблон развертывания группы ресурсов в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="a7713-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="a7713-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7713-107">EXAMPLES</span></span>

### <span data-ttu-id="a7713-108">Пример 1: сохранение шаблона развертывания</span><span class="sxs-lookup"><span data-stu-id="a7713-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="a7713-109">Эта команда получает шаблон развертывания из TestDeployment и сохраняет его в виде JSON-файла в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a7713-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="a7713-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7713-110">PARAMETERS</span></span>

### <span data-ttu-id="a7713-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a7713-111">-ApiVersion</span></span>
<span data-ttu-id="a7713-112">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7713-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a7713-113">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="a7713-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="a7713-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7713-114">-DefaultProfile</span></span>
<span data-ttu-id="a7713-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7713-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7713-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a7713-116">-DeploymentName</span></span>
<span data-ttu-id="a7713-117">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="a7713-117">Specifies the name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a7713-118">-Force</span></span>
<span data-ttu-id="a7713-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7713-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7713-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a7713-120">-InformationAction</span></span>
<span data-ttu-id="a7713-121">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a7713-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a7713-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a7713-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7713-123">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a7713-123">Continue</span></span>
- <span data-ttu-id="a7713-124">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a7713-124">Ignore</span></span>
- <span data-ttu-id="a7713-125">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a7713-125">Inquire</span></span>
- <span data-ttu-id="a7713-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a7713-126">SilentlyContinue</span></span>
- <span data-ttu-id="a7713-127">Остановить</span><span class="sxs-lookup"><span data-stu-id="a7713-127">Stop</span></span>
- <span data-ttu-id="a7713-128">Рвать</span><span class="sxs-lookup"><span data-stu-id="a7713-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a7713-129">-InformationVariable</span></span>
<span data-ttu-id="a7713-130">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a7713-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-131">-Path</span><span class="sxs-lookup"><span data-stu-id="a7713-131">-Path</span></span>
<span data-ttu-id="a7713-132">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="a7713-132">Specifies the output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="a7713-133">-Pre</span></span>
<span data-ttu-id="a7713-134">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="a7713-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="a7713-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7713-135">-ResourceGroupName</span></span>
<span data-ttu-id="a7713-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7713-136">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7713-137">-Confirm</span></span>
<span data-ttu-id="a7713-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7713-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7713-139">-WhatIf</span></span>
<span data-ttu-id="a7713-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a7713-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7713-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a7713-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7713-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7713-142">CommonParameters</span></span>
<span data-ttu-id="a7713-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7713-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7713-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7713-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7713-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7713-145">INPUTS</span></span>

### <span data-ttu-id="a7713-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7713-146">None</span></span>
<span data-ttu-id="a7713-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a7713-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7713-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7713-148">OUTPUTS</span></span>

### <span data-ttu-id="a7713-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a7713-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a7713-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7713-150">NOTES</span></span>

## <span data-ttu-id="a7713-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7713-151">RELATED LINKS</span></span>
