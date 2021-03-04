---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952355"
---
# <span data-ttu-id="b6b89-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="b6b89-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="b6b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b89-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b89-103">Создание свойств региональной веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b6b89-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="b6b89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6b89-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b89-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b89-106">Создание региональных свойств службы машинного обучения Azure для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b6b89-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="b6b89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6b89-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b89-108">Пример 1. Добавление новых региональных свойств для западного центра США</span><span class="sxs-lookup"><span data-stu-id="b6b89-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="b6b89-109">В этом примере для веб-службы в регионе "Западная центральная часть США" создается региональное свойство.</span><span class="sxs-lookup"><span data-stu-id="b6b89-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="b6b89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b89-110">PARAMETERS</span></span>

### <span data-ttu-id="b6b89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b89-111">-DefaultProfile</span></span>
<span data-ttu-id="b6b89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6b89-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6b89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b6b89-113">-Force</span></span>
<span data-ttu-id="b6b89-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b6b89-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6b89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b6b89-115">-Name</span></span>
<span data-ttu-id="b6b89-116">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b6b89-116">The name for the web service.</span></span>

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

### <span data-ttu-id="b6b89-117">-Регион</span><span class="sxs-lookup"><span data-stu-id="b6b89-117">-Region</span></span>
<span data-ttu-id="b6b89-118">Регион, в котором нужно создать свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b6b89-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="b6b89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b89-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6b89-120">Группа ресурсов, к которой относится веб-служба.</span><span class="sxs-lookup"><span data-stu-id="b6b89-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="b6b89-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6b89-121">-Confirm</span></span>
<span data-ttu-id="b6b89-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6b89-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b89-123">-WhatIf</span></span>
<span data-ttu-id="b6b89-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6b89-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b89-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6b89-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b89-126">CommonParameters</span></span>
<span data-ttu-id="b6b89-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b89-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b89-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b89-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6b89-129">INPUTS</span></span>

### <span data-ttu-id="b6b89-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b6b89-130">System.String</span></span>

## <span data-ttu-id="b6b89-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6b89-131">OUTPUTS</span></span>

### <span data-ttu-id="b6b89-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="b6b89-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b6b89-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6b89-133">NOTES</span></span>
<span data-ttu-id="b6b89-134">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b6b89-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b6b89-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6b89-135">RELATED LINKS</span></span>
