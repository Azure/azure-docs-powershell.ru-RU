---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561688"
---
# <span data-ttu-id="5f61a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5f61a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="5f61a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f61a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f61a-103">Настройка общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5f61a-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f61a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f61a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f61a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f61a-105">DESCRIPTION</span></span>
<span data-ttu-id="5f61a-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5f61a-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="5f61a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f61a-107">EXAMPLES</span></span>

## <span data-ttu-id="5f61a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f61a-108">PARAMETERS</span></span>

### <span data-ttu-id="5f61a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f61a-109">-DefaultProfile</span></span>
<span data-ttu-id="5f61a-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f61a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f61a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5f61a-111">-Force</span></span>
<span data-ttu-id="5f61a-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f61a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f61a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f61a-113">-Name</span></span>
<span data-ttu-id="5f61a-114">Указывает имя общего ключа шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5f61a-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="5f61a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f61a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f61a-116">Указывает имя группы ресурсов, к которой относится шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5f61a-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="5f61a-117">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="5f61a-117">-Value</span></span>
<span data-ttu-id="5f61a-118">Задает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="5f61a-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="5f61a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f61a-119">-Confirm</span></span>
<span data-ttu-id="5f61a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f61a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f61a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f61a-121">-WhatIf</span></span>
<span data-ttu-id="5f61a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f61a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f61a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f61a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f61a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f61a-124">CommonParameters</span></span>
<span data-ttu-id="5f61a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f61a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f61a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f61a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f61a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f61a-127">INPUTS</span></span>

### <span data-ttu-id="5f61a-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="5f61a-128">None</span></span>
<span data-ttu-id="5f61a-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5f61a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f61a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f61a-130">OUTPUTS</span></span>

### <span data-ttu-id="5f61a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f61a-131">System.String</span></span>

## <span data-ttu-id="5f61a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f61a-132">NOTES</span></span>

## <span data-ttu-id="5f61a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f61a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f61a-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5f61a-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="5f61a-135">Сброс — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5f61a-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


