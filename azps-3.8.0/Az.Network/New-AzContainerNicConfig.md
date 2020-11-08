---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 75f05c76b76f37e936798766d9288ace38d1397f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074758"
---
# <span data-ttu-id="c78d4-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c78d4-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="c78d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c78d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c78d4-103">Создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="c78d4-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="c78d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c78d4-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c78d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c78d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c78d4-106">Командлет **New-AzContainerNicConfig** создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="c78d4-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="c78d4-107">Этот объект определяет характеристики сетевого интерфейса контейнера, созданного с помощью ссылки на родительский профиль сети.</span><span class="sxs-lookup"><span data-stu-id="c78d4-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="c78d4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c78d4-108">EXAMPLES</span></span>

### <span data-ttu-id="c78d4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c78d4-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="c78d4-110">Первая команда создает пустую конфигурацию сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="c78d4-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="c78d4-111">Вторая создает новый профиль сети, передающий ранее созданную конфигурацию сетевого интерфейса контейнера в качестве аргумента командлету New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="c78d4-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="c78d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c78d4-112">PARAMETERS</span></span>

### <span data-ttu-id="c78d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78d4-113">-DefaultProfile</span></span>
<span data-ttu-id="c78d4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c78d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c78d4-115">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="c78d4-115">-IpConfiguration</span></span>
<span data-ttu-id="c78d4-116">Коллекция профилей конфигурации IP-адресов, которые определяют, какие конфигурации IP создаются при создании экземпляра контейнера из конфигурации сетевого интерфейса контейнера</span><span class="sxs-lookup"><span data-stu-id="c78d4-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c78d4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c78d4-117">-Name</span></span>
<span data-ttu-id="c78d4-118">Имя конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="c78d4-118">Name of the container network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78d4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c78d4-119">-Confirm</span></span>
<span data-ttu-id="c78d4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c78d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c78d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c78d4-121">-WhatIf</span></span>
<span data-ttu-id="c78d4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c78d4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c78d4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c78d4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c78d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78d4-124">CommonParameters</span></span>
<span data-ttu-id="c78d4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c78d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78d4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c78d4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78d4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c78d4-127">INPUTS</span></span>

### <span data-ttu-id="c78d4-128">Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="c78d4-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="c78d4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c78d4-129">OUTPUTS</span></span>

### <span data-ttu-id="c78d4-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c78d4-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c78d4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c78d4-131">NOTES</span></span>

## <span data-ttu-id="c78d4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c78d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="c78d4-133">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c78d4-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
