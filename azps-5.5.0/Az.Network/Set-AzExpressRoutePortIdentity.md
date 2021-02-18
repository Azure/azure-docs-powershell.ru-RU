---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240576"
---
# <span data-ttu-id="4737b-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4737b-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="4737b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4737b-102">SYNOPSIS</span></span>
<span data-ttu-id="4737b-103">Обновляет удостоверение, назначенное ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4737b-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="4737b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4737b-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4737b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4737b-105">DESCRIPTION</span></span>
<span data-ttu-id="4737b-106">Для локального объекта Azure ExpressRoutePort с его использованием обновляется объект **Set-AzExpressRoutePortIdentity.**</span><span class="sxs-lookup"><span data-stu-id="4737b-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="4737b-107">Используйте **Set-AzExpressRoutePort,** чтобы назначить его ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4737b-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="4737b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4737b-108">EXAMPLES</span></span>

### <span data-ttu-id="4737b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4737b-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="4737b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4737b-110">PARAMETERS</span></span>

### <span data-ttu-id="4737b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4737b-111">-DefaultProfile</span></span>
<span data-ttu-id="4737b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4737b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4737b-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4737b-113">-ExpressRoutePort</span></span>
<span data-ttu-id="4737b-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4737b-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="4737b-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="4737b-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="4737b-116">ResourceId идентификатора пользователя, назначенного expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4737b-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="4737b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4737b-117">-Confirm</span></span>
<span data-ttu-id="4737b-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4737b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4737b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4737b-119">-WhatIf</span></span>
<span data-ttu-id="4737b-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4737b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4737b-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4737b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4737b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4737b-122">CommonParameters</span></span>
<span data-ttu-id="4737b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4737b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4737b-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4737b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4737b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4737b-125">INPUTS</span></span>

### <span data-ttu-id="4737b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4737b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="4737b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4737b-127">System.String</span></span>

## <span data-ttu-id="4737b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4737b-128">OUTPUTS</span></span>

### <span data-ttu-id="4737b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4737b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4737b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4737b-130">NOTES</span></span>

## <span data-ttu-id="4737b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4737b-131">RELATED LINKS</span></span>
[<span data-ttu-id="4737b-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4737b-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4737b-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4737b-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4737b-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4737b-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
