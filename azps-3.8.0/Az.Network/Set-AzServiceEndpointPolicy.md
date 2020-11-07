---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912963"
---
# <span data-ttu-id="f7261-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7261-102">SYNOPSIS</span></span>
<span data-ttu-id="f7261-103">Обновление политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="f7261-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="f7261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7261-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7261-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7261-105">DESCRIPTION</span></span>
<span data-ttu-id="f7261-106">Командлет **Set-AzServiceEndpointPolicy** , чтобы создать политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="f7261-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="f7261-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7261-107">EXAMPLES</span></span>

### <span data-ttu-id="f7261-108">Пример 1: Настройка политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="f7261-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f7261-109">Эта команда обновляет политику конечной точки службы с именем Policy1, определенную объектом, $serviceEndpointPolicy принадлежит к группе ресурсов "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="f7261-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="f7261-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7261-110">PARAMETERS</span></span>

### <span data-ttu-id="f7261-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7261-111">-DefaultProfile</span></span>
<span data-ttu-id="f7261-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7261-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7261-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f7261-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f7261-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7261-115">-Confirm</span></span>
<span data-ttu-id="f7261-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7261-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7261-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7261-117">-WhatIf</span></span>
<span data-ttu-id="f7261-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7261-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7261-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7261-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7261-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7261-120">CommonParameters</span></span>
<span data-ttu-id="f7261-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7261-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7261-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7261-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7261-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7261-123">INPUTS</span></span>

### <span data-ttu-id="f7261-124">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7261-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7261-125">OUTPUTS</span></span>

### <span data-ttu-id="f7261-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7261-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7261-127">NOTES</span></span>

## <span data-ttu-id="f7261-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7261-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7261-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7261-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7261-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7261-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
