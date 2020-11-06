---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556584"
---
# <span data-ttu-id="711ce-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="711ce-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="711ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="711ce-102">SYNOPSIS</span></span>
<span data-ttu-id="711ce-103">Задает состояние цели для настройки TAP</span><span class="sxs-lookup"><span data-stu-id="711ce-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="711ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="711ce-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="711ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="711ce-105">DESCRIPTION</span></span>
<span data-ttu-id="711ce-106">**Set-AzureRmNetworkInterfaceTapConfig** задает состояние цели для сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="711ce-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="711ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="711ce-107">EXAMPLES</span></span>

### <span data-ttu-id="711ce-108">Пример 1: Установка TapConfiguration с обновленным именем TapConfig</span><span class="sxs-lookup"><span data-stu-id="711ce-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="711ce-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="711ce-109">PARAMETERS</span></span>

### <span data-ttu-id="711ce-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="711ce-110">-AsJob</span></span>
<span data-ttu-id="711ce-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="711ce-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="711ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711ce-112">-DefaultProfile</span></span>
<span data-ttu-id="711ce-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="711ce-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="711ce-114">-Force</span><span class="sxs-lookup"><span data-stu-id="711ce-114">-Force</span></span>
<span data-ttu-id="711ce-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="711ce-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="711ce-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="711ce-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="711ce-117">NetworkInterface TAP configurtion</span><span class="sxs-lookup"><span data-stu-id="711ce-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="711ce-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="711ce-118">-Confirm</span></span>
<span data-ttu-id="711ce-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="711ce-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711ce-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711ce-120">-WhatIf</span></span>
<span data-ttu-id="711ce-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="711ce-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711ce-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="711ce-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ce-123">CommonParameters</span></span>
<span data-ttu-id="711ce-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="711ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ce-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="711ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ce-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="711ce-126">INPUTS</span></span>

### <span data-ttu-id="711ce-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="711ce-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="711ce-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="711ce-128">OUTPUTS</span></span>

### <span data-ttu-id="711ce-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="711ce-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="711ce-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="711ce-130">NOTES</span></span>

## <span data-ttu-id="711ce-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="711ce-131">RELATED LINKS</span></span>
