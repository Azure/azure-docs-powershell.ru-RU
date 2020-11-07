---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 3bb2df6349c734e9802183c13eb39ae8ceafc50b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902225"
---
# <span data-ttu-id="f2752-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f2752-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f2752-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2752-102">SYNOPSIS</span></span>
<span data-ttu-id="f2752-103">Создает объект Identity для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f2752-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="f2752-104">Это будет содержать ссылку на удостоверение пользователя, которому она назначена.</span><span class="sxs-lookup"><span data-stu-id="f2752-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="f2752-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2752-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2752-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2752-106">DESCRIPTION</span></span>
<span data-ttu-id="f2752-107">Командлет **New-AzApplicationGatewayIdentity** создает объект удостоверения для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f2752-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="f2752-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2752-108">EXAMPLES</span></span>

### <span data-ttu-id="f2752-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2752-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="f2752-110">В этом примере мы создадим удостоверение пользователя и сослаться на него в объекте Identity, используемом с шлюзом приложений.</span><span class="sxs-lookup"><span data-stu-id="f2752-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="f2752-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2752-111">PARAMETERS</span></span>

### <span data-ttu-id="f2752-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2752-112">-DefaultProfile</span></span>
<span data-ttu-id="f2752-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2752-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2752-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f2752-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f2752-115">ResourceId для пользователя, которому назначена идентификация, назначаемая шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="f2752-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="f2752-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2752-116">-Confirm</span></span>
<span data-ttu-id="f2752-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2752-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2752-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2752-118">-WhatIf</span></span>
<span data-ttu-id="f2752-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2752-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2752-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2752-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2752-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2752-121">CommonParameters</span></span>
<span data-ttu-id="f2752-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2752-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2752-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2752-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2752-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2752-124">INPUTS</span></span>

### <span data-ttu-id="f2752-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f2752-125">System.String</span></span>

## <span data-ttu-id="f2752-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2752-126">OUTPUTS</span></span>

### <span data-ttu-id="f2752-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f2752-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f2752-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2752-128">NOTES</span></span>

## <span data-ttu-id="f2752-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2752-129">RELATED LINKS</span></span>
