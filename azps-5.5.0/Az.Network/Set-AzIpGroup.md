---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223569"
---
# <span data-ttu-id="d9b4c-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d9b4c-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="d9b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b4c-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="d9b4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9b4c-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9b4c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b4c-106">С **его использованием** обновляется ipGroup в Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="d9b4c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b4c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9b4c-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="d9b4c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9b4c-109">PARAMETERS</span></span>

### <span data-ttu-id="d9b4c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9b4c-110">-AsJob</span></span>
<span data-ttu-id="d9b4c-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d9b4c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9b4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b4c-112">-DefaultProfile</span></span>
<span data-ttu-id="d9b4c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b4c-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="d9b4c-114">-IpGroup</span></span>
<span data-ttu-id="d9b4c-115">The IpGroup</span><span class="sxs-lookup"><span data-stu-id="d9b4c-115">The IpGroup</span></span>

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

### <span data-ttu-id="d9b4c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b4c-116">-Confirm</span></span>
<span data-ttu-id="d9b4c-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b4c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b4c-118">-WhatIf</span></span>
<span data-ttu-id="d9b4c-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b4c-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b4c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b4c-121">CommonParameters</span></span>
<span data-ttu-id="d9b4c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b4c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b4c-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9b4c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b4c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9b4c-124">INPUTS</span></span>

### <span data-ttu-id="d9b4c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d9b4c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d9b4c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9b4c-126">OUTPUTS</span></span>

### <span data-ttu-id="d9b4c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d9b4c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d9b4c-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9b4c-128">NOTES</span></span>

## <span data-ttu-id="d9b4c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9b4c-129">RELATED LINKS</span></span>
