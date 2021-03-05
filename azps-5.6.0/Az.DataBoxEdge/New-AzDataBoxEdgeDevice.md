---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978680"
---
# <span data-ttu-id="30cd9-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="30cd9-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="30cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="30cd9-103">Настройка нового устройства Edge для полей данных</span><span class="sxs-lookup"><span data-stu-id="30cd9-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="30cd9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30cd9-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30cd9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="30cd9-106">Новый **буклет AzDataBoxEdgeDevice** настраивает новое устройство Edge box для данных.</span><span class="sxs-lookup"><span data-stu-id="30cd9-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="30cd9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30cd9-107">EXAMPLES</span></span>

### <span data-ttu-id="30cd9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30cd9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="30cd9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30cd9-109">PARAMETERS</span></span>

### <span data-ttu-id="30cd9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30cd9-110">-AsJob</span></span>
<span data-ttu-id="30cd9-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30cd9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30cd9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cd9-112">-DefaultProfile</span></span>
<span data-ttu-id="30cd9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30cd9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30cd9-114">-Location</span><span class="sxs-lookup"><span data-stu-id="30cd9-114">-Location</span></span>
<span data-ttu-id="30cd9-115">Расположение устройства</span><span class="sxs-lookup"><span data-stu-id="30cd9-115">Location of the device</span></span>

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

### <span data-ttu-id="30cd9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="30cd9-116">-Name</span></span>
<span data-ttu-id="30cd9-117">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="30cd9-117">Resource Name</span></span>

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

### <span data-ttu-id="30cd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30cd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="30cd9-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="30cd9-119">Resource Group Name</span></span>

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

### <span data-ttu-id="30cd9-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="30cd9-120">-Sku</span></span>
<span data-ttu-id="30cd9-121">Доступны только skus: Edge и Gateway</span><span class="sxs-lookup"><span data-stu-id="30cd9-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="30cd9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30cd9-122">-Confirm</span></span>
<span data-ttu-id="30cd9-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="30cd9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30cd9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30cd9-124">-WhatIf</span></span>
<span data-ttu-id="30cd9-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30cd9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30cd9-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30cd9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30cd9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cd9-127">CommonParameters</span></span>
<span data-ttu-id="30cd9-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30cd9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cd9-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30cd9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cd9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30cd9-130">INPUTS</span></span>

### <span data-ttu-id="30cd9-131">Нет</span><span class="sxs-lookup"><span data-stu-id="30cd9-131">None</span></span>

## <span data-ttu-id="30cd9-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30cd9-132">OUTPUTS</span></span>

### <span data-ttu-id="30cd9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="30cd9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="30cd9-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30cd9-134">NOTES</span></span>

## <span data-ttu-id="30cd9-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30cd9-135">RELATED LINKS</span></span>
