---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244521"
---
# <span data-ttu-id="d4290-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="d4290-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="d4290-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4290-102">SYNOPSIS</span></span>
<span data-ttu-id="d4290-103">Удаление содержимого с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="d4290-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="d4290-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4290-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4290-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4290-105">DESCRIPTION</span></span>
<span data-ttu-id="d4290-106">Remove-AzFrontDoorContent удаляет кэшированное содержимое на передней дверце</span><span class="sxs-lookup"><span data-stu-id="d4290-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="d4290-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4290-107">EXAMPLES</span></span>

### <span data-ttu-id="d4290-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4290-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="d4290-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4290-109">PARAMETERS</span></span>

### <span data-ttu-id="d4290-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="d4290-110">-ContentPath</span></span>
<span data-ttu-id="d4290-111">Пути к содержимому, которое нужно очистить.</span><span class="sxs-lookup"><span data-stu-id="d4290-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="d4290-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4290-112">-DefaultProfile</span></span>
<span data-ttu-id="d4290-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4290-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4290-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4290-114">-Name</span></span>
<span data-ttu-id="d4290-115">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="d4290-115">Front Door name.</span></span>

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

### <span data-ttu-id="d4290-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4290-116">-PassThru</span></span>
<span data-ttu-id="d4290-117">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="d4290-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="d4290-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4290-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4290-119">Название группы ресурсов передней дверцы</span><span class="sxs-lookup"><span data-stu-id="d4290-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="d4290-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4290-120">-Confirm</span></span>
<span data-ttu-id="d4290-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4290-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4290-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4290-122">-WhatIf</span></span>
<span data-ttu-id="d4290-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4290-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4290-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4290-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4290-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4290-125">CommonParameters</span></span>
<span data-ttu-id="d4290-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4290-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4290-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4290-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4290-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4290-128">INPUTS</span></span>

### <span data-ttu-id="d4290-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4290-129">None</span></span>

## <span data-ttu-id="d4290-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4290-130">OUTPUTS</span></span>

### <span data-ttu-id="d4290-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4290-131">System.Boolean</span></span>

## <span data-ttu-id="d4290-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4290-132">NOTES</span></span>

## <span data-ttu-id="d4290-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4290-133">RELATED LINKS</span></span>
