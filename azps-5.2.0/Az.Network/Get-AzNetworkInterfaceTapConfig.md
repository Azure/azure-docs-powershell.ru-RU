---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395516"
---
# <span data-ttu-id="3e674-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3e674-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="3e674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e674-102">SYNOPSIS</span></span>
<span data-ttu-id="3e674-103">Получает ресурс конфигурации "Коснитесь".</span><span class="sxs-lookup"><span data-stu-id="3e674-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="3e674-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e674-104">SYNTAX</span></span>

### <span data-ttu-id="3e674-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e674-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e674-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e674-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e674-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e674-107">DESCRIPTION</span></span>
<span data-ttu-id="3e674-108">Командлет **Get-AzNetworkInterfaceTapConfig** получает конфигурацию Azure Tap для данной группы ресурсов, сетевого интерфейса и имени конфигурации tap или списка конфигураций tap в группе ресурсов и сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3e674-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="3e674-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e674-109">EXAMPLES</span></span>

### <span data-ttu-id="3e674-110">Пример 1. Получить все конфигурации касания для данного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="3e674-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="3e674-111">Эта команда получает добавленные конфигурации касания для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e674-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="3e674-112">Пример 2. Настройка касания</span><span class="sxs-lookup"><span data-stu-id="3e674-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="3e674-113">Эта команда получает определенную конфигурацию касания, добавленную для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e674-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="3e674-114">Пример 3. Настройка касания</span><span class="sxs-lookup"><span data-stu-id="3e674-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="3e674-115">Эта команда получает добавленные конфигурации касания для данного сетевого интерфейса с именем, которое начинается с "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="3e674-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="3e674-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e674-116">PARAMETERS</span></span>

### <span data-ttu-id="3e674-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e674-117">-DefaultProfile</span></span>
<span data-ttu-id="3e674-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e674-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e674-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3e674-119">-Name</span></span>
<span data-ttu-id="3e674-120">Имя конфигурации для конкретного касания.</span><span class="sxs-lookup"><span data-stu-id="3e674-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3e674-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3e674-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="3e674-122">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e674-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="3e674-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e674-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e674-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e674-124">The resource group name.</span></span>

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

### <span data-ttu-id="3e674-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e674-125">-ResourceId</span></span>
<span data-ttu-id="3e674-126">ResourceId ресурса TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e674-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="3e674-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e674-127">-Confirm</span></span>
<span data-ttu-id="3e674-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e674-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e674-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e674-129">-WhatIf</span></span>
<span data-ttu-id="3e674-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e674-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e674-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3e674-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e674-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e674-132">CommonParameters</span></span>
<span data-ttu-id="3e674-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e674-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e674-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e674-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e674-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e674-135">INPUTS</span></span>

### <span data-ttu-id="3e674-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3e674-136">System.String</span></span>

## <span data-ttu-id="3e674-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e674-137">OUTPUTS</span></span>

### <span data-ttu-id="3e674-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e674-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="3e674-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e674-139">NOTES</span></span>

## <span data-ttu-id="3e674-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e674-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e674-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3e674-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="3e674-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3e674-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="3e674-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3e674-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
