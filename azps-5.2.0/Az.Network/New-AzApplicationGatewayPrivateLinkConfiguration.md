---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417455"
---
# <span data-ttu-id="aad17-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="aad17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad17-102">SYNOPSIS</span></span>
<span data-ttu-id="aad17-103">Создает конфигурацию личной ссылки для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="aad17-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="aad17-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aad17-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad17-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad17-105">DESCRIPTION</span></span>
<span data-ttu-id="aad17-106">Для **шлюза приложения Azure** создается конфигурация PrivateLink для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="aad17-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="aad17-107">Чтобы она была активна, конфигурация частных ссылок должна быть связана с конфигурацией IP-адреса переднего звена.</span><span class="sxs-lookup"><span data-stu-id="aad17-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="aad17-108">Одну конфигурацию частных ссылок можно связать только с одной конфигурацией IP-адреса переднего звена в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="aad17-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="aad17-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aad17-109">EXAMPLES</span></span>

### <span data-ttu-id="aad17-110">Пример 1. Создание конфигурации личной ссылки с одним ip-адресом</span><span class="sxs-lookup"><span data-stu-id="aad17-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="aad17-111">Эта команда создает конфигурацию PrivateLink с именем PrivateLinkConfig01 и сохраняет результат в переменной с именем $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aad17-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="aad17-112">Пример 2. Создание конфигурации личной ссылки с несколькими конфигурациями IP-адресов</span><span class="sxs-lookup"><span data-stu-id="aad17-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="aad17-113">Эта команда создает конфигурацию PrivateLink с именем PrivateLinkConfig01 с двумя параметрами ipConfiguration и сохраняет результат в переменной с именем $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aad17-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="aad17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad17-114">PARAMETERS</span></span>

### <span data-ttu-id="aad17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad17-115">-DefaultProfile</span></span>
<span data-ttu-id="aad17-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aad17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad17-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-117">-IpConfiguration</span></span>
<span data-ttu-id="aad17-118">Список ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad17-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aad17-119">-Name</span></span>
<span data-ttu-id="aad17-120">Имя конфигурации PrivateLink</span><span class="sxs-lookup"><span data-stu-id="aad17-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="aad17-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad17-121">-Confirm</span></span>
<span data-ttu-id="aad17-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad17-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad17-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad17-123">-WhatIf</span></span>
<span data-ttu-id="aad17-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad17-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad17-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aad17-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad17-126">CommonParameters</span></span>
<span data-ttu-id="aad17-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad17-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aad17-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad17-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aad17-129">INPUTS</span></span>

### <span data-ttu-id="aad17-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="aad17-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="aad17-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aad17-131">OUTPUTS</span></span>

### <span data-ttu-id="aad17-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="aad17-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aad17-133">NOTES</span></span>

## <span data-ttu-id="aad17-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aad17-134">RELATED LINKS</span></span>

[<span data-ttu-id="aad17-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="aad17-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="aad17-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="aad17-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad17-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
