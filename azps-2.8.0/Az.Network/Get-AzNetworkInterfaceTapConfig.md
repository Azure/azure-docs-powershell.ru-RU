---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902902"
---
# <span data-ttu-id="2b365-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2b365-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="2b365-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b365-102">SYNOPSIS</span></span>
<span data-ttu-id="2b365-103">Возвращает ресурс конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="2b365-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="2b365-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b365-104">SYNTAX</span></span>

### <span data-ttu-id="2b365-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b365-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b365-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b365-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b365-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b365-107">DESCRIPTION</span></span>
<span data-ttu-id="2b365-108">Командлет **Get-AzNetworkInterfaceTapConfig** получает конфигурацию Azure TAP для указанной группы ресурсов, сетевого интерфейса и нажмите имя конфигурации или список вариантов TAP в группе ресурсов и сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="2b365-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="2b365-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b365-109">EXAMPLES</span></span>

### <span data-ttu-id="2b365-110">Пример 1: получение всех конфигураций TAP для определенного сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b365-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="2b365-111">Эта команда получает конфигурации для TAP, добавленные для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b365-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="2b365-112">Пример 2: получение конфигурации в указанном фрагменте TAP</span><span class="sxs-lookup"><span data-stu-id="2b365-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="2b365-113">Эта команда получает специальную конфигурацию TAP, добавленную для данного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b365-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="2b365-114">Пример 3: получение конфигурации в указанном фрагменте TAP</span><span class="sxs-lookup"><span data-stu-id="2b365-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="2b365-115">Эта команда получает конфигурации для TAP, добавленные для указанного сетевого интерфейса с именем, начинающимся с "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="2b365-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="2b365-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b365-116">PARAMETERS</span></span>

### <span data-ttu-id="2b365-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b365-117">-DefaultProfile</span></span>
<span data-ttu-id="2b365-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b365-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b365-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b365-119">-Name</span></span>
<span data-ttu-id="2b365-120">Имя конкретной конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="2b365-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="2b365-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2b365-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="2b365-122">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b365-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="2b365-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b365-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b365-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b365-124">The resource group name.</span></span>

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

### <span data-ttu-id="2b365-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b365-125">-ResourceId</span></span>
<span data-ttu-id="2b365-126">ResourceId для ресурса TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b365-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="2b365-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b365-127">-Confirm</span></span>
<span data-ttu-id="2b365-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b365-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b365-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b365-129">-WhatIf</span></span>
<span data-ttu-id="2b365-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b365-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b365-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b365-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b365-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b365-132">CommonParameters</span></span>
<span data-ttu-id="2b365-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b365-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b365-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b365-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b365-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b365-135">INPUTS</span></span>

### <span data-ttu-id="2b365-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2b365-136">System.String</span></span>

## <span data-ttu-id="2b365-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b365-137">OUTPUTS</span></span>

### <span data-ttu-id="2b365-138">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b365-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="2b365-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b365-139">NOTES</span></span>

## <span data-ttu-id="2b365-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b365-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b365-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2b365-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2b365-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2b365-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2b365-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2b365-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
