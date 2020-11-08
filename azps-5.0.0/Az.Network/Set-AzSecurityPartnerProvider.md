---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247938"
---
# <span data-ttu-id="3fcda-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3fcda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fcda-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcda-103">Сохранение измененного SecurityPartnerProvider Azure.</span><span class="sxs-lookup"><span data-stu-id="3fcda-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3fcda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fcda-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fcda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fcda-105">DESCRIPTION</span></span>
<span data-ttu-id="3fcda-106">Командлет **Set-AzSecurityPartnerProvider** обновляет Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3fcda-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fcda-107">EXAMPLES</span></span>

### <span data-ttu-id="3fcda-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fcda-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="3fcda-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fcda-109">PARAMETERS</span></span>

### <span data-ttu-id="3fcda-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fcda-110">-AsJob</span></span>
<span data-ttu-id="3fcda-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3fcda-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fcda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcda-112">-DefaultProfile</span></span>
<span data-ttu-id="3fcda-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fcda-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fcda-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="3fcda-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="3fcda-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fcda-116">-Confirm</span></span>
<span data-ttu-id="3fcda-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fcda-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcda-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcda-118">-WhatIf</span></span>
<span data-ttu-id="3fcda-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fcda-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fcda-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fcda-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcda-121">CommonParameters</span></span>
<span data-ttu-id="3fcda-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fcda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcda-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fcda-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcda-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fcda-124">INPUTS</span></span>

### <span data-ttu-id="3fcda-125">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3fcda-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fcda-126">OUTPUTS</span></span>

### <span data-ttu-id="3fcda-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3fcda-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3fcda-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fcda-128">NOTES</span></span>

## <span data-ttu-id="3fcda-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fcda-129">RELATED LINKS</span></span>
