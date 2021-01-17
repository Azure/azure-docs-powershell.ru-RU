---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398660"
---
# <span data-ttu-id="9cc96-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9cc96-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="9cc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc96-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc96-103">Создает конфигурацию пула адресов для резерва нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9cc96-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="9cc96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9cc96-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc96-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cc96-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc96-106">С **помощью cmdlet New-AzLoadBalancerBackendAddressPoolConfig** создается конфигурация пула адресов для резервирования нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc96-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9cc96-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9cc96-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc96-108">Пример 1. Создание конфигурации пула адресов для резерва нагрузки</span><span class="sxs-lookup"><span data-stu-id="9cc96-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="9cc96-109">Эта команда создает конфигурацию пула адресов для дополнительных адресов с именем BackendAddressPool02 для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9cc96-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="9cc96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cc96-110">PARAMETERS</span></span>

### <span data-ttu-id="9cc96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc96-111">-DefaultProfile</span></span>
<span data-ttu-id="9cc96-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc96-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cc96-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9cc96-113">-Name</span></span>
<span data-ttu-id="9cc96-114">Указывает имя созда создаемой конфигурации пула адресов.</span><span class="sxs-lookup"><span data-stu-id="9cc96-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="9cc96-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cc96-115">-Confirm</span></span>
<span data-ttu-id="9cc96-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cc96-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc96-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc96-117">-WhatIf</span></span>
<span data-ttu-id="9cc96-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cc96-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cc96-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9cc96-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc96-120">CommonParameters</span></span>
<span data-ttu-id="9cc96-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc96-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc96-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc96-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cc96-123">INPUTS</span></span>

### <span data-ttu-id="9cc96-124">Нет</span><span class="sxs-lookup"><span data-stu-id="9cc96-124">None</span></span>

## <span data-ttu-id="9cc96-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cc96-125">OUTPUTS</span></span>

### <span data-ttu-id="9cc96-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9cc96-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9cc96-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9cc96-127">NOTES</span></span>

## <span data-ttu-id="9cc96-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cc96-128">RELATED LINKS</span></span>

[<span data-ttu-id="9cc96-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9cc96-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9cc96-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9cc96-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9cc96-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9cc96-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


