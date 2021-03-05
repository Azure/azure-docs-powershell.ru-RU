---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: e3b3b0a0990f8c72fcd18d8828ae97d5c1a8a5aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015043"
---
# <span data-ttu-id="57aa8-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="57aa8-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="57aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="57aa8-103">Создает объект Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="57aa8-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="57aa8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57aa8-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57aa8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="57aa8-106">С **его использованием** создается локальный объект удостоверения Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="57aa8-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="57aa8-107">Используйте **New-AzExpressRoutePort** или **Set-AzExpressRoutePort,** чтобы назначить его Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="57aa8-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="57aa8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57aa8-108">EXAMPLES</span></span>

### <span data-ttu-id="57aa8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57aa8-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="57aa8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57aa8-110">PARAMETERS</span></span>

### <span data-ttu-id="57aa8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57aa8-111">-DefaultProfile</span></span>
<span data-ttu-id="57aa8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57aa8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57aa8-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="57aa8-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="57aa8-114">ResourceId идентификатора пользователя, назначенного ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="57aa8-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="57aa8-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57aa8-115">-Confirm</span></span>
<span data-ttu-id="57aa8-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57aa8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57aa8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57aa8-117">-WhatIf</span></span>
<span data-ttu-id="57aa8-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57aa8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57aa8-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57aa8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57aa8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57aa8-120">CommonParameters</span></span>
<span data-ttu-id="57aa8-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57aa8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57aa8-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57aa8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57aa8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57aa8-123">INPUTS</span></span>

### <span data-ttu-id="57aa8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="57aa8-124">System.String</span></span>

## <span data-ttu-id="57aa8-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57aa8-125">OUTPUTS</span></span>

### <span data-ttu-id="57aa8-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="57aa8-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="57aa8-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57aa8-127">NOTES</span></span>

## <span data-ttu-id="57aa8-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57aa8-128">RELATED LINKS</span></span>
[<span data-ttu-id="57aa8-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="57aa8-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="57aa8-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="57aa8-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="57aa8-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="57aa8-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)