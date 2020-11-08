---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 5b07928b78c8a6513e91c9e8ec21dbc27294552e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064844"
---
# <span data-ttu-id="78353-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78353-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="78353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78353-102">SYNOPSIS</span></span>
<span data-ttu-id="78353-103">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="78353-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="78353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78353-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78353-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78353-105">DESCRIPTION</span></span>
<span data-ttu-id="78353-106">Командлет **Remove-AzAutoscaleSetting** удаляет параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="78353-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="78353-107">Вы должны указать имя параметра и имя группы ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="78353-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="78353-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="78353-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="78353-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78353-109">EXAMPLES</span></span>

## <span data-ttu-id="78353-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78353-110">PARAMETERS</span></span>

### <span data-ttu-id="78353-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78353-111">-DefaultProfile</span></span>
<span data-ttu-id="78353-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78353-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78353-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78353-113">-Name</span></span>
<span data-ttu-id="78353-114">Задает имя параметра автомасштабирования, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="78353-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="78353-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78353-115">-ResourceGroupName</span></span>
<span data-ttu-id="78353-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78353-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78353-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78353-117">-Confirm</span></span>
<span data-ttu-id="78353-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78353-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78353-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78353-119">-WhatIf</span></span>
<span data-ttu-id="78353-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78353-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78353-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78353-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78353-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78353-122">CommonParameters</span></span>
<span data-ttu-id="78353-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78353-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78353-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78353-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78353-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78353-125">INPUTS</span></span>

### <span data-ttu-id="78353-126">System. String</span><span class="sxs-lookup"><span data-stu-id="78353-126">System.String</span></span>

## <span data-ttu-id="78353-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78353-127">OUTPUTS</span></span>

### <span data-ttu-id="78353-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78353-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="78353-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="78353-129">NOTES</span></span>

## <span data-ttu-id="78353-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78353-130">RELATED LINKS</span></span>

[<span data-ttu-id="78353-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78353-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="78353-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78353-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


