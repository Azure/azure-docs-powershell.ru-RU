---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244463"
---
# <span data-ttu-id="f1930-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="f1930-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="f1930-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1930-102">SYNOPSIS</span></span>
<span data-ttu-id="f1930-103">Создание свойств региональных веб-служб.</span><span class="sxs-lookup"><span data-stu-id="f1930-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="f1930-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1930-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1930-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1930-105">DESCRIPTION</span></span>
<span data-ttu-id="f1930-106">Создание региональных свойств для службы машинного обучения Azure для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f1930-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="f1930-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1930-107">EXAMPLES</span></span>

### <span data-ttu-id="f1930-108">Пример 1: Добавление новых региональных свойств для "Западная Центральная США"</span><span class="sxs-lookup"><span data-stu-id="f1930-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="f1930-109">Этот пример команды создает региональное свойство для веб-службы в регионе "Западная Центральная часть США".</span><span class="sxs-lookup"><span data-stu-id="f1930-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="f1930-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1930-110">PARAMETERS</span></span>

### <span data-ttu-id="f1930-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1930-111">-DefaultProfile</span></span>
<span data-ttu-id="f1930-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1930-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1930-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f1930-113">-Force</span></span>
<span data-ttu-id="f1930-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f1930-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1930-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1930-115">-Name</span></span>
<span data-ttu-id="f1930-116">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f1930-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1930-117">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="f1930-117">-Region</span></span>
<span data-ttu-id="f1930-118">Область, в которой нужно создать свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f1930-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1930-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1930-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1930-120">Группа ресурсов, к которой принадлежит веб-служба.</span><span class="sxs-lookup"><span data-stu-id="f1930-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1930-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1930-121">-Confirm</span></span>
<span data-ttu-id="f1930-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1930-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1930-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1930-123">-WhatIf</span></span>
<span data-ttu-id="f1930-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1930-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1930-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1930-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1930-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1930-126">CommonParameters</span></span>
<span data-ttu-id="f1930-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1930-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1930-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1930-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1930-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1930-129">INPUTS</span></span>

### <span data-ttu-id="f1930-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1930-130">System.String</span></span>

## <span data-ttu-id="f1930-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1930-131">OUTPUTS</span></span>

### <span data-ttu-id="f1930-132">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="f1930-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f1930-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1930-133">NOTES</span></span>
<span data-ttu-id="f1930-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f1930-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f1930-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1930-135">RELATED LINKS</span></span>
