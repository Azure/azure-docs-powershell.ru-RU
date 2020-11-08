---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243826"
---
# <span data-ttu-id="f7b53-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f7b53-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="f7b53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7b53-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b53-103">Настройка нового пограничного устройства в стопке</span><span class="sxs-lookup"><span data-stu-id="f7b53-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="f7b53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7b53-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b53-105">DESCRIPTION</span></span>
<span data-ttu-id="f7b53-106">Командлет **New-AzStackEdgeDevice** настраивает новое пограничное устройство для стеков.</span><span class="sxs-lookup"><span data-stu-id="f7b53-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="f7b53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7b53-107">EXAMPLES</span></span>

### <span data-ttu-id="f7b53-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7b53-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="f7b53-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7b53-109">PARAMETERS</span></span>

### <span data-ttu-id="f7b53-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b53-110">-AsJob</span></span>
<span data-ttu-id="f7b53-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f7b53-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7b53-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b53-112">-DefaultProfile</span></span>
<span data-ttu-id="f7b53-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b53-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b53-114">-Location</span><span class="sxs-lookup"><span data-stu-id="f7b53-114">-Location</span></span>
<span data-ttu-id="f7b53-115">Расположение устройства</span><span class="sxs-lookup"><span data-stu-id="f7b53-115">Location of the device</span></span>

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

### <span data-ttu-id="f7b53-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7b53-116">-Name</span></span>
<span data-ttu-id="f7b53-117">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f7b53-117">Resource Name</span></span>

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

### <span data-ttu-id="f7b53-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b53-118">-ResourceGroupName</span></span>
<span data-ttu-id="f7b53-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f7b53-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f7b53-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="f7b53-120">-Sku</span></span>
<span data-ttu-id="f7b53-121">Доступные SKU — EDGE, шлюз</span><span class="sxs-lookup"><span data-stu-id="f7b53-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="f7b53-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7b53-122">-Confirm</span></span>
<span data-ttu-id="f7b53-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b53-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b53-124">-WhatIf</span></span>
<span data-ttu-id="f7b53-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b53-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7b53-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7b53-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b53-127">CommonParameters</span></span>
<span data-ttu-id="f7b53-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7b53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b53-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b53-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b53-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7b53-130">INPUTS</span></span>

### <span data-ttu-id="f7b53-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7b53-131">None</span></span>

## <span data-ttu-id="f7b53-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b53-132">OUTPUTS</span></span>

### <span data-ttu-id="f7b53-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f7b53-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f7b53-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7b53-134">NOTES</span></span>

## <span data-ttu-id="f7b53-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7b53-135">RELATED LINKS</span></span>
