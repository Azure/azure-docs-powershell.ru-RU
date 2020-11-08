---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243025"
---
# <span data-ttu-id="41d20-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="41d20-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="41d20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41d20-102">SYNOPSIS</span></span>
<span data-ttu-id="41d20-103">Создает объект Identity для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="41d20-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="41d20-104">Это будет содержать ссылку на удостоверение пользователя, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="41d20-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="41d20-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41d20-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d20-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41d20-106">DESCRIPTION</span></span>
<span data-ttu-id="41d20-107">Командлет **New-AzApplicationGatewayIdentity** создает объект удостоверения для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="41d20-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="41d20-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41d20-108">EXAMPLES</span></span>

### <span data-ttu-id="41d20-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41d20-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="41d20-110">В этом примере мы создадим удостоверение пользователя и сослаться на него в объекте Identity, используемом с шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="41d20-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="41d20-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41d20-111">PARAMETERS</span></span>

### <span data-ttu-id="41d20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d20-112">-DefaultProfile</span></span>
<span data-ttu-id="41d20-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41d20-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d20-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="41d20-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="41d20-115">ResourceId для пользователя, которому назначена идентификация, назначаемая шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="41d20-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="41d20-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d20-116">-Confirm</span></span>
<span data-ttu-id="41d20-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41d20-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d20-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d20-118">-WhatIf</span></span>
<span data-ttu-id="41d20-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41d20-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d20-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41d20-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d20-121">CommonParameters</span></span>
<span data-ttu-id="41d20-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41d20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d20-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d20-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d20-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41d20-124">INPUTS</span></span>

### <span data-ttu-id="41d20-125">System. String</span><span class="sxs-lookup"><span data-stu-id="41d20-125">System.String</span></span>

## <span data-ttu-id="41d20-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41d20-126">OUTPUTS</span></span>

### <span data-ttu-id="41d20-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="41d20-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="41d20-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="41d20-128">NOTES</span></span>

## <span data-ttu-id="41d20-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41d20-129">RELATED LINKS</span></span>