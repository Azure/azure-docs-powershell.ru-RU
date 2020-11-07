---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: b51aac195a6f0f4870b89894cce8f26c732077ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902182"
---
# <span data-ttu-id="5e766-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e766-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5e766-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e766-102">SYNOPSIS</span></span>
<span data-ttu-id="5e766-103">Создание Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="5e766-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="5e766-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e766-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e766-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e766-105">DESCRIPTION</span></span>
<span data-ttu-id="5e766-106">Командлет **New-AzExpressRoutePortIdentity** создает локальный объект Azure ExpressRoutePort Identity.</span><span class="sxs-lookup"><span data-stu-id="5e766-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="5e766-107">С помощью **New-AzExpressRoutePort** или **Set-AzExpressRoutePort** назначьте его в Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="5e766-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="5e766-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e766-108">EXAMPLES</span></span>

### <span data-ttu-id="5e766-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e766-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="5e766-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e766-110">PARAMETERS</span></span>

### <span data-ttu-id="5e766-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e766-111">-DefaultProfile</span></span>
<span data-ttu-id="5e766-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e766-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e766-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="5e766-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="5e766-114">ResourceId для пользователя, которому назначена идентификация, для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="5e766-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="5e766-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e766-115">-Confirm</span></span>
<span data-ttu-id="5e766-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e766-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e766-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e766-117">-WhatIf</span></span>
<span data-ttu-id="5e766-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e766-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e766-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e766-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e766-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e766-120">CommonParameters</span></span>
<span data-ttu-id="5e766-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e766-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e766-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e766-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e766-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e766-123">INPUTS</span></span>

### <span data-ttu-id="5e766-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5e766-124">System.String</span></span>

## <span data-ttu-id="5e766-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e766-125">OUTPUTS</span></span>

### <span data-ttu-id="5e766-126">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5e766-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="5e766-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e766-127">NOTES</span></span>

## <span data-ttu-id="5e766-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e766-128">RELATED LINKS</span></span>
[<span data-ttu-id="5e766-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e766-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5e766-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e766-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5e766-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5e766-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)