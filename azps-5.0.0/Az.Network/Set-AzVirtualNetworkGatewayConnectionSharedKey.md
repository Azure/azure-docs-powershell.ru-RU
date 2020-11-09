---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247578"
---
# <span data-ttu-id="43ffa-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ffa-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="43ffa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="43ffa-103">Настройка общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="43ffa-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="43ffa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ffa-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ffa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ffa-105">DESCRIPTION</span></span>
<span data-ttu-id="43ffa-106">Командлет **Set-AzVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="43ffa-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="43ffa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ffa-107">EXAMPLES</span></span>

### <span data-ttu-id="43ffa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43ffa-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="43ffa-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ffa-109">PARAMETERS</span></span>

### <span data-ttu-id="43ffa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ffa-110">-DefaultProfile</span></span>
<span data-ttu-id="43ffa-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43ffa-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ffa-112">-Force</span><span class="sxs-lookup"><span data-stu-id="43ffa-112">-Force</span></span>
<span data-ttu-id="43ffa-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="43ffa-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43ffa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43ffa-114">-Name</span></span>
<span data-ttu-id="43ffa-115">Указывает имя общего ключа шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="43ffa-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ffa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ffa-116">-ResourceGroupName</span></span>
<span data-ttu-id="43ffa-117">Указывает имя группы ресурсов, к которой относится шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="43ffa-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ffa-118">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="43ffa-118">-Value</span></span>
<span data-ttu-id="43ffa-119">Задает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="43ffa-119">Specifies the value of the shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ffa-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43ffa-120">-Confirm</span></span>
<span data-ttu-id="43ffa-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43ffa-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ffa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ffa-122">-WhatIf</span></span>
<span data-ttu-id="43ffa-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43ffa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ffa-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43ffa-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ffa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ffa-125">CommonParameters</span></span>
<span data-ttu-id="43ffa-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ffa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ffa-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ffa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ffa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ffa-128">INPUTS</span></span>

### <span data-ttu-id="43ffa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="43ffa-129">System.String</span></span>

## <span data-ttu-id="43ffa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ffa-130">OUTPUTS</span></span>

### <span data-ttu-id="43ffa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="43ffa-131">System.String</span></span>

## <span data-ttu-id="43ffa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ffa-132">NOTES</span></span>

## <span data-ttu-id="43ffa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ffa-133">RELATED LINKS</span></span>

[<span data-ttu-id="43ffa-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ffa-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="43ffa-135">Сброс — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ffa-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)