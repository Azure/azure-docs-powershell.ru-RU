---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556635"
---
# <span data-ttu-id="827f3-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="827f3-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="827f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="827f3-102">SYNOPSIS</span></span>
<span data-ttu-id="827f3-103">Удаление содержимого с передней дверцы</span><span class="sxs-lookup"><span data-stu-id="827f3-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="827f3-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="827f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="827f3-105">DESCRIPTION</span></span>
<span data-ttu-id="827f3-106">Remove-AzureRmFrontDoorContent удаляет кэшированное содержимое на передней дверце</span><span class="sxs-lookup"><span data-stu-id="827f3-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="827f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="827f3-107">EXAMPLES</span></span>

### <span data-ttu-id="827f3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="827f3-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="827f3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="827f3-109">PARAMETERS</span></span>

### <span data-ttu-id="827f3-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="827f3-110">-ContentPath</span></span>
<span data-ttu-id="827f3-111">Пути к содержимому, которое нужно очистить.</span><span class="sxs-lookup"><span data-stu-id="827f3-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="827f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827f3-112">-DefaultProfile</span></span>
<span data-ttu-id="827f3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="827f3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="827f3-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="827f3-114">-Name</span></span>
<span data-ttu-id="827f3-115">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="827f3-115">Front Door name.</span></span>

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

### <span data-ttu-id="827f3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="827f3-116">-PassThru</span></span>
<span data-ttu-id="827f3-117">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="827f3-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="827f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="827f3-119">Название группы ресурсов передней дверцы</span><span class="sxs-lookup"><span data-stu-id="827f3-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="827f3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="827f3-120">-Confirm</span></span>
<span data-ttu-id="827f3-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="827f3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="827f3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="827f3-122">-WhatIf</span></span>
<span data-ttu-id="827f3-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="827f3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="827f3-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="827f3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="827f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827f3-125">CommonParameters</span></span>
<span data-ttu-id="827f3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="827f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827f3-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827f3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827f3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="827f3-128">INPUTS</span></span>

### <span data-ttu-id="827f3-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="827f3-129">None</span></span>

## <span data-ttu-id="827f3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="827f3-130">OUTPUTS</span></span>

### <span data-ttu-id="827f3-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="827f3-131">System.Boolean</span></span>

## <span data-ttu-id="827f3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="827f3-132">NOTES</span></span>

## <span data-ttu-id="827f3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="827f3-133">RELATED LINKS</span></span>
