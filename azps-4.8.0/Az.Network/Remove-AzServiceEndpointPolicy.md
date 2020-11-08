---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079438"
---
# <span data-ttu-id="ad94d-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad94d-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ad94d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad94d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad94d-103">Удаление политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ad94d-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="ad94d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad94d-104">SYNTAX</span></span>

### <span data-ttu-id="ad94d-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad94d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad94d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad94d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad94d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad94d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad94d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad94d-108">DESCRIPTION</span></span>
<span data-ttu-id="ad94d-109">Командлет **Remove-AzServiceEndpointPolicy** удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ad94d-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="ad94d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad94d-110">EXAMPLES</span></span>

### <span data-ttu-id="ad94d-111">Пример 1: Удаление политики конечной точки службы с помощью имени</span><span class="sxs-lookup"><span data-stu-id="ad94d-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ad94d-112">Эта команда удаляет политику конечной точки службы с именем Policy1, которая принадлежит к параметру resourcegroup с именем "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ad94d-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="ad94d-113">Пример 2: Удаление политики конечной точки службы с помощью объекта input</span><span class="sxs-lookup"><span data-stu-id="ad94d-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ad94d-114">Эта команда удаляет объект политики конечной точки службы Policy1, который принадлежит к параметру resourcegroup с именем "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ad94d-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="ad94d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad94d-115">PARAMETERS</span></span>

### <span data-ttu-id="ad94d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad94d-116">-DefaultProfile</span></span>
<span data-ttu-id="ad94d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad94d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad94d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad94d-118">-Force</span></span>
<span data-ttu-id="ad94d-119">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="ad94d-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad94d-120">-InputObject</span></span>
<span data-ttu-id="ad94d-121">Объект политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ad94d-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad94d-122">-Name</span></span>
<span data-ttu-id="ad94d-123">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ad94d-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad94d-124">-PassThru</span></span>
<span data-ttu-id="ad94d-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ad94d-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad94d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad94d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad94d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad94d-128">-ResourceId</span></span>
<span data-ttu-id="ad94d-129">Идентификатор политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ad94d-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad94d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad94d-130">-Confirm</span></span>
<span data-ttu-id="ad94d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad94d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad94d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad94d-132">-WhatIf</span></span>
<span data-ttu-id="ad94d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad94d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad94d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad94d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad94d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad94d-135">CommonParameters</span></span>
<span data-ttu-id="ad94d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad94d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad94d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad94d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad94d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad94d-138">INPUTS</span></span>

### <span data-ttu-id="ad94d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad94d-139">System.String</span></span>

### <span data-ttu-id="ad94d-140">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad94d-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ad94d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad94d-141">OUTPUTS</span></span>

### <span data-ttu-id="ad94d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad94d-142">System.Boolean</span></span>

## <span data-ttu-id="ad94d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad94d-143">NOTES</span></span>

## <span data-ttu-id="ad94d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad94d-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad94d-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad94d-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ad94d-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad94d-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ad94d-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ad94d-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)