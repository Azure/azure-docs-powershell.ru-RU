---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734930"
---
# <span data-ttu-id="5495c-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5495c-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="5495c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5495c-102">SYNOPSIS</span></span>
<span data-ttu-id="5495c-103">Создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5495c-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5495c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5495c-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5495c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5495c-105">DESCRIPTION</span></span>
<span data-ttu-id="5495c-106">Командлет **New-AzureRmNetworkProfileContainerNicConfig** создает новый объект конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5495c-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="5495c-107">Этот объект определяет характеристики сетевого interfacs, созданного на родительском сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="5495c-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="5495c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5495c-108">EXAMPLES</span></span>

### <span data-ttu-id="5495c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5495c-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="5495c-110">Первая команда создает пустую конфигурацию сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5495c-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="5495c-111">Вторая создает новый профиль сети, передающий ранее созданную конфигурацию сетевого интерфейса контейнера в качестве аргумента командлету New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="5495c-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="5495c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5495c-112">PARAMETERS</span></span>

### <span data-ttu-id="5495c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5495c-113">-DefaultProfile</span></span>
<span data-ttu-id="5495c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5495c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5495c-115">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="5495c-115">-IpConfiguration</span></span>
<span data-ttu-id="5495c-116">{{Fill описание конфигурация]}</span><span class="sxs-lookup"><span data-stu-id="5495c-116">{{Fill IpConfiguration Description}}</span></span>

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

### <span data-ttu-id="5495c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5495c-117">-Name</span></span>
<span data-ttu-id="5495c-118">Имя конфигурации сетевого интерфейса контейнера.</span><span class="sxs-lookup"><span data-stu-id="5495c-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="5495c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5495c-119">-Confirm</span></span>
<span data-ttu-id="5495c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5495c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5495c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5495c-121">-WhatIf</span></span>
<span data-ttu-id="5495c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5495c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5495c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5495c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5495c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5495c-124">CommonParameters</span></span>
<span data-ttu-id="5495c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5495c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5495c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5495c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5495c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5495c-127">INPUTS</span></span>

### <span data-ttu-id="5495c-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5495c-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5495c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5495c-129">OUTPUTS</span></span>

### <span data-ttu-id="5495c-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5495c-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5495c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5495c-131">NOTES</span></span>

## <span data-ttu-id="5495c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5495c-132">RELATED LINKS</span></span>
