---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409340"
---
# <span data-ttu-id="4d0c4-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="4d0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0c4-103">Обновляет политику конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="4d0c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d0c4-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d0c4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="4d0c4-106">Для создания политики конечных точек службы будет создана политика **Set-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="4d0c4-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4d0c4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="4d0c4-108">Пример 1. Задает политику конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="4d0c4-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4d0c4-109">Эта команда обновляет политику конечной точки службы "Политика1", $serviceEndpointPolicy относится к группе ресурсов "группа ресурсов1".</span><span class="sxs-lookup"><span data-stu-id="4d0c4-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4d0c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="4d0c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0c4-111">-DefaultProfile</span></span>
<span data-ttu-id="4d0c4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d0c4-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4d0c4-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0c4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d0c4-115">-Confirm</span></span>
<span data-ttu-id="4d0c4-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d0c4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d0c4-117">-WhatIf</span></span>
<span data-ttu-id="4d0c4-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d0c4-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d0c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0c4-120">CommonParameters</span></span>
<span data-ttu-id="4d0c4-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0c4-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d0c4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0c4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d0c4-123">INPUTS</span></span>

### <span data-ttu-id="4d0c4-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4d0c4-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d0c4-125">OUTPUTS</span></span>

### <span data-ttu-id="4d0c4-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4d0c4-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d0c4-127">NOTES</span></span>

## <span data-ttu-id="4d0c4-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d0c4-128">RELATED LINKS</span></span>

[<span data-ttu-id="4d0c4-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4d0c4-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4d0c4-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4d0c4-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
