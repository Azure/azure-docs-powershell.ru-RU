---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415540"
---
# <span data-ttu-id="052cd-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="052cd-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="052cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052cd-102">SYNOPSIS</span></span>
<span data-ttu-id="052cd-103">Создание свойств региональной веб-службы.</span><span class="sxs-lookup"><span data-stu-id="052cd-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="052cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="052cd-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052cd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="052cd-105">DESCRIPTION</span></span>
<span data-ttu-id="052cd-106">Создание региональных свойств службы машинного обучения Azure для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="052cd-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="052cd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="052cd-107">EXAMPLES</span></span>

### <span data-ttu-id="052cd-108">Пример 1. Добавление новых региональных свойств для западного центра США</span><span class="sxs-lookup"><span data-stu-id="052cd-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="052cd-109">В этом примере для веб-службы в регионе "Западная центральная часть США" создается региональное свойство.</span><span class="sxs-lookup"><span data-stu-id="052cd-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="052cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="052cd-110">PARAMETERS</span></span>

### <span data-ttu-id="052cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052cd-111">-DefaultProfile</span></span>
<span data-ttu-id="052cd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="052cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="052cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="052cd-113">-Force</span></span>
<span data-ttu-id="052cd-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="052cd-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="052cd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="052cd-115">-Name</span></span>
<span data-ttu-id="052cd-116">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="052cd-116">The name for the web service.</span></span>

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

### <span data-ttu-id="052cd-117">-Регион</span><span class="sxs-lookup"><span data-stu-id="052cd-117">-Region</span></span>
<span data-ttu-id="052cd-118">Регион, в котором создаются свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="052cd-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="052cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="052cd-120">Группа ресурсов, к которой относится веб-служба.</span><span class="sxs-lookup"><span data-stu-id="052cd-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="052cd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="052cd-121">-Confirm</span></span>
<span data-ttu-id="052cd-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="052cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052cd-123">-WhatIf</span></span>
<span data-ttu-id="052cd-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052cd-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="052cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052cd-126">CommonParameters</span></span>
<span data-ttu-id="052cd-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052cd-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052cd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052cd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="052cd-129">INPUTS</span></span>

### <span data-ttu-id="052cd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="052cd-130">System.String</span></span>

## <span data-ttu-id="052cd-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="052cd-131">OUTPUTS</span></span>

### <span data-ttu-id="052cd-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="052cd-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="052cd-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="052cd-133">NOTES</span></span>
<span data-ttu-id="052cd-134">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="052cd-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="052cd-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="052cd-135">RELATED LINKS</span></span>
