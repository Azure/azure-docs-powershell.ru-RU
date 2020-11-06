---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564260"
---
# <span data-ttu-id="31d7e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31d7e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="31d7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="31d7e-103">Создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="31d7e-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31d7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31d7e-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31d7e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="31d7e-106">Командлет **New-AzureRmLoadBalancerBackendAddressPoolConfig** создает конфигурацию пула серверных адресов для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="31d7e-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="31d7e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="31d7e-108">Пример 1: создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="31d7e-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="31d7e-109">Эта команда создает конфигурацию пула адресных адресов с именем BackendAddressPool02 для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="31d7e-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="31d7e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="31d7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d7e-111">-DefaultProfile</span></span>
<span data-ttu-id="31d7e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31d7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d7e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31d7e-113">-Name</span></span>
<span data-ttu-id="31d7e-114">Указывает имя создаваемой конфигурации пула адресов.</span><span class="sxs-lookup"><span data-stu-id="31d7e-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="31d7e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31d7e-115">-Confirm</span></span>
<span data-ttu-id="31d7e-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31d7e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31d7e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31d7e-117">-WhatIf</span></span>
<span data-ttu-id="31d7e-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31d7e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31d7e-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31d7e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31d7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d7e-120">CommonParameters</span></span>
<span data-ttu-id="31d7e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31d7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d7e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d7e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d7e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31d7e-123">INPUTS</span></span>

### <span data-ttu-id="31d7e-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="31d7e-124">None</span></span>

## <span data-ttu-id="31d7e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d7e-125">OUTPUTS</span></span>

### <span data-ttu-id="31d7e-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="31d7e-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="31d7e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="31d7e-127">NOTES</span></span>

## <span data-ttu-id="31d7e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31d7e-128">RELATED LINKS</span></span>

[<span data-ttu-id="31d7e-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31d7e-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="31d7e-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31d7e-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="31d7e-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="31d7e-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


