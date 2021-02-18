---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223756"
---
# <span data-ttu-id="45a68-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="45a68-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="45a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a68-102">SYNOPSIS</span></span>
<span data-ttu-id="45a68-103">Создает объект Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="45a68-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="45a68-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45a68-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a68-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a68-105">DESCRIPTION</span></span>
<span data-ttu-id="45a68-106">Для **создания локального объекта Удостоверения** Azure ExpressRoutePort создается новый объект Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="45a68-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="45a68-107">Используйте **New-AzExpressRoutePort** или **Set-AzExpressRoutePort,** чтобы назначить его Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="45a68-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="45a68-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45a68-108">EXAMPLES</span></span>

### <span data-ttu-id="45a68-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45a68-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="45a68-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45a68-110">PARAMETERS</span></span>

### <span data-ttu-id="45a68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a68-111">-DefaultProfile</span></span>
<span data-ttu-id="45a68-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45a68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45a68-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="45a68-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="45a68-114">ResourceId идентификатора пользователя, назначенного ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="45a68-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="45a68-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45a68-115">-Confirm</span></span>
<span data-ttu-id="45a68-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a68-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a68-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a68-117">-WhatIf</span></span>
<span data-ttu-id="45a68-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a68-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45a68-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45a68-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a68-120">CommonParameters</span></span>
<span data-ttu-id="45a68-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a68-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a68-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a68-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45a68-123">INPUTS</span></span>

### <span data-ttu-id="45a68-124">System.String</span><span class="sxs-lookup"><span data-stu-id="45a68-124">System.String</span></span>

## <span data-ttu-id="45a68-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45a68-125">OUTPUTS</span></span>

### <span data-ttu-id="45a68-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="45a68-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="45a68-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45a68-127">NOTES</span></span>

## <span data-ttu-id="45a68-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45a68-128">RELATED LINKS</span></span>
[<span data-ttu-id="45a68-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="45a68-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="45a68-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="45a68-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="45a68-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="45a68-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)