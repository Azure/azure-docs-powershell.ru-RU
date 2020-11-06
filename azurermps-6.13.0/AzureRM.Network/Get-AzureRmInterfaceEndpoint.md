---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564303"
---
# <span data-ttu-id="6bb90-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bb90-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="6bb90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bb90-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb90-103">Командлет Get-AzureRmInterfaceEndpoint получает конечную точку интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6bb90-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bb90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bb90-104">SYNTAX</span></span>

### <span data-ttu-id="6bb90-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bb90-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bb90-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bb90-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb90-107">DESCRIPTION</span></span>
<span data-ttu-id="6bb90-108">Командлет **Get-AzureRmInterfaceEndpoint** получает конечную точку интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6bb90-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="6bb90-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bb90-109">EXAMPLES</span></span>

### <span data-ttu-id="6bb90-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bb90-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6bb90-111">Эта команда получает конечную точку интерфейса с именем InterfaceEndpoint1, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="6bb90-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="6bb90-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bb90-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="6bb90-113">Эта команда получает конечную точку интерфейса с resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 и сохраняет ее в переменной $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="6bb90-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="6bb90-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb90-114">PARAMETERS</span></span>

### <span data-ttu-id="6bb90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb90-115">-DefaultProfile</span></span>
<span data-ttu-id="6bb90-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6bb90-117">-Name</span></span>
<span data-ttu-id="6bb90-118">Имя конечной точки интерфейса</span><span class="sxs-lookup"><span data-stu-id="6bb90-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb90-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bb90-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb90-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bb90-121">-ResourceId</span></span>
<span data-ttu-id="6bb90-122">{Определение ИД ресурса заполнения}}</span><span class="sxs-lookup"><span data-stu-id="6bb90-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bb90-123">-Confirm</span></span>
<span data-ttu-id="6bb90-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6bb90-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb90-125">-WhatIf</span></span>
<span data-ttu-id="6bb90-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6bb90-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb90-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6bb90-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb90-128">CommonParameters</span></span>
<span data-ttu-id="6bb90-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bb90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6bb90-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb90-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bb90-131">INPUTS</span></span>

### <span data-ttu-id="6bb90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6bb90-132">System.String</span></span>


## <span data-ttu-id="6bb90-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb90-133">OUTPUTS</span></span>

### <span data-ttu-id="6bb90-134">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bb90-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="6bb90-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bb90-135">NOTES</span></span>

## <span data-ttu-id="6bb90-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb90-136">RELATED LINKS</span></span>
