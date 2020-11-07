---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: f48dedc50ae134967a57320b065389505aa9c1ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900593"
---
# <span data-ttu-id="8e742-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="8e742-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="8e742-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e742-102">SYNOPSIS</span></span>
<span data-ttu-id="8e742-103">Удаление содержимого с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="8e742-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="8e742-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e742-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e742-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e742-105">DESCRIPTION</span></span>
<span data-ttu-id="8e742-106">Remove-AzFrontDoorContent удаляет кэшированное содержимое на передней дверце</span><span class="sxs-lookup"><span data-stu-id="8e742-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="8e742-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e742-107">EXAMPLES</span></span>

### <span data-ttu-id="8e742-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e742-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="8e742-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e742-109">PARAMETERS</span></span>

### <span data-ttu-id="8e742-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="8e742-110">-ContentPath</span></span>
<span data-ttu-id="8e742-111">Пути к содержимому, которое нужно очистить.</span><span class="sxs-lookup"><span data-stu-id="8e742-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="8e742-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e742-112">-DefaultProfile</span></span>
<span data-ttu-id="8e742-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e742-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e742-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e742-114">-Name</span></span>
<span data-ttu-id="8e742-115">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8e742-115">Front Door name.</span></span>

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

### <span data-ttu-id="8e742-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e742-116">-PassThru</span></span>
<span data-ttu-id="8e742-117">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="8e742-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="8e742-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e742-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e742-119">Название группы ресурсов передней дверцы</span><span class="sxs-lookup"><span data-stu-id="8e742-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="8e742-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e742-120">-Confirm</span></span>
<span data-ttu-id="8e742-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e742-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e742-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e742-122">-WhatIf</span></span>
<span data-ttu-id="8e742-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e742-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e742-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e742-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e742-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e742-125">CommonParameters</span></span>
<span data-ttu-id="8e742-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e742-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e742-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e742-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e742-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e742-128">INPUTS</span></span>

### <span data-ttu-id="8e742-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="8e742-129">None</span></span>

## <span data-ttu-id="8e742-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e742-130">OUTPUTS</span></span>

### <span data-ttu-id="8e742-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e742-131">System.Boolean</span></span>

## <span data-ttu-id="8e742-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e742-132">NOTES</span></span>

## <span data-ttu-id="8e742-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e742-133">RELATED LINKS</span></span>
