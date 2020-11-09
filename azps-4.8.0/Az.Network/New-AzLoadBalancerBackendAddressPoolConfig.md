---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244831"
---
# <span data-ttu-id="c117d-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c117d-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c117d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c117d-102">SYNOPSIS</span></span>
<span data-ttu-id="c117d-103">Создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c117d-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c117d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c117d-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c117d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c117d-105">DESCRIPTION</span></span>
<span data-ttu-id="c117d-106">Командлет **New-AzLoadBalancerBackendAddressPoolConfig** создает конфигурацию пула серверных адресов для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="c117d-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c117d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c117d-107">EXAMPLES</span></span>

### <span data-ttu-id="c117d-108">Пример 1: создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c117d-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="c117d-109">Эта команда создает конфигурацию пула адресных адресов с именем BackendAddressPool02 для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c117d-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="c117d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c117d-110">PARAMETERS</span></span>

### <span data-ttu-id="c117d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c117d-111">-DefaultProfile</span></span>
<span data-ttu-id="c117d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c117d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c117d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c117d-113">-Name</span></span>
<span data-ttu-id="c117d-114">Указывает имя создаваемой конфигурации пула адресов.</span><span class="sxs-lookup"><span data-stu-id="c117d-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="c117d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c117d-115">-Confirm</span></span>
<span data-ttu-id="c117d-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c117d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c117d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c117d-117">-WhatIf</span></span>
<span data-ttu-id="c117d-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c117d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c117d-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c117d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c117d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c117d-120">CommonParameters</span></span>
<span data-ttu-id="c117d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c117d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c117d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c117d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c117d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c117d-123">INPUTS</span></span>

### <span data-ttu-id="c117d-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="c117d-124">None</span></span>

## <span data-ttu-id="c117d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c117d-125">OUTPUTS</span></span>

### <span data-ttu-id="c117d-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c117d-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c117d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c117d-127">NOTES</span></span>

## <span data-ttu-id="c117d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c117d-128">RELATED LINKS</span></span>

[<span data-ttu-id="c117d-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c117d-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c117d-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c117d-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c117d-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c117d-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

