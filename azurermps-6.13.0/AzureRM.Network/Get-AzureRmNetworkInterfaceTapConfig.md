---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735093"
---
# <span data-ttu-id="ba1c9-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ba1c9-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ba1c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1c9-103">Возвращает ресурс конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba1c9-104">SYNTAX</span></span>

### <span data-ttu-id="ba1c9-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba1c9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba1c9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba1c9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba1c9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba1c9-107">DESCRIPTION</span></span>
<span data-ttu-id="ba1c9-108">Командлет **Get-AzureRmNetworkInterfaceTapConfig** получает конфигурацию Azure TAP для указанной группы ресурсов, сетевого интерфейса и нажмите имя конфигурации или список вариантов TAP в группе ресурсов и сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="ba1c9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba1c9-109">EXAMPLES</span></span>

### <span data-ttu-id="ba1c9-110">Пример 1: получение всех конфигураций TAP для определенного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="ba1c9-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="ba1c9-111">Эта команда получает конфигурации для TAP, добавленные для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="ba1c9-112">Пример 2: получение конфигурации в указанном фрагменте TAP</span><span class="sxs-lookup"><span data-stu-id="ba1c9-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="ba1c9-113">Эта команда получает специальную конфигурацию TAP, добавленную для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="ba1c9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba1c9-114">PARAMETERS</span></span>

### <span data-ttu-id="ba1c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1c9-115">-DefaultProfile</span></span>
<span data-ttu-id="ba1c9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba1c9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba1c9-117">-Name</span></span>
<span data-ttu-id="ba1c9-118">Имя конкретной конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c9-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ba1c9-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="ba1c9-120">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba1c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba1c9-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba1c9-123">-ResourceId</span></span>
<span data-ttu-id="ba1c9-124">ResourceId для ресурса TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba1c9-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba1c9-125">-Confirm</span></span>
<span data-ttu-id="ba1c9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba1c9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba1c9-127">-WhatIf</span></span>
<span data-ttu-id="ba1c9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba1c9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba1c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1c9-130">CommonParameters</span></span>
<span data-ttu-id="ba1c9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1c9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1c9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1c9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba1c9-133">INPUTS</span></span>

### <span data-ttu-id="ba1c9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba1c9-134">System.String</span></span>

## <span data-ttu-id="ba1c9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba1c9-135">OUTPUTS</span></span>

### <span data-ttu-id="ba1c9-136">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba1c9-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="ba1c9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba1c9-137">NOTES</span></span>

## <span data-ttu-id="ba1c9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba1c9-138">RELATED LINKS</span></span>
