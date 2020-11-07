---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913875"
---
# <span data-ttu-id="d3f1d-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d3f1d-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="d3f1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f1d-103">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3f1d-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f1d-106">Командлет **Remove-AzureRmAutoscaleSetting** удаляет параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="d3f1d-107">Вы должны указать имя параметра и имя группы ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="d3f1d-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d3f1d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3f1d-109">EXAMPLES</span></span>

## <span data-ttu-id="d3f1d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3f1d-110">PARAMETERS</span></span>

### <span data-ttu-id="d3f1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f1d-111">-DefaultProfile</span></span>
<span data-ttu-id="d3f1d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3f1d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3f1d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3f1d-113">-Name</span></span>
<span data-ttu-id="d3f1d-114">Задает имя параметра автомасштабирования, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="d3f1d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f1d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3f1d-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d3f1d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3f1d-117">-Confirm</span></span>
<span data-ttu-id="d3f1d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f1d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f1d-119">-WhatIf</span></span>
<span data-ttu-id="d3f1d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3f1d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f1d-122">CommonParameters</span></span>
<span data-ttu-id="d3f1d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3f1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f1d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f1d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f1d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3f1d-125">INPUTS</span></span>

### <span data-ttu-id="d3f1d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f1d-126">System.String</span></span>

## <span data-ttu-id="d3f1d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f1d-127">OUTPUTS</span></span>

### <span data-ttu-id="d3f1d-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d3f1d-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d3f1d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3f1d-129">NOTES</span></span>

## <span data-ttu-id="d3f1d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3f1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3f1d-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d3f1d-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="d3f1d-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d3f1d-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


