---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212348"
---
# <span data-ttu-id="82c0e-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="82c0e-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="82c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="82c0e-103">Настройка нового устройства Stack Edge</span><span class="sxs-lookup"><span data-stu-id="82c0e-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="82c0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82c0e-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c0e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="82c0e-106">Новый **cmdlet AzStackEdgeDevice** настраивает новое устройство Stack Edge</span><span class="sxs-lookup"><span data-stu-id="82c0e-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="82c0e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="82c0e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82c0e-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="82c0e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c0e-109">PARAMETERS</span></span>

### <span data-ttu-id="82c0e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82c0e-110">-AsJob</span></span>
<span data-ttu-id="82c0e-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="82c0e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82c0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c0e-112">-DefaultProfile</span></span>
<span data-ttu-id="82c0e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82c0e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c0e-114">-Location</span><span class="sxs-lookup"><span data-stu-id="82c0e-114">-Location</span></span>
<span data-ttu-id="82c0e-115">Расположение устройства</span><span class="sxs-lookup"><span data-stu-id="82c0e-115">Location of the device</span></span>

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

### <span data-ttu-id="82c0e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="82c0e-116">-Name</span></span>
<span data-ttu-id="82c0e-117">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="82c0e-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c0e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c0e-118">-ResourceGroupName</span></span>
<span data-ttu-id="82c0e-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="82c0e-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c0e-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="82c0e-120">-Sku</span></span>
<span data-ttu-id="82c0e-121">Доступны только skus: Edge и Gateway</span><span class="sxs-lookup"><span data-stu-id="82c0e-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="82c0e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82c0e-122">-Confirm</span></span>
<span data-ttu-id="82c0e-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c0e-124">-WhatIf</span></span>
<span data-ttu-id="82c0e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c0e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82c0e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82c0e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c0e-127">CommonParameters</span></span>
<span data-ttu-id="82c0e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c0e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82c0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c0e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82c0e-130">INPUTS</span></span>

### <span data-ttu-id="82c0e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="82c0e-131">None</span></span>

## <span data-ttu-id="82c0e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82c0e-132">OUTPUTS</span></span>

### <span data-ttu-id="82c0e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="82c0e-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="82c0e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82c0e-134">NOTES</span></span>

## <span data-ttu-id="82c0e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82c0e-135">RELATED LINKS</span></span>
