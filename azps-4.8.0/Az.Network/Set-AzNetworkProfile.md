---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234894"
---
# <span data-ttu-id="4ee4f-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="4ee4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ee4f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee4f-103">Обновляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-103">Updates a network profile.</span></span>

## <span data-ttu-id="4ee4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ee4f-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ee4f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee4f-106">Командлет **Set-AzPublicIpPrefix** обновляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="4ee4f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ee4f-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee4f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ee4f-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="4ee4f-109">Первая команда получает существующий профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="4ee4f-110">Вторая команда обновляет тег, а третья добавляет конфигурацию сетевого интерфейса в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="4ee4f-111">Четвертая команда обновляет профиль сети.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="4ee4f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ee4f-112">PARAMETERS</span></span>

### <span data-ttu-id="4ee4f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ee4f-113">-AsJob</span></span>
<span data-ttu-id="4ee4f-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ee4f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-115">-DefaultProfile</span></span>
<span data-ttu-id="4ee4f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee4f-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-117">-NetworkProfile</span></span>
<span data-ttu-id="4ee4f-118">Профиль сети</span><span class="sxs-lookup"><span data-stu-id="4ee4f-118">The network profile</span></span>

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

### <span data-ttu-id="4ee4f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ee4f-119">-Confirm</span></span>
<span data-ttu-id="4ee4f-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee4f-121">-WhatIf</span></span>
<span data-ttu-id="4ee4f-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee4f-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee4f-124">CommonParameters</span></span>
<span data-ttu-id="4ee4f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ee4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee4f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee4f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee4f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ee4f-127">INPUTS</span></span>

### <span data-ttu-id="4ee4f-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ee4f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ee4f-129">OUTPUTS</span></span>

### <span data-ttu-id="4ee4f-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ee4f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ee4f-131">NOTES</span></span>

## <span data-ttu-id="4ee4f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ee4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ee4f-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="4ee4f-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="4ee4f-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ee4f-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
