---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566706"
---
# <span data-ttu-id="d959b-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="d959b-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="d959b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d959b-102">SYNOPSIS</span></span>
<span data-ttu-id="d959b-103">Удаление веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d959b-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d959b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d959b-104">SYNTAX</span></span>

### <span data-ttu-id="d959b-105">Удалите ресурс веб-службы Azure ML по имени и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d959b-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d959b-106">Удаление веб-службы Azure ML, указанной как объект.</span><span class="sxs-lookup"><span data-stu-id="d959b-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d959b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d959b-107">DESCRIPTION</span></span>
<span data-ttu-id="d959b-108">Удаление веб-службы машинного обучения Azure, на которую ссылается группа ресурсов и имя.</span><span class="sxs-lookup"><span data-stu-id="d959b-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="d959b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d959b-109">EXAMPLES</span></span>

### <span data-ttu-id="d959b-110">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d959b-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="d959b-111">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d959b-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="d959b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d959b-112">PARAMETERS</span></span>

### <span data-ttu-id="d959b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d959b-113">-Force</span></span>
<span data-ttu-id="d959b-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d959b-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d959b-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="d959b-115">-MlWebService</span></span>
<span data-ttu-id="d959b-116">Веб-служба, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d959b-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d959b-117">-Name</span></span>
<span data-ttu-id="d959b-118">Имя веб-службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d959b-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d959b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d959b-120">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d959b-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d959b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d959b-121">-Confirm</span></span>
<span data-ttu-id="d959b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d959b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d959b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d959b-123">-WhatIf</span></span>
<span data-ttu-id="d959b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d959b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d959b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d959b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d959b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d959b-126">-DefaultProfile</span></span>
<span data-ttu-id="d959b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d959b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d959b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d959b-128">CommonParameters</span></span>
<span data-ttu-id="d959b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d959b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d959b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d959b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d959b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d959b-131">INPUTS</span></span>

### <span data-ttu-id="d959b-132">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="d959b-132">WebService</span></span>
<span data-ttu-id="d959b-133">Параметр "MlWebService" принимает значение типа WebService из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d959b-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="d959b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d959b-134">OUTPUTS</span></span>

### <span data-ttu-id="d959b-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="d959b-135">None</span></span>

## <span data-ttu-id="d959b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d959b-136">NOTES</span></span>
<span data-ttu-id="d959b-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d959b-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d959b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d959b-138">RELATED LINKS</span></span>

