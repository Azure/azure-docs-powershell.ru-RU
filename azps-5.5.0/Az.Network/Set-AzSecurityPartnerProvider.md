---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240565"
---
# <span data-ttu-id="3924c-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3924c-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3924c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3924c-102">SYNOPSIS</span></span>
<span data-ttu-id="3924c-103">Сохранение измененного azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="3924c-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3924c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3924c-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3924c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3924c-105">DESCRIPTION</span></span>
<span data-ttu-id="3924c-106">**Cmdlet Set-AzSecurityPartnerProvider** обновляет Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="3924c-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3924c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3924c-107">EXAMPLES</span></span>

### <span data-ttu-id="3924c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3924c-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="3924c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3924c-109">PARAMETERS</span></span>

### <span data-ttu-id="3924c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3924c-110">-AsJob</span></span>
<span data-ttu-id="3924c-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3924c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3924c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3924c-112">-DefaultProfile</span></span>
<span data-ttu-id="3924c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3924c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3924c-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3924c-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="3924c-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3924c-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="3924c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3924c-116">-Confirm</span></span>
<span data-ttu-id="3924c-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3924c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3924c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3924c-118">-WhatIf</span></span>
<span data-ttu-id="3924c-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3924c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3924c-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3924c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3924c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3924c-121">CommonParameters</span></span>
<span data-ttu-id="3924c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3924c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3924c-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3924c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3924c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3924c-124">INPUTS</span></span>

### <span data-ttu-id="3924c-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3924c-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3924c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3924c-126">OUTPUTS</span></span>

### <span data-ttu-id="3924c-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3924c-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3924c-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3924c-128">NOTES</span></span>

## <span data-ttu-id="3924c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3924c-129">RELATED LINKS</span></span>
