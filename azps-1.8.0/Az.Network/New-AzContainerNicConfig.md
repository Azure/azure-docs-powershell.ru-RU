---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 18d5891e07dd9d0f9916ebf43e8967152e2c9cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730364"
---
# <span data-ttu-id="95392-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="95392-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="95392-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95392-102">SYNOPSIS</span></span>
<span data-ttu-id="95392-103">Создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="95392-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="95392-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95392-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95392-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95392-105">DESCRIPTION</span></span>
<span data-ttu-id="95392-106">Командлет **New-AzContainerNicConfig** создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="95392-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="95392-107">Этот объект определяет характеристики сетевого interfacs, созданного на родительском сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="95392-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="95392-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95392-108">EXAMPLES</span></span>

### <span data-ttu-id="95392-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95392-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="95392-110">Первая команда создает пустую конфигурацию сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="95392-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="95392-111">Вторая создает новый профиль сети, передающий ранее созданную конфигурацию сетевого интерфейса контейнера в качестве аргумента командлету New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="95392-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="95392-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95392-112">PARAMETERS</span></span>

### <span data-ttu-id="95392-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95392-113">-DefaultProfile</span></span>
<span data-ttu-id="95392-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95392-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95392-115">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="95392-115">-IpConfiguration</span></span>
<span data-ttu-id="95392-116">Коллекция профилей конфигурации IP-адресов, которые определяют, какие конфигурации IP создаются при создании экземпляра контейнера из конфигурации сетевого интерфейса контейнера</span><span class="sxs-lookup"><span data-stu-id="95392-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

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

### <span data-ttu-id="95392-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95392-117">-Name</span></span>
<span data-ttu-id="95392-118">Имя конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="95392-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="95392-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95392-119">-Confirm</span></span>
<span data-ttu-id="95392-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95392-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95392-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95392-121">-WhatIf</span></span>
<span data-ttu-id="95392-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95392-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95392-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95392-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95392-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95392-124">CommonParameters</span></span>
<span data-ttu-id="95392-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95392-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95392-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95392-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95392-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95392-127">INPUTS</span></span>

### <span data-ttu-id="95392-128">Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="95392-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="95392-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95392-129">OUTPUTS</span></span>

### <span data-ttu-id="95392-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="95392-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="95392-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="95392-131">NOTES</span></span>

## <span data-ttu-id="95392-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95392-132">RELATED LINKS</span></span>

[<span data-ttu-id="95392-133">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="95392-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
