---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570364"
---
# <span data-ttu-id="e5908-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="e5908-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="e5908-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5908-102">SYNOPSIS</span></span>
<span data-ttu-id="e5908-103">Создание свойств региональных веб-служб.</span><span class="sxs-lookup"><span data-stu-id="e5908-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5908-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5908-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5908-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5908-105">DESCRIPTION</span></span>
<span data-ttu-id="e5908-106">Создание региональных свойств для службы машинного обучения Azure для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5908-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="e5908-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5908-107">EXAMPLES</span></span>

### <span data-ttu-id="e5908-108">--------------------------Пример 1: Добавление новых региональных свойств для "Западная Центральная часть США"--------------------------</span><span class="sxs-lookup"><span data-stu-id="e5908-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="e5908-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e5908-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="e5908-110">Этот пример команды создает региональное свойство для веб-службы в регионе "Западная Центральная часть США".</span><span class="sxs-lookup"><span data-stu-id="e5908-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="e5908-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5908-111">PARAMETERS</span></span>

### <span data-ttu-id="e5908-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e5908-112">-Force</span></span>
<span data-ttu-id="e5908-113">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e5908-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e5908-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5908-114">-Name</span></span>
<span data-ttu-id="e5908-115">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5908-115">The name for the web service.</span></span>

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

### <span data-ttu-id="e5908-116">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="e5908-116">-Region</span></span>
<span data-ttu-id="e5908-117">Область, в которой нужно создать свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5908-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="e5908-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5908-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5908-119">Группа ресурсов, к которой принадлежит веб-служба.</span><span class="sxs-lookup"><span data-stu-id="e5908-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="e5908-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5908-120">-Confirm</span></span>
<span data-ttu-id="e5908-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5908-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5908-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5908-122">-WhatIf</span></span>
<span data-ttu-id="e5908-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5908-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5908-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5908-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5908-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5908-125">-DefaultProfile</span></span>
<span data-ttu-id="e5908-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5908-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5908-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5908-127">CommonParameters</span></span>
<span data-ttu-id="e5908-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5908-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5908-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5908-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5908-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5908-130">INPUTS</span></span>

## <span data-ttu-id="e5908-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5908-131">OUTPUTS</span></span>

### <span data-ttu-id="e5908-132">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="e5908-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="e5908-133">Сводное описание веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="e5908-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="e5908-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5908-134">NOTES</span></span>
<span data-ttu-id="e5908-135">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e5908-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e5908-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5908-136">RELATED LINKS</span></span>

