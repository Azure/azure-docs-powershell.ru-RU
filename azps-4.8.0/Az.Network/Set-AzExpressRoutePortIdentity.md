---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244785"
---
# <span data-ttu-id="addd7-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="addd7-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="addd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="addd7-102">SYNOPSIS</span></span>
<span data-ttu-id="addd7-103">Обновляет удостоверение, назначенное ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="addd7-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="addd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="addd7-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="addd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="addd7-105">DESCRIPTION</span></span>
<span data-ttu-id="addd7-106">Командлет **Set-AzExpressRoutePortIdentity** обновляет локальный объект Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="addd7-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="addd7-107">С помощью **Set-AzExpressRoutePort** назначьте ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="addd7-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="addd7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="addd7-108">EXAMPLES</span></span>

### <span data-ttu-id="addd7-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="addd7-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="addd7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="addd7-110">PARAMETERS</span></span>

### <span data-ttu-id="addd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addd7-111">-DefaultProfile</span></span>
<span data-ttu-id="addd7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="addd7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="addd7-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="addd7-113">-ExpressRoutePort</span></span>
<span data-ttu-id="addd7-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="addd7-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="addd7-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="addd7-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="addd7-116">ResourceId для пользователя, которому назначена идентификация, для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="addd7-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="addd7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="addd7-117">-Confirm</span></span>
<span data-ttu-id="addd7-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="addd7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="addd7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="addd7-119">-WhatIf</span></span>
<span data-ttu-id="addd7-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="addd7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="addd7-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="addd7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="addd7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addd7-122">CommonParameters</span></span>
<span data-ttu-id="addd7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="addd7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addd7-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addd7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addd7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="addd7-125">INPUTS</span></span>

### <span data-ttu-id="addd7-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="addd7-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="addd7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="addd7-127">System.String</span></span>

## <span data-ttu-id="addd7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="addd7-128">OUTPUTS</span></span>

### <span data-ttu-id="addd7-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="addd7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="addd7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="addd7-130">NOTES</span></span>

## <span data-ttu-id="addd7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="addd7-131">RELATED LINKS</span></span>
[<span data-ttu-id="addd7-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="addd7-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="addd7-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="addd7-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="addd7-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="addd7-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
