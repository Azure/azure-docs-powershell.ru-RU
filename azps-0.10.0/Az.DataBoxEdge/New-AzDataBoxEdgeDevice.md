---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 353d4ca1e5f5eebd1cda1ec22d801a73db239963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911272"
---
# <span data-ttu-id="67569-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="67569-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="67569-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67569-102">SYNOPSIS</span></span>
<span data-ttu-id="67569-103">Настройка пограничного устройства "новое поле данных"</span><span class="sxs-lookup"><span data-stu-id="67569-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="67569-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67569-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67569-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67569-105">DESCRIPTION</span></span>
<span data-ttu-id="67569-106">Командлет **New-AzDataBoxEdgeDevice** настраивает новое пограничного устройства для полей данных</span><span class="sxs-lookup"><span data-stu-id="67569-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="67569-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67569-107">EXAMPLES</span></span>

### <span data-ttu-id="67569-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67569-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="67569-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67569-109">PARAMETERS</span></span>

### <span data-ttu-id="67569-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67569-110">-AsJob</span></span>
<span data-ttu-id="67569-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67569-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67569-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67569-112">-DefaultProfile</span></span>
<span data-ttu-id="67569-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67569-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67569-114">-Location</span><span class="sxs-lookup"><span data-stu-id="67569-114">-Location</span></span>
<span data-ttu-id="67569-115">Расположение устройства</span><span class="sxs-lookup"><span data-stu-id="67569-115">Location of the device</span></span>

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

### <span data-ttu-id="67569-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67569-116">-Name</span></span>
<span data-ttu-id="67569-117">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="67569-117">Resource Name</span></span>

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

### <span data-ttu-id="67569-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67569-118">-ResourceGroupName</span></span>
<span data-ttu-id="67569-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="67569-119">Resource Group Name</span></span>

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

### <span data-ttu-id="67569-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="67569-120">-Sku</span></span>
<span data-ttu-id="67569-121">Доступные SKU — EDGE, шлюз</span><span class="sxs-lookup"><span data-stu-id="67569-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="67569-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67569-122">-Confirm</span></span>
<span data-ttu-id="67569-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67569-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67569-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67569-124">-WhatIf</span></span>
<span data-ttu-id="67569-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67569-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67569-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67569-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67569-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67569-127">CommonParameters</span></span>
<span data-ttu-id="67569-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67569-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67569-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67569-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67569-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67569-130">INPUTS</span></span>

### <span data-ttu-id="67569-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="67569-131">None</span></span>

## <span data-ttu-id="67569-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67569-132">OUTPUTS</span></span>

### <span data-ttu-id="67569-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="67569-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="67569-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="67569-134">NOTES</span></span>

## <span data-ttu-id="67569-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67569-135">RELATED LINKS</span></span>
