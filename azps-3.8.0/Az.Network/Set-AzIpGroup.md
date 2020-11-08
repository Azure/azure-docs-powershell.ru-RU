---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066978"
---
# <span data-ttu-id="a4b7f-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="a4b7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b7f-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="a4b7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4b7f-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b7f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b7f-106">Командлет **Set-AzIpGroup** обновляет Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="a4b7f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b7f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4b7f-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="a4b7f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4b7f-109">PARAMETERS</span></span>

### <span data-ttu-id="a4b7f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4b7f-110">-AsJob</span></span>
<span data-ttu-id="a4b7f-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a4b7f-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b7f-112">-DefaultProfile</span></span>
<span data-ttu-id="a4b7f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b7f-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-114">-IpGroup</span></span>
<span data-ttu-id="a4b7f-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b7f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4b7f-116">-Confirm</span></span>
<span data-ttu-id="a4b7f-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b7f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b7f-118">-WhatIf</span></span>
<span data-ttu-id="a4b7f-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b7f-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b7f-121">CommonParameters</span></span>
<span data-ttu-id="a4b7f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4b7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b7f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b7f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b7f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4b7f-124">INPUTS</span></span>

### <span data-ttu-id="a4b7f-125">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a4b7f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b7f-126">OUTPUTS</span></span>

### <span data-ttu-id="a4b7f-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a4b7f-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a4b7f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4b7f-128">NOTES</span></span>

## <span data-ttu-id="a4b7f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4b7f-129">RELATED LINKS</span></span>
