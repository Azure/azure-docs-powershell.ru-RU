---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244874"
---
# <span data-ttu-id="3a615-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="3a615-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a615-102">SYNOPSIS</span></span>
<span data-ttu-id="3a615-103">Создание конфигурации частной ссылки для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3a615-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="3a615-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a615-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a615-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a615-105">DESCRIPTION</span></span>
<span data-ttu-id="3a615-106">Командлет **New-AzApplicationGatewayPrivateLinkConfiguration** создает конфигурацию PrivateLink для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3a615-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="3a615-107">Чтобы включить функцию закрытой связи, необходимо связать конфигурацию частной ссылки с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3a615-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="3a615-108">Одну из конфигураций личных ссылок можно atmost только в конфигурации с интерфейсом IP на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="3a615-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="3a615-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a615-109">EXAMPLES</span></span>

### <span data-ttu-id="3a615-110">Пример 1: создание конфигурации частной ссылки с единственной IP-конфигурацией</span><span class="sxs-lookup"><span data-stu-id="3a615-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="3a615-111">Эта команда создает конфигурацию PrivateLink с именем "privateLinkConfig01" и сохраняет результат в переменной с именем $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a615-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="3a615-112">Пример 2: создание конфигурации частной ссылки с несколькими IP-конфигурациями</span><span class="sxs-lookup"><span data-stu-id="3a615-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="3a615-113">Эта команда создает конфигурацию PrivateLink с именем "privateLinkConfig01" с двумя ipConfigurations и сохраняет результат в переменной с именем $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a615-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="3a615-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a615-114">PARAMETERS</span></span>

### <span data-ttu-id="3a615-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a615-115">-DefaultProfile</span></span>
<span data-ttu-id="3a615-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a615-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a615-117">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="3a615-117">-IpConfiguration</span></span>
<span data-ttu-id="3a615-118">Список IP.</span><span class="sxs-lookup"><span data-stu-id="3a615-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="3a615-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a615-119">-Name</span></span>
<span data-ttu-id="3a615-120">Имя конфигурации privateLink</span><span class="sxs-lookup"><span data-stu-id="3a615-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="3a615-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a615-121">-Confirm</span></span>
<span data-ttu-id="3a615-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a615-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a615-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a615-123">-WhatIf</span></span>
<span data-ttu-id="3a615-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a615-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a615-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a615-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a615-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a615-126">CommonParameters</span></span>
<span data-ttu-id="3a615-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a615-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a615-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a615-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a615-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a615-129">INPUTS</span></span>

### <span data-ttu-id="3a615-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="3a615-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="3a615-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a615-131">OUTPUTS</span></span>

### <span data-ttu-id="3a615-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="3a615-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a615-133">NOTES</span></span>

## <span data-ttu-id="3a615-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a615-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a615-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3a615-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3a615-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3a615-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a615-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
