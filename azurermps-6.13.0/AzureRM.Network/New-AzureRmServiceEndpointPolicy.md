---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567707"
---
# <span data-ttu-id="61dfc-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61dfc-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="61dfc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="61dfc-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="61dfc-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61dfc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61dfc-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61dfc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="61dfc-106">Командлет **New-AzureRmServiceEndpointPolicy** создает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="61dfc-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="61dfc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="61dfc-108">Пример 1: Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="61dfc-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="61dfc-109">Эта команда создает политику конечной точки службы с именем Policy1 с определениями, определенными объектом, $serviceEndpointDefinition и сохраняет их в переменной $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="61dfc-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="61dfc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="61dfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dfc-111">-DefaultProfile</span></span>
<span data-ttu-id="61dfc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61dfc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61dfc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="61dfc-113">-Force</span></span>
<span data-ttu-id="61dfc-114">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="61dfc-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dfc-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61dfc-115">-Name</span></span>
<span data-ttu-id="61dfc-116">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="61dfc-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61dfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="61dfc-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61dfc-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61dfc-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="61dfc-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="61dfc-120">Список определений конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="61dfc-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dfc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61dfc-121">-Confirm</span></span>
<span data-ttu-id="61dfc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61dfc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dfc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dfc-123">-WhatIf</span></span>
<span data-ttu-id="61dfc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61dfc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61dfc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61dfc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dfc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dfc-126">CommonParameters</span></span>
<span data-ttu-id="61dfc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61dfc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="61dfc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61dfc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dfc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61dfc-129">INPUTS</span></span>

### <span data-ttu-id="61dfc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61dfc-130">System.String</span></span>


## <span data-ttu-id="61dfc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61dfc-131">OUTPUTS</span></span>

### <span data-ttu-id="61dfc-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61dfc-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="61dfc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="61dfc-133">NOTES</span></span>

## <span data-ttu-id="61dfc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61dfc-134">RELATED LINKS</span></span>
