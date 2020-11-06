---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556580"
---
# <span data-ttu-id="4ad11-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ad11-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="4ad11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ad11-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad11-103">Задает состояние цели для существующего профиля сети</span><span class="sxs-lookup"><span data-stu-id="4ad11-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ad11-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad11-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ad11-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad11-106">Командлет **Set-AzureRmPublicIpPrefix** задает состояние цели для профиля сети.</span><span class="sxs-lookup"><span data-stu-id="4ad11-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="4ad11-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ad11-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad11-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ad11-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="4ad11-109">Первая команда получает существующий профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ad11-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="4ad11-110">Вторая команда обновляет тег, а третья добавляет конфигурацию сетевого интерфейса в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="4ad11-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="4ad11-111">Четвертая команда обновляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ad11-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="4ad11-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ad11-112">PARAMETERS</span></span>

### <span data-ttu-id="4ad11-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad11-113">-AsJob</span></span>
<span data-ttu-id="4ad11-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ad11-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ad11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad11-115">-DefaultProfile</span></span>
<span data-ttu-id="4ad11-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad11-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad11-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ad11-117">-NetworkProfile</span></span>
<span data-ttu-id="4ad11-118">Профиль сети</span><span class="sxs-lookup"><span data-stu-id="4ad11-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad11-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ad11-119">-Confirm</span></span>
<span data-ttu-id="4ad11-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ad11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad11-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad11-121">-WhatIf</span></span>
<span data-ttu-id="4ad11-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ad11-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad11-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ad11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad11-124">CommonParameters</span></span>
<span data-ttu-id="4ad11-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ad11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad11-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad11-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ad11-127">INPUTS</span></span>

### <span data-ttu-id="4ad11-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ad11-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ad11-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ad11-129">OUTPUTS</span></span>

### <span data-ttu-id="4ad11-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ad11-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ad11-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ad11-131">NOTES</span></span>

## <span data-ttu-id="4ad11-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ad11-132">RELATED LINKS</span></span>
