---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417583"
---
# <span data-ttu-id="20992-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="20992-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="20992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20992-102">SYNOPSIS</span></span>
<span data-ttu-id="20992-103">Настройка нового устройства Edge для полей данных</span><span class="sxs-lookup"><span data-stu-id="20992-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="20992-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20992-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20992-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20992-105">DESCRIPTION</span></span>
<span data-ttu-id="20992-106">Новый **буклет AzDataBoxEdgeDevice** настраивает новое устройство Edge box для данных.</span><span class="sxs-lookup"><span data-stu-id="20992-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="20992-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20992-107">EXAMPLES</span></span>

### <span data-ttu-id="20992-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20992-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="20992-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20992-109">PARAMETERS</span></span>

### <span data-ttu-id="20992-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20992-110">-AsJob</span></span>
<span data-ttu-id="20992-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="20992-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20992-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20992-112">-DefaultProfile</span></span>
<span data-ttu-id="20992-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20992-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20992-114">-Location</span><span class="sxs-lookup"><span data-stu-id="20992-114">-Location</span></span>
<span data-ttu-id="20992-115">Расположение устройства</span><span class="sxs-lookup"><span data-stu-id="20992-115">Location of the device</span></span>

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

### <span data-ttu-id="20992-116">-Name</span><span class="sxs-lookup"><span data-stu-id="20992-116">-Name</span></span>
<span data-ttu-id="20992-117">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="20992-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20992-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20992-118">-ResourceGroupName</span></span>
<span data-ttu-id="20992-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="20992-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20992-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="20992-120">-Sku</span></span>
<span data-ttu-id="20992-121">Доступны только skus: Edge и Gateway</span><span class="sxs-lookup"><span data-stu-id="20992-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="20992-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20992-122">-Confirm</span></span>
<span data-ttu-id="20992-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20992-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20992-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20992-124">-WhatIf</span></span>
<span data-ttu-id="20992-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20992-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20992-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="20992-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20992-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20992-127">CommonParameters</span></span>
<span data-ttu-id="20992-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20992-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20992-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20992-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20992-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20992-130">INPUTS</span></span>

### <span data-ttu-id="20992-131">Нет</span><span class="sxs-lookup"><span data-stu-id="20992-131">None</span></span>

## <span data-ttu-id="20992-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20992-132">OUTPUTS</span></span>

### <span data-ttu-id="20992-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="20992-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="20992-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20992-134">NOTES</span></span>

## <span data-ttu-id="20992-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20992-135">RELATED LINKS</span></span>
