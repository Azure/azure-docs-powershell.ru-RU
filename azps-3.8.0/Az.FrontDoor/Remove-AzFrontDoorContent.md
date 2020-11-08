---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065176"
---
# <span data-ttu-id="85efe-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="85efe-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="85efe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85efe-102">SYNOPSIS</span></span>
<span data-ttu-id="85efe-103">Удаление содержимого с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="85efe-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="85efe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85efe-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85efe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85efe-105">DESCRIPTION</span></span>
<span data-ttu-id="85efe-106">Remove-AzFrontDoorContent удаляет кэшированное содержимое на передней дверце</span><span class="sxs-lookup"><span data-stu-id="85efe-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="85efe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85efe-107">EXAMPLES</span></span>

### <span data-ttu-id="85efe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85efe-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="85efe-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85efe-109">PARAMETERS</span></span>

### <span data-ttu-id="85efe-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="85efe-110">-ContentPath</span></span>
<span data-ttu-id="85efe-111">Пути к содержимому, которое нужно очистить.</span><span class="sxs-lookup"><span data-stu-id="85efe-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85efe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85efe-112">-DefaultProfile</span></span>
<span data-ttu-id="85efe-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85efe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85efe-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85efe-114">-Name</span></span>
<span data-ttu-id="85efe-115">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="85efe-115">Front Door name.</span></span>

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

### <span data-ttu-id="85efe-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85efe-116">-PassThru</span></span>
<span data-ttu-id="85efe-117">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="85efe-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="85efe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85efe-118">-ResourceGroupName</span></span>
<span data-ttu-id="85efe-119">Название группы ресурсов передней дверцы</span><span class="sxs-lookup"><span data-stu-id="85efe-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="85efe-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85efe-120">-Confirm</span></span>
<span data-ttu-id="85efe-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85efe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85efe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85efe-122">-WhatIf</span></span>
<span data-ttu-id="85efe-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85efe-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85efe-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85efe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85efe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85efe-125">CommonParameters</span></span>
<span data-ttu-id="85efe-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85efe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85efe-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85efe-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85efe-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85efe-128">INPUTS</span></span>

### <span data-ttu-id="85efe-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="85efe-129">None</span></span>

## <span data-ttu-id="85efe-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85efe-130">OUTPUTS</span></span>

### <span data-ttu-id="85efe-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85efe-131">System.Boolean</span></span>

## <span data-ttu-id="85efe-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="85efe-132">NOTES</span></span>

## <span data-ttu-id="85efe-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85efe-133">RELATED LINKS</span></span>
