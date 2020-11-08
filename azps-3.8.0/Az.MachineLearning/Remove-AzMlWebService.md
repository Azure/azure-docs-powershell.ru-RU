---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074228"
---
# <span data-ttu-id="f402e-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="f402e-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="f402e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f402e-102">SYNOPSIS</span></span>
<span data-ttu-id="f402e-103">Удаление веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f402e-103">Deletes a web service.</span></span>

## <span data-ttu-id="f402e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f402e-104">SYNTAX</span></span>

### <span data-ttu-id="f402e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f402e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f402e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="f402e-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f402e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f402e-107">DESCRIPTION</span></span>
<span data-ttu-id="f402e-108">Удаление веб-службы машинного обучения Azure, на которую ссылается группа ресурсов и имя.</span><span class="sxs-lookup"><span data-stu-id="f402e-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="f402e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f402e-109">EXAMPLES</span></span>

### <span data-ttu-id="f402e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f402e-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="f402e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f402e-111">PARAMETERS</span></span>

### <span data-ttu-id="f402e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f402e-112">-DefaultProfile</span></span>
<span data-ttu-id="f402e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f402e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f402e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f402e-114">-Force</span></span>
<span data-ttu-id="f402e-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f402e-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f402e-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f402e-116">-MlWebService</span></span>
<span data-ttu-id="f402e-117">Веб-служба, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f402e-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f402e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f402e-118">-Name</span></span>
<span data-ttu-id="f402e-119">Имя веб-службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f402e-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f402e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f402e-120">-ResourceGroupName</span></span>
<span data-ttu-id="f402e-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f402e-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f402e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f402e-122">-Confirm</span></span>
<span data-ttu-id="f402e-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f402e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f402e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f402e-124">-WhatIf</span></span>
<span data-ttu-id="f402e-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f402e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f402e-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f402e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f402e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f402e-127">CommonParameters</span></span>
<span data-ttu-id="f402e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f402e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f402e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f402e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f402e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f402e-130">INPUTS</span></span>

### <span data-ttu-id="f402e-131">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="f402e-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f402e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f402e-132">OUTPUTS</span></span>

### <span data-ttu-id="f402e-133">System. void</span><span class="sxs-lookup"><span data-stu-id="f402e-133">System.Void</span></span>

## <span data-ttu-id="f402e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f402e-134">NOTES</span></span>
<span data-ttu-id="f402e-135">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f402e-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f402e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f402e-136">RELATED LINKS</span></span>
