---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 8019cb905859e6e46fbf5ae90b90d72b170c631e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568992"
---
# <span data-ttu-id="0f621-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0f621-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="0f621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f621-102">SYNOPSIS</span></span>
<span data-ttu-id="0f621-103">Удаляет политику SSL из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="0f621-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f621-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f621-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f621-105">DESCRIPTION</span></span>
<span data-ttu-id="0f621-106">Командлет Remove-AzureRmApplicationGatewaySslPolicy удаляет политику SSL из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="0f621-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="0f621-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f621-107">EXAMPLES</span></span>

### <span data-ttu-id="0f621-108">Пример 1: Удаление политики SSL из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0f621-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="0f621-109">Эта команда удаляет политику SSL с шлюза приложений с именем ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="0f621-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="0f621-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f621-110">PARAMETERS</span></span>

### <span data-ttu-id="0f621-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f621-111">-ApplicationGateway</span></span>
<span data-ttu-id="0f621-112">Указывает шлюз приложений, с которого этот командлет удаляет политику SSL.</span><span class="sxs-lookup"><span data-stu-id="0f621-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f621-113">-DefaultProfile</span></span>
<span data-ttu-id="0f621-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f621-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f621-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0f621-115">-Force</span></span>
<span data-ttu-id="0f621-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0f621-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0f621-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f621-117">-Confirm</span></span>
<span data-ttu-id="0f621-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f621-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f621-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f621-119">-WhatIf</span></span>
<span data-ttu-id="0f621-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f621-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f621-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f621-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f621-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f621-122">CommonParameters</span></span>
<span data-ttu-id="0f621-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f621-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f621-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f621-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f621-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f621-125">INPUTS</span></span>

### <span data-ttu-id="0f621-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0f621-126">System.String</span></span>

## <span data-ttu-id="0f621-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f621-127">OUTPUTS</span></span>

### <span data-ttu-id="0f621-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f621-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0f621-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f621-129">NOTES</span></span>
<span data-ttu-id="0f621-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="0f621-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0f621-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f621-131">RELATED LINKS</span></span>

[<span data-ttu-id="0f621-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0f621-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0f621-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0f621-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0f621-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0f621-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

