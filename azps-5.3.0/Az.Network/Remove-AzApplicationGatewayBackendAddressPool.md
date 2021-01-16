---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421540"
---
# <span data-ttu-id="9fef0-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9fef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fef0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fef0-103">Удаляет пул конечных адресов из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9fef0-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="9fef0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9fef0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fef0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fef0-105">DESCRIPTION</span></span>
<span data-ttu-id="9fef0-106">С **помощью cmdlet Remove-AzApplicationGatewayBackendAddressPool** можно удалить пул адресов с задней стороны из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9fef0-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="9fef0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9fef0-107">EXAMPLES</span></span>

### <span data-ttu-id="9fef0-108">Пример 1. Удаление пула адресов с конечными адресами из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="9fef0-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="9fef0-109">Первая команда получает шлюз приложения ApplicationGateway01, относящееся к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="9fef0-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="9fef0-110">Вторая команда удаляет из шлюза приложения пул адресов с именем BackEndPool02.</span><span class="sxs-lookup"><span data-stu-id="9fef0-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="9fef0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fef0-111">PARAMETERS</span></span>

### <span data-ttu-id="9fef0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fef0-112">-ApplicationGateway</span></span>
<span data-ttu-id="9fef0-113">Указывает шлюз приложения, из которого этот cmdlet удаляет пул конечных адресов.</span><span class="sxs-lookup"><span data-stu-id="9fef0-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fef0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fef0-114">-DefaultProfile</span></span>
<span data-ttu-id="9fef0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fef0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fef0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9fef0-116">-Name</span></span>
<span data-ttu-id="9fef0-117">Имя пула адресов, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fef0-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fef0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fef0-118">-Confirm</span></span>
<span data-ttu-id="9fef0-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fef0-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fef0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fef0-120">-WhatIf</span></span>
<span data-ttu-id="9fef0-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fef0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fef0-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9fef0-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fef0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fef0-123">CommonParameters</span></span>
<span data-ttu-id="9fef0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fef0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fef0-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fef0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fef0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fef0-126">INPUTS</span></span>

### <span data-ttu-id="9fef0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fef0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9fef0-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9fef0-128">OUTPUTS</span></span>

### <span data-ttu-id="9fef0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9fef0-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9fef0-130">NOTES</span></span>

## <span data-ttu-id="9fef0-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fef0-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fef0-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fef0-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fef0-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9fef0-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9fef0-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


