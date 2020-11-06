---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565221"
---
# <span data-ttu-id="d432b-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d432b-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="d432b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d432b-102">SYNOPSIS</span></span>
<span data-ttu-id="d432b-103">Настройка общего ключа подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d432b-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d432b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d432b-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d432b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d432b-105">DESCRIPTION</span></span>
<span data-ttu-id="d432b-106">Командлет **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d432b-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="d432b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d432b-107">EXAMPLES</span></span>

## <span data-ttu-id="d432b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d432b-108">PARAMETERS</span></span>

### <span data-ttu-id="d432b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="d432b-109">-Force</span></span>
<span data-ttu-id="d432b-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d432b-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d432b-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d432b-111">-Name</span></span>
<span data-ttu-id="d432b-112">Указывает имя общего ключа шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d432b-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="d432b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d432b-113">-ResourceGroupName</span></span>
<span data-ttu-id="d432b-114">Указывает имя группы ресурсов, к которой относится шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d432b-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="d432b-115">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="d432b-115">-Value</span></span>
<span data-ttu-id="d432b-116">Задает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="d432b-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="d432b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d432b-117">-Confirm</span></span>
<span data-ttu-id="d432b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d432b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d432b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d432b-119">-WhatIf</span></span>
<span data-ttu-id="d432b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d432b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d432b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d432b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d432b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d432b-122">-DefaultProfile</span></span>
<span data-ttu-id="d432b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d432b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d432b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d432b-124">CommonParameters</span></span>
<span data-ttu-id="d432b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d432b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d432b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d432b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d432b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d432b-127">INPUTS</span></span>

## <span data-ttu-id="d432b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d432b-128">OUTPUTS</span></span>

### <span data-ttu-id="d432b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d432b-129">System.String</span></span>

## <span data-ttu-id="d432b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d432b-130">NOTES</span></span>

## <span data-ttu-id="d432b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d432b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d432b-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d432b-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="d432b-133">Сброс — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d432b-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


