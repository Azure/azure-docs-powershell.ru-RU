---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248513"
---
# <span data-ttu-id="c4fa2-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c4fa2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fa2-103">Обновляет конфигурацию TAP для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="c4fa2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4fa2-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fa2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="c4fa2-106">**Set-AzNetworkInterfaceTapConfig** обновляет конфигурацию TAP для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="c4fa2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="c4fa2-108">Пример 1: Установка TapConfiguration с обновленным именем TapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="c4fa2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4fa2-109">PARAMETERS</span></span>

### <span data-ttu-id="c4fa2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4fa2-110">-AsJob</span></span>
<span data-ttu-id="c4fa2-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c4fa2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4fa2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fa2-112">-DefaultProfile</span></span>
<span data-ttu-id="c4fa2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fa2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c4fa2-114">-Force</span></span>
<span data-ttu-id="c4fa2-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4fa2-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="c4fa2-117">Настройка NetworkInterface TAP</span><span class="sxs-lookup"><span data-stu-id="c4fa2-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="c4fa2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4fa2-118">-Confirm</span></span>
<span data-ttu-id="c4fa2-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4fa2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fa2-120">-WhatIf</span></span>
<span data-ttu-id="c4fa2-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4fa2-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4fa2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fa2-123">CommonParameters</span></span>
<span data-ttu-id="c4fa2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4fa2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fa2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fa2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fa2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4fa2-126">INPUTS</span></span>

### <span data-ttu-id="c4fa2-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4fa2-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c4fa2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4fa2-128">OUTPUTS</span></span>

### <span data-ttu-id="c4fa2-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c4fa2-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c4fa2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4fa2-130">NOTES</span></span>

## <span data-ttu-id="c4fa2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4fa2-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4fa2-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c4fa2-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c4fa2-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4fa2-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
