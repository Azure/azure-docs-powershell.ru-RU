---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909698"
---
# <span data-ttu-id="7f410-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f410-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="7f410-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f410-102">SYNOPSIS</span></span>
<span data-ttu-id="7f410-103">Создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7f410-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="7f410-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f410-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f410-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f410-105">DESCRIPTION</span></span>
<span data-ttu-id="7f410-106">Командлет **New-AzLoadBalancerBackendAddressPoolConfig** создает конфигурацию пула серверных адресов для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="7f410-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7f410-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f410-107">EXAMPLES</span></span>

### <span data-ttu-id="7f410-108">Пример 1: создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="7f410-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="7f410-109">Эта команда создает конфигурацию пула адресных адресов с именем BackendAddressPool02 для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7f410-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="7f410-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f410-110">PARAMETERS</span></span>

### <span data-ttu-id="7f410-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f410-111">-DefaultProfile</span></span>
<span data-ttu-id="7f410-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f410-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f410-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f410-113">-Name</span></span>
<span data-ttu-id="7f410-114">Указывает имя создаваемой конфигурации пула адресов.</span><span class="sxs-lookup"><span data-stu-id="7f410-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="7f410-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f410-115">CommonParameters</span></span>
<span data-ttu-id="7f410-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f410-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f410-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f410-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f410-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f410-118">INPUTS</span></span>

## <span data-ttu-id="7f410-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f410-119">OUTPUTS</span></span>

### <span data-ttu-id="7f410-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f410-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="7f410-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f410-121">NOTES</span></span>

## <span data-ttu-id="7f410-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f410-122">RELATED LINKS</span></span>

[<span data-ttu-id="7f410-123">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f410-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7f410-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f410-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="7f410-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f410-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


