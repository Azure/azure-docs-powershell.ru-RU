---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237806"
---
# <span data-ttu-id="a7391-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="a7391-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="a7391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7391-102">SYNOPSIS</span></span>
<span data-ttu-id="a7391-103">Удаление содержимого на переднем входе</span><span class="sxs-lookup"><span data-stu-id="a7391-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="a7391-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7391-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7391-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7391-105">DESCRIPTION</span></span>
<span data-ttu-id="a7391-106">Remove-AzFrontDoorContent очищает кэшное содержимое на передней двери</span><span class="sxs-lookup"><span data-stu-id="a7391-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="a7391-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7391-107">EXAMPLES</span></span>

### <span data-ttu-id="a7391-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7391-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="a7391-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7391-109">PARAMETERS</span></span>

### <span data-ttu-id="a7391-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="a7391-110">-ContentPath</span></span>
<span data-ttu-id="a7391-111">Пути к нужному содержимому.</span><span class="sxs-lookup"><span data-stu-id="a7391-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="a7391-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7391-112">-DefaultProfile</span></span>
<span data-ttu-id="a7391-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7391-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7391-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a7391-114">-Name</span></span>
<span data-ttu-id="a7391-115">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="a7391-115">Front Door name.</span></span>

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

### <span data-ttu-id="a7391-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7391-116">-PassThru</span></span>
<span data-ttu-id="a7391-117">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="a7391-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="a7391-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7391-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7391-119">Название группы ресурсов в front Door</span><span class="sxs-lookup"><span data-stu-id="a7391-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="a7391-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7391-120">-Confirm</span></span>
<span data-ttu-id="a7391-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7391-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7391-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7391-122">-WhatIf</span></span>
<span data-ttu-id="a7391-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7391-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7391-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7391-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7391-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7391-125">CommonParameters</span></span>
<span data-ttu-id="a7391-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7391-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7391-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7391-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7391-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7391-128">INPUTS</span></span>

### <span data-ttu-id="a7391-129">Нет</span><span class="sxs-lookup"><span data-stu-id="a7391-129">None</span></span>

## <span data-ttu-id="a7391-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7391-130">OUTPUTS</span></span>

### <span data-ttu-id="a7391-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7391-131">System.Boolean</span></span>

## <span data-ttu-id="a7391-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7391-132">NOTES</span></span>

## <span data-ttu-id="a7391-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7391-133">RELATED LINKS</span></span>
