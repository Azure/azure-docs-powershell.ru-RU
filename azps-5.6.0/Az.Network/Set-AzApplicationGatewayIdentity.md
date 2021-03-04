---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2f100d29b2251d71b170c7833f77ab2f23f90209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955768"
---
# <span data-ttu-id="a82aa-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a82aa-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a82aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a82aa-103">Обновляет удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a82aa-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a82aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a82aa-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a82aa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a82aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a82aa-106">**Cmdlet Set-AzApplicationGatewayIdentity** обновляет удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a82aa-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="a82aa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a82aa-107">EXAMPLES</span></span>

### <span data-ttu-id="a82aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a82aa-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a82aa-109">В этом примере назначается удостоверение пользователя существующему шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a82aa-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="a82aa-110">Примечание. У этого удостоверения должен быть доступ к ключам, на которые будут ссылаться сертификаты и секреты.</span><span class="sxs-lookup"><span data-stu-id="a82aa-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="a82aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a82aa-111">PARAMETERS</span></span>

### <span data-ttu-id="a82aa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a82aa-112">-ApplicationGateway</span></span>
<span data-ttu-id="a82aa-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a82aa-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a82aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82aa-114">-DefaultProfile</span></span>
<span data-ttu-id="a82aa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a82aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82aa-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a82aa-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a82aa-117">ResourceId идентификатора пользователя, назначенного шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a82aa-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="a82aa-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a82aa-118">-Confirm</span></span>
<span data-ttu-id="a82aa-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a82aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82aa-120">-WhatIf</span></span>
<span data-ttu-id="a82aa-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a82aa-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82aa-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a82aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a82aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82aa-123">CommonParameters</span></span>
<span data-ttu-id="a82aa-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82aa-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a82aa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82aa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a82aa-126">INPUTS</span></span>

### <span data-ttu-id="a82aa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a82aa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a82aa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a82aa-128">System.String</span></span>

## <span data-ttu-id="a82aa-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a82aa-129">OUTPUTS</span></span>

### <span data-ttu-id="a82aa-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a82aa-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a82aa-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a82aa-131">NOTES</span></span>

## <span data-ttu-id="a82aa-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a82aa-132">RELATED LINKS</span></span>
