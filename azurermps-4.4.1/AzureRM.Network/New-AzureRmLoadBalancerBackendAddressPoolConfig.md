---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a810d85a96bd0686ca4ac98b7feb0dd4f905bd9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568730"
---
# <span data-ttu-id="e395f-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e395f-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e395f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e395f-102">SYNOPSIS</span></span>
<span data-ttu-id="e395f-103">Создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e395f-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e395f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e395f-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e395f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e395f-105">DESCRIPTION</span></span>
<span data-ttu-id="e395f-106">Командлет **New-AzureRmLoadBalancerBackendAddressPoolConfig** создает конфигурацию пула серверных адресов для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="e395f-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e395f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e395f-107">EXAMPLES</span></span>

### <span data-ttu-id="e395f-108">Пример 1: создание конфигурации пула адресных адресов для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="e395f-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e395f-109">Эта команда создает конфигурацию пула адресных адресов с именем BackendAddressPool02 для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e395f-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e395f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e395f-110">PARAMETERS</span></span>

### <span data-ttu-id="e395f-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e395f-111">-Name</span></span>
<span data-ttu-id="e395f-112">Указывает имя создаваемой конфигурации пула адресов.</span><span class="sxs-lookup"><span data-stu-id="e395f-112">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="e395f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e395f-113">-DefaultProfile</span></span>
<span data-ttu-id="e395f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e395f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e395f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e395f-115">CommonParameters</span></span>
<span data-ttu-id="e395f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e395f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e395f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e395f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e395f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e395f-118">INPUTS</span></span>

## <span data-ttu-id="e395f-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e395f-119">OUTPUTS</span></span>

### <span data-ttu-id="e395f-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e395f-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e395f-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e395f-121">NOTES</span></span>

## <span data-ttu-id="e395f-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e395f-122">RELATED LINKS</span></span>

[<span data-ttu-id="e395f-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e395f-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e395f-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e395f-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e395f-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e395f-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


