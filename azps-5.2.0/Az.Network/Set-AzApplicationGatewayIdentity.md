---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416391"
---
# <span data-ttu-id="914cc-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="914cc-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="914cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="914cc-102">SYNOPSIS</span></span>
<span data-ttu-id="914cc-103">Обновляет удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="914cc-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="914cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="914cc-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="914cc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="914cc-105">DESCRIPTION</span></span>
<span data-ttu-id="914cc-106">**Cmdlet Set-AzApplicationGatewayIdentity** обновляет удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="914cc-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="914cc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="914cc-107">EXAMPLES</span></span>

### <span data-ttu-id="914cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="914cc-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="914cc-109">В этом примере мы назначаем удостоверение пользователя существующему шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="914cc-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="914cc-110">Примечание. У этого удостоверения должен быть доступ к ключам, на которые будут ссылаться сертификаты и секреты.</span><span class="sxs-lookup"><span data-stu-id="914cc-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="914cc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="914cc-111">PARAMETERS</span></span>

### <span data-ttu-id="914cc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914cc-112">-ApplicationGateway</span></span>
<span data-ttu-id="914cc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914cc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="914cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914cc-114">-DefaultProfile</span></span>
<span data-ttu-id="914cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="914cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="914cc-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="914cc-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="914cc-117">ResourceId идентификатора пользователя, назначенного шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="914cc-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="914cc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="914cc-118">-Confirm</span></span>
<span data-ttu-id="914cc-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="914cc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="914cc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="914cc-120">-WhatIf</span></span>
<span data-ttu-id="914cc-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="914cc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="914cc-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="914cc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="914cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914cc-123">CommonParameters</span></span>
<span data-ttu-id="914cc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914cc-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="914cc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914cc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="914cc-126">INPUTS</span></span>

### <span data-ttu-id="914cc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914cc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="914cc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="914cc-128">System.String</span></span>

## <span data-ttu-id="914cc-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="914cc-129">OUTPUTS</span></span>

### <span data-ttu-id="914cc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914cc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="914cc-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="914cc-131">NOTES</span></span>

## <span data-ttu-id="914cc-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="914cc-132">RELATED LINKS</span></span>
