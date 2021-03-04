---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008707"
---
# <span data-ttu-id="d549b-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="d549b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d549b-102">SYNOPSIS</span></span>
<span data-ttu-id="d549b-103">Обновляет политику конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="d549b-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="d549b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d549b-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d549b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d549b-105">DESCRIPTION</span></span>
<span data-ttu-id="d549b-106">Для создания политики конечных точек службы будет создана политика **Set-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="d549b-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="d549b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d549b-107">EXAMPLES</span></span>

### <span data-ttu-id="d549b-108">Пример 1. Задает политику конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="d549b-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d549b-109">Эта команда обновляет политику конечной точки службы "Политика1", $serviceEndpointPolicy относится к группе ресурсов "группа ресурсов1".</span><span class="sxs-lookup"><span data-stu-id="d549b-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="d549b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d549b-110">PARAMETERS</span></span>

### <span data-ttu-id="d549b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d549b-111">-DefaultProfile</span></span>
<span data-ttu-id="d549b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d549b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d549b-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d549b-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="d549b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d549b-115">-Confirm</span></span>
<span data-ttu-id="d549b-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d549b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d549b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d549b-117">-WhatIf</span></span>
<span data-ttu-id="d549b-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d549b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d549b-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d549b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d549b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d549b-120">CommonParameters</span></span>
<span data-ttu-id="d549b-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d549b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d549b-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d549b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d549b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d549b-123">INPUTS</span></span>

### <span data-ttu-id="d549b-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d549b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d549b-125">OUTPUTS</span></span>

### <span data-ttu-id="d549b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d549b-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d549b-127">NOTES</span></span>

## <span data-ttu-id="d549b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d549b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d549b-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d549b-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d549b-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d549b-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
