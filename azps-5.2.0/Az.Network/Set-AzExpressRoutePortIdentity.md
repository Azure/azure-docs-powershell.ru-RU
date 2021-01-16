---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326987"
---
# <span data-ttu-id="0cd3d-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0cd3d-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="0cd3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd3d-103">Обновляет удостоверение, назначенное ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="0cd3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0cd3d-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cd3d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cd3d-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd3d-106">**Cmdlet Set-AzExpressRoutePortIdentity** обновляет локальный объект Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="0cd3d-107">Используйте **Set-AzExpressRoutePort,** чтобы назначить его ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="0cd3d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0cd3d-108">EXAMPLES</span></span>

### <span data-ttu-id="0cd3d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0cd3d-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="0cd3d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cd3d-110">PARAMETERS</span></span>

### <span data-ttu-id="0cd3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd3d-111">-DefaultProfile</span></span>
<span data-ttu-id="0cd3d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cd3d-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0cd3d-113">-ExpressRoutePort</span></span>
<span data-ttu-id="0cd3d-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0cd3d-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="0cd3d-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="0cd3d-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="0cd3d-116">ResourceId идентификатора пользователя, назначенного expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="0cd3d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cd3d-117">-Confirm</span></span>
<span data-ttu-id="0cd3d-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd3d-119">-WhatIf</span></span>
<span data-ttu-id="0cd3d-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd3d-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd3d-122">CommonParameters</span></span>
<span data-ttu-id="0cd3d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd3d-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd3d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd3d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cd3d-125">INPUTS</span></span>

### <span data-ttu-id="0cd3d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0cd3d-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="0cd3d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0cd3d-127">System.String</span></span>

## <span data-ttu-id="0cd3d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0cd3d-128">OUTPUTS</span></span>

### <span data-ttu-id="0cd3d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0cd3d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="0cd3d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0cd3d-130">NOTES</span></span>

## <span data-ttu-id="0cd3d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cd3d-131">RELATED LINKS</span></span>
[<span data-ttu-id="0cd3d-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0cd3d-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0cd3d-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0cd3d-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0cd3d-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0cd3d-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)