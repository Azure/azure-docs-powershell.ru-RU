---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 5ad5b27397c0659d45fba1857a021efaa49db013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901833"
---
# <span data-ttu-id="a690f-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a690f-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a690f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a690f-102">SYNOPSIS</span></span>
<span data-ttu-id="a690f-103">Обновляет удостоверение, назначенное для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a690f-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a690f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a690f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a690f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a690f-105">DESCRIPTION</span></span>
<span data-ttu-id="a690f-106">Командлет **Set-AzApplicationGatewayIdentity** обновляет удостоверение, назначенное для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a690f-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="a690f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a690f-107">EXAMPLES</span></span>

### <span data-ttu-id="a690f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a690f-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a690f-109">В этом примере мы назначаем удостоверению пользователя существующему шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a690f-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="a690f-110">Примечание. Эта идентификация должна иметь доступ к keyvault, из которого будут ссылаться сертификаты и секреты.</span><span class="sxs-lookup"><span data-stu-id="a690f-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="a690f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a690f-111">PARAMETERS</span></span>

### <span data-ttu-id="a690f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a690f-112">-ApplicationGateway</span></span>
<span data-ttu-id="a690f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a690f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a690f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a690f-114">-DefaultProfile</span></span>
<span data-ttu-id="a690f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a690f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a690f-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a690f-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a690f-117">ResourceId для пользователя, которому назначена идентификация, назначаемая шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a690f-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a690f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a690f-118">-Confirm</span></span>
<span data-ttu-id="a690f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a690f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a690f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a690f-120">-WhatIf</span></span>
<span data-ttu-id="a690f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a690f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a690f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a690f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a690f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a690f-123">CommonParameters</span></span>
<span data-ttu-id="a690f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a690f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a690f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a690f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a690f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a690f-126">INPUTS</span></span>

### <span data-ttu-id="a690f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a690f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a690f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a690f-128">System.String</span></span>

## <span data-ttu-id="a690f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a690f-129">OUTPUTS</span></span>

### <span data-ttu-id="a690f-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a690f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a690f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a690f-131">NOTES</span></span>

## <span data-ttu-id="a690f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a690f-132">RELATED LINKS</span></span>
