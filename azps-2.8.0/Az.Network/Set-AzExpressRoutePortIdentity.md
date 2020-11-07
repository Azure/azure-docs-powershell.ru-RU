---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 330264eaaffd9d81da2ed8dbcc7c892477ffb7e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903318"
---
# <span data-ttu-id="2a2b0-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a2b0-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="2a2b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2b0-103">Обновляет удостоверение, назначенное ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="2a2b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a2b0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2b0-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2b0-106">Командлет **Set-AzExpressRoutePortIdentity** обновляет локальный объект Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="2a2b0-107">С помощью **Set-AzExpressRoutePort** назначьте ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="2a2b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a2b0-108">EXAMPLES</span></span>

### <span data-ttu-id="2a2b0-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a2b0-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="2a2b0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a2b0-110">PARAMETERS</span></span>

### <span data-ttu-id="2a2b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2b0-111">-DefaultProfile</span></span>
<span data-ttu-id="2a2b0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2b0-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a2b0-113">-ExpressRoutePort</span></span>
<span data-ttu-id="2a2b0-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a2b0-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="2a2b0-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="2a2b0-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="2a2b0-116">ResourceId для пользователя, которому назначена идентификация, для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="2a2b0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a2b0-117">-Confirm</span></span>
<span data-ttu-id="2a2b0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2b0-119">-WhatIf</span></span>
<span data-ttu-id="2a2b0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2b0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2b0-122">CommonParameters</span></span>
<span data-ttu-id="2a2b0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a2b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2b0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2b0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a2b0-125">INPUTS</span></span>

### <span data-ttu-id="2a2b0-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a2b0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="2a2b0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2b0-127">System.String</span></span>

## <span data-ttu-id="2a2b0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2b0-128">OUTPUTS</span></span>

### <span data-ttu-id="2a2b0-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a2b0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2a2b0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a2b0-130">NOTES</span></span>

## <span data-ttu-id="2a2b0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a2b0-131">RELATED LINKS</span></span>
[<span data-ttu-id="2a2b0-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a2b0-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="2a2b0-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a2b0-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="2a2b0-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a2b0-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
