---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 21cc1e70e0122e21dac5cb78cfa4f4346cf72e5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903230"
---
# <span data-ttu-id="adcc0-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adcc0-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="adcc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adcc0-102">SYNOPSIS</span></span>
<span data-ttu-id="adcc0-103">Удаление параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="adcc0-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="adcc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adcc0-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adcc0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adcc0-105">DESCRIPTION</span></span>
<span data-ttu-id="adcc0-106">Командлет **Remove-AzAutoscaleSetting** удаляет параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="adcc0-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="adcc0-107">Вы должны указать имя параметра и имя группы ресурсов, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="adcc0-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="adcc0-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="adcc0-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="adcc0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adcc0-109">EXAMPLES</span></span>

## <span data-ttu-id="adcc0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adcc0-110">PARAMETERS</span></span>

### <span data-ttu-id="adcc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcc0-111">-DefaultProfile</span></span>
<span data-ttu-id="adcc0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="adcc0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adcc0-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adcc0-113">-Name</span></span>
<span data-ttu-id="adcc0-114">Задает имя параметра автомасштабирования, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="adcc0-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="adcc0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adcc0-115">-ResourceGroupName</span></span>
<span data-ttu-id="adcc0-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adcc0-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="adcc0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adcc0-117">-Confirm</span></span>
<span data-ttu-id="adcc0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="adcc0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adcc0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adcc0-119">-WhatIf</span></span>
<span data-ttu-id="adcc0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="adcc0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adcc0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="adcc0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adcc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcc0-122">CommonParameters</span></span>
<span data-ttu-id="adcc0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adcc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcc0-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adcc0-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcc0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adcc0-125">INPUTS</span></span>

### <span data-ttu-id="adcc0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="adcc0-126">System.String</span></span>

## <span data-ttu-id="adcc0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adcc0-127">OUTPUTS</span></span>

### <span data-ttu-id="adcc0-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="adcc0-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="adcc0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="adcc0-129">NOTES</span></span>

## <span data-ttu-id="adcc0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adcc0-130">RELATED LINKS</span></span>

[<span data-ttu-id="adcc0-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adcc0-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="adcc0-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adcc0-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


