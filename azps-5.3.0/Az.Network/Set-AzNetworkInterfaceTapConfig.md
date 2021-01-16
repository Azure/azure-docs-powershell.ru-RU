---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519892"
---
# <span data-ttu-id="6538f-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="6538f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6538f-102">SYNOPSIS</span></span>
<span data-ttu-id="6538f-103">Обновляет конфигурацию касания для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6538f-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6538f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6538f-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6538f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6538f-105">DESCRIPTION</span></span>
<span data-ttu-id="6538f-106">**Set-AzNetworkInterfaceTapConfig** обновляет конфигурацию касания для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6538f-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="6538f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6538f-107">EXAMPLES</span></span>

### <span data-ttu-id="6538f-108">Пример 1. Настройка TapConfiguration с обновленным именем TapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="6538f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6538f-109">PARAMETERS</span></span>

### <span data-ttu-id="6538f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6538f-110">-AsJob</span></span>
<span data-ttu-id="6538f-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6538f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6538f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6538f-112">-DefaultProfile</span></span>
<span data-ttu-id="6538f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6538f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6538f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6538f-114">-Force</span></span>
<span data-ttu-id="6538f-115">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6538f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6538f-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="6538f-117">Конфигурация NetworkInterface Tap</span><span class="sxs-lookup"><span data-stu-id="6538f-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="6538f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6538f-118">-Confirm</span></span>
<span data-ttu-id="6538f-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6538f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6538f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6538f-120">-WhatIf</span></span>
<span data-ttu-id="6538f-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6538f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6538f-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6538f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6538f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6538f-123">CommonParameters</span></span>
<span data-ttu-id="6538f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6538f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6538f-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6538f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6538f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6538f-126">INPUTS</span></span>

### <span data-ttu-id="6538f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="6538f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="6538f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6538f-128">OUTPUTS</span></span>

### <span data-ttu-id="6538f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6538f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6538f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6538f-130">NOTES</span></span>

## <span data-ttu-id="6538f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6538f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6538f-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6538f-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="6538f-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6538f-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)