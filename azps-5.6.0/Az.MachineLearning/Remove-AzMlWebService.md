---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006696"
---
# <span data-ttu-id="0a915-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0a915-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="0a915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a915-102">SYNOPSIS</span></span>
<span data-ttu-id="0a915-103">Удаляет веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0a915-103">Deletes a web service.</span></span>

## <span data-ttu-id="0a915-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a915-104">SYNTAX</span></span>

### <span data-ttu-id="0a915-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a915-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a915-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0a915-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a915-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a915-107">DESCRIPTION</span></span>
<span data-ttu-id="0a915-108">Удаляет веб-службу машинного обучения Azure, на которые ссылается группа ресурсов и имя.</span><span class="sxs-lookup"><span data-stu-id="0a915-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="0a915-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a915-109">EXAMPLES</span></span>

### <span data-ttu-id="0a915-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a915-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="0a915-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a915-111">PARAMETERS</span></span>

### <span data-ttu-id="0a915-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a915-112">-DefaultProfile</span></span>
<span data-ttu-id="0a915-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a915-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a915-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0a915-114">-Force</span></span>
<span data-ttu-id="0a915-115">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0a915-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a915-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="0a915-116">-MlWebService</span></span>
<span data-ttu-id="0a915-117">Удаляемая веб-служба.</span><span class="sxs-lookup"><span data-stu-id="0a915-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="0a915-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0a915-118">-Name</span></span>
<span data-ttu-id="0a915-119">Имя удаляемой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0a915-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="0a915-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a915-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a915-121">Группа ресурсов веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0a915-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="0a915-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a915-122">-Confirm</span></span>
<span data-ttu-id="0a915-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0a915-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a915-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a915-124">-WhatIf</span></span>
<span data-ttu-id="0a915-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a915-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a915-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0a915-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a915-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a915-127">CommonParameters</span></span>
<span data-ttu-id="0a915-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a915-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a915-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a915-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a915-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a915-130">INPUTS</span></span>

### <span data-ttu-id="0a915-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0a915-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0a915-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a915-132">OUTPUTS</span></span>

### <span data-ttu-id="0a915-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="0a915-133">System.Void</span></span>

## <span data-ttu-id="0a915-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a915-134">NOTES</span></span>
<span data-ttu-id="0a915-135">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0a915-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0a915-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a915-136">RELATED LINKS</span></span>
