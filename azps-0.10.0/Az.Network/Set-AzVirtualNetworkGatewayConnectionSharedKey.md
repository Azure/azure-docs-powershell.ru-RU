---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2683af757bc1b0b58ebb6865a1cfd1edeef580e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911004"
---
# <span data-ttu-id="8f207-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8f207-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="8f207-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f207-102">SYNOPSIS</span></span>
<span data-ttu-id="8f207-103">Настройка общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f207-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="8f207-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f207-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f207-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f207-105">DESCRIPTION</span></span>
<span data-ttu-id="8f207-106">Командлет **Set-AzVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f207-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="8f207-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f207-107">EXAMPLES</span></span>

### <span data-ttu-id="8f207-108">1:</span><span class="sxs-lookup"><span data-stu-id="8f207-108">1:</span></span>
```

```

## <span data-ttu-id="8f207-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f207-109">PARAMETERS</span></span>

### <span data-ttu-id="8f207-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f207-110">-DefaultProfile</span></span>
<span data-ttu-id="8f207-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f207-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f207-112">-Force</span><span class="sxs-lookup"><span data-stu-id="8f207-112">-Force</span></span>
<span data-ttu-id="8f207-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f207-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f207-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f207-114">-Name</span></span>
<span data-ttu-id="8f207-115">Указывает имя общего ключа шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f207-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="8f207-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f207-116">-ResourceGroupName</span></span>
<span data-ttu-id="8f207-117">Указывает имя группы ресурсов, к которой относится шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8f207-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="8f207-118">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="8f207-118">-Value</span></span>
<span data-ttu-id="8f207-119">Задает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="8f207-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="8f207-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f207-120">-Confirm</span></span>
<span data-ttu-id="8f207-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f207-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f207-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f207-122">-WhatIf</span></span>
<span data-ttu-id="8f207-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f207-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f207-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f207-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f207-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f207-125">CommonParameters</span></span>
<span data-ttu-id="8f207-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f207-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f207-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f207-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f207-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f207-128">INPUTS</span></span>

## <span data-ttu-id="8f207-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f207-129">OUTPUTS</span></span>

### <span data-ttu-id="8f207-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8f207-130">System.String</span></span>

## <span data-ttu-id="8f207-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f207-131">NOTES</span></span>

## <span data-ttu-id="8f207-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f207-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f207-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8f207-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="8f207-134">Сброс — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8f207-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)


