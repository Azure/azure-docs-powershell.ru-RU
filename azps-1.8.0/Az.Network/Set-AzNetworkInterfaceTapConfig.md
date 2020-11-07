---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2a860c295106755c326624a0bb37de22976d072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729992"
---
# <span data-ttu-id="56210-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="56210-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56210-102">SYNOPSIS</span></span>
<span data-ttu-id="56210-103">Обновляет конфигурацию TAP для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="56210-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="56210-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56210-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56210-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56210-105">DESCRIPTION</span></span>
<span data-ttu-id="56210-106">**Set-AzNetworkInterfaceTapConfig** обновляет конфигурацию TAP для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="56210-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="56210-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56210-107">EXAMPLES</span></span>

### <span data-ttu-id="56210-108">Пример 1: Установка TapConfiguration с обновленным именем TapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="56210-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56210-109">PARAMETERS</span></span>

### <span data-ttu-id="56210-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56210-110">-AsJob</span></span>
<span data-ttu-id="56210-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56210-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56210-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56210-112">-DefaultProfile</span></span>
<span data-ttu-id="56210-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56210-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56210-114">-Force</span><span class="sxs-lookup"><span data-stu-id="56210-114">-Force</span></span>
<span data-ttu-id="56210-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="56210-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56210-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="56210-117">NetworkInterface TAP configurtion</span><span class="sxs-lookup"><span data-stu-id="56210-117">The NetworkInterface Tap configurtion</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56210-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56210-118">-Confirm</span></span>
<span data-ttu-id="56210-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56210-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56210-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56210-120">-WhatIf</span></span>
<span data-ttu-id="56210-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56210-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56210-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56210-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56210-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56210-123">CommonParameters</span></span>
<span data-ttu-id="56210-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56210-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56210-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56210-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56210-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56210-126">INPUTS</span></span>

### <span data-ttu-id="56210-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="56210-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="56210-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56210-128">OUTPUTS</span></span>

### <span data-ttu-id="56210-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56210-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="56210-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="56210-130">NOTES</span></span>

## <span data-ttu-id="56210-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56210-131">RELATED LINKS</span></span>

[<span data-ttu-id="56210-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="56210-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="56210-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56210-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
