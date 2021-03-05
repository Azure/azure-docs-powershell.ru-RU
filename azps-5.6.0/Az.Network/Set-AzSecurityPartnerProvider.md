---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010307"
---
# <span data-ttu-id="7f827-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="7f827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f827-102">SYNOPSIS</span></span>
<span data-ttu-id="7f827-103">Сохранение измененного azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="7f827-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="7f827-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f827-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f827-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f827-105">DESCRIPTION</span></span>
<span data-ttu-id="7f827-106">**Cmdlet Set-AzSecurityPartnerProvider** обновляет Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="7f827-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f827-107">EXAMPLES</span></span>

### <span data-ttu-id="7f827-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f827-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="7f827-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f827-109">PARAMETERS</span></span>

### <span data-ttu-id="7f827-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f827-110">-AsJob</span></span>
<span data-ttu-id="7f827-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7f827-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f827-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f827-112">-DefaultProfile</span></span>
<span data-ttu-id="7f827-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f827-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f827-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="7f827-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f827-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f827-116">-Confirm</span></span>
<span data-ttu-id="7f827-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f827-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f827-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f827-118">-WhatIf</span></span>
<span data-ttu-id="7f827-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f827-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f827-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f827-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f827-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f827-121">CommonParameters</span></span>
<span data-ttu-id="7f827-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f827-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f827-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f827-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f827-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f827-124">INPUTS</span></span>

### <span data-ttu-id="7f827-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="7f827-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f827-126">OUTPUTS</span></span>

### <span data-ttu-id="7f827-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7f827-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="7f827-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f827-128">NOTES</span></span>

## <span data-ttu-id="7f827-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f827-129">RELATED LINKS</span></span>
