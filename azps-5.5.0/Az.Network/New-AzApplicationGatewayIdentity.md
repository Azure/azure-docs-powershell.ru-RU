---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236865"
---
# <span data-ttu-id="32f84-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="32f84-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="32f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f84-102">SYNOPSIS</span></span>
<span data-ttu-id="32f84-103">Создает объект удостоверения для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="32f84-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="32f84-104">При этом будет удержана ссылка на удостоверение пользователя, назначенное пользователю.</span><span class="sxs-lookup"><span data-stu-id="32f84-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="32f84-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32f84-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f84-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32f84-106">DESCRIPTION</span></span>
<span data-ttu-id="32f84-107">**Для создания объекта New-AzApplicationGatewayIdentity** создается объект удостоверения шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="32f84-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="32f84-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32f84-108">EXAMPLES</span></span>

### <span data-ttu-id="32f84-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32f84-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="32f84-110">В этом примере мы создадим удостоверение, назначенное пользователю, и будем ссылаться на него в объекте удостоверения, используемом со шлюзом приложения.</span><span class="sxs-lookup"><span data-stu-id="32f84-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="32f84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32f84-111">PARAMETERS</span></span>

### <span data-ttu-id="32f84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f84-112">-DefaultProfile</span></span>
<span data-ttu-id="32f84-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32f84-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32f84-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="32f84-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="32f84-115">ResourceId идентификатора пользователя, назначенного шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="32f84-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="32f84-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32f84-116">-Confirm</span></span>
<span data-ttu-id="32f84-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="32f84-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f84-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f84-118">-WhatIf</span></span>
<span data-ttu-id="32f84-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32f84-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f84-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32f84-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f84-121">CommonParameters</span></span>
<span data-ttu-id="32f84-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f84-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f84-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f84-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32f84-124">INPUTS</span></span>

### <span data-ttu-id="32f84-125">System.String</span><span class="sxs-lookup"><span data-stu-id="32f84-125">System.String</span></span>

## <span data-ttu-id="32f84-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32f84-126">OUTPUTS</span></span>

### <span data-ttu-id="32f84-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="32f84-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="32f84-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32f84-128">NOTES</span></span>

## <span data-ttu-id="32f84-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32f84-129">RELATED LINKS</span></span>
