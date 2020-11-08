---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079475"
---
# <span data-ttu-id="7e7d5-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7e7d5-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7e7d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7d5-103">Создание Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="7e7d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e7d5-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e7d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="7e7d5-106">Командлет **New-AzExpressRoutePortIdentity** создает локальный объект Azure ExpressRoutePort Identity.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="7e7d5-107">С помощью **New-AzExpressRoutePort** или **Set-AzExpressRoutePort** назначьте его в Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="7e7d5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e7d5-108">EXAMPLES</span></span>

### <span data-ttu-id="7e7d5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e7d5-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="7e7d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e7d5-110">PARAMETERS</span></span>

### <span data-ttu-id="7e7d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7d5-111">-DefaultProfile</span></span>
<span data-ttu-id="7e7d5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7d5-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7e7d5-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7e7d5-114">ResourceId для пользователя, которому назначена идентификация, для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7e7d5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e7d5-115">-Confirm</span></span>
<span data-ttu-id="7e7d5-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7d5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7d5-117">-WhatIf</span></span>
<span data-ttu-id="7e7d5-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e7d5-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7d5-120">CommonParameters</span></span>
<span data-ttu-id="7e7d5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7d5-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e7d5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7d5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e7d5-123">INPUTS</span></span>

### <span data-ttu-id="7e7d5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7e7d5-124">System.String</span></span>

## <span data-ttu-id="7e7d5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e7d5-125">OUTPUTS</span></span>

### <span data-ttu-id="7e7d5-126">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7e7d5-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7e7d5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e7d5-127">NOTES</span></span>

## <span data-ttu-id="7e7d5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e7d5-128">RELATED LINKS</span></span>
[<span data-ttu-id="7e7d5-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7e7d5-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7e7d5-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7e7d5-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7e7d5-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7e7d5-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)