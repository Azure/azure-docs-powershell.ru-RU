---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220996"
---
# <span data-ttu-id="76e04-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76e04-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="76e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e04-102">SYNOPSIS</span></span>
<span data-ttu-id="76e04-103">Удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="76e04-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="76e04-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76e04-104">SYNTAX</span></span>

### <span data-ttu-id="76e04-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76e04-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e04-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76e04-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e04-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76e04-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e04-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76e04-108">DESCRIPTION</span></span>
<span data-ttu-id="76e04-109">Для удаления политики конечных точек службы будет назначена cmdlet **Remove-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="76e04-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="76e04-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76e04-110">EXAMPLES</span></span>

### <span data-ttu-id="76e04-111">Пример 1. Удаление политики конечной точки службы с использованием имени</span><span class="sxs-lookup"><span data-stu-id="76e04-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="76e04-112">Эта команда удаляет политику конечной точки службы с именем Policy1, которая относится к группе ресурсов с именем resourcegroup1.</span><span class="sxs-lookup"><span data-stu-id="76e04-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="76e04-113">Пример 2. Удаление политики конечной точки службы с помощью объекта ввода</span><span class="sxs-lookup"><span data-stu-id="76e04-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="76e04-114">Эта команда удаляет объект политики конечных точек обслуживания Policy1, принадлежащий группе ресурсов с именем resourcegroup1.</span><span class="sxs-lookup"><span data-stu-id="76e04-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="76e04-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76e04-115">PARAMETERS</span></span>

### <span data-ttu-id="76e04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e04-116">-DefaultProfile</span></span>
<span data-ttu-id="76e04-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76e04-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e04-118">-Force</span><span class="sxs-lookup"><span data-stu-id="76e04-118">-Force</span></span>
<span data-ttu-id="76e04-119">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="76e04-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="76e04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76e04-120">-InputObject</span></span>
<span data-ttu-id="76e04-121">Объект политики конечных точек обслуживания.</span><span class="sxs-lookup"><span data-stu-id="76e04-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="76e04-122">-Name</span><span class="sxs-lookup"><span data-stu-id="76e04-122">-Name</span></span>
<span data-ttu-id="76e04-123">Имя политики конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="76e04-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="76e04-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76e04-124">-PassThru</span></span>
<span data-ttu-id="76e04-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="76e04-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="76e04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e04-126">-ResourceGroupName</span></span>
<span data-ttu-id="76e04-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76e04-127">The resource group name.</span></span>

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

### <span data-ttu-id="76e04-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76e04-128">-ResourceId</span></span>
<span data-ttu-id="76e04-129">ИД политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="76e04-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="76e04-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76e04-130">-Confirm</span></span>
<span data-ttu-id="76e04-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76e04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e04-132">-WhatIf</span></span>
<span data-ttu-id="76e04-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76e04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76e04-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76e04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76e04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e04-135">CommonParameters</span></span>
<span data-ttu-id="76e04-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e04-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e04-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e04-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76e04-138">INPUTS</span></span>

### <span data-ttu-id="76e04-139">System.String</span><span class="sxs-lookup"><span data-stu-id="76e04-139">System.String</span></span>

### <span data-ttu-id="76e04-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76e04-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="76e04-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76e04-141">OUTPUTS</span></span>

### <span data-ttu-id="76e04-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76e04-142">System.Boolean</span></span>

## <span data-ttu-id="76e04-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76e04-143">NOTES</span></span>

## <span data-ttu-id="76e04-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76e04-144">RELATED LINKS</span></span>

[<span data-ttu-id="76e04-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76e04-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="76e04-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76e04-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="76e04-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76e04-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
