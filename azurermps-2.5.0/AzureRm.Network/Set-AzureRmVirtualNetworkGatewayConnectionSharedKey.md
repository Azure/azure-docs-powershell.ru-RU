---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914393"
---
# <span data-ttu-id="b7b70-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b7b70-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b7b70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7b70-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b70-103">Настройка общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7b70-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7b70-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7b70-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b70-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7b70-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b7b70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7b70-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b70-108">1:</span><span class="sxs-lookup"><span data-stu-id="b7b70-108">1:</span></span>
```

```

## <span data-ttu-id="b7b70-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7b70-109">PARAMETERS</span></span>

### <span data-ttu-id="b7b70-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b70-110">-DefaultProfile</span></span>
<span data-ttu-id="b7b70-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b70-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b70-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b7b70-112">-Force</span></span>
<span data-ttu-id="b7b70-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7b70-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7b70-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7b70-114">-Name</span></span>
<span data-ttu-id="b7b70-115">Указывает имя общего ключа шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7b70-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b70-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b70-116">-ResourceGroupName</span></span>
<span data-ttu-id="b7b70-117">Указывает имя группы ресурсов, к которой относится шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7b70-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="b7b70-118">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b7b70-118">-Value</span></span>
<span data-ttu-id="b7b70-119">Задает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="b7b70-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="b7b70-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7b70-120">-Confirm</span></span>
<span data-ttu-id="b7b70-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7b70-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b70-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b70-122">-WhatIf</span></span>
<span data-ttu-id="b7b70-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7b70-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b70-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7b70-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b70-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b70-125">CommonParameters</span></span>
<span data-ttu-id="b7b70-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7b70-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b70-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b70-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b70-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7b70-128">INPUTS</span></span>

## <span data-ttu-id="b7b70-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7b70-129">OUTPUTS</span></span>

### <span data-ttu-id="b7b70-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b70-130">System.String</span></span>

## <span data-ttu-id="b7b70-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7b70-131">NOTES</span></span>

## <span data-ttu-id="b7b70-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7b70-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7b70-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b7b70-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b7b70-134">Сброс — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b7b70-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


