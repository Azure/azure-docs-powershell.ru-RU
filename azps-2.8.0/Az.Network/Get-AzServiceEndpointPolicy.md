---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902850"
---
# <span data-ttu-id="cdc24-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc24-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="cdc24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cdc24-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc24-103">Получает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cdc24-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="cdc24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cdc24-104">SYNTAX</span></span>

### <span data-ttu-id="cdc24-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cdc24-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdc24-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdc24-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc24-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdc24-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc24-108">Командлет **Get-AzServiceEndpointPolicy** получает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cdc24-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="cdc24-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cdc24-109">EXAMPLES</span></span>

### <span data-ttu-id="cdc24-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdc24-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cdc24-111">Эта команда получает политику конечной точки службы с именем ServiceEndpointPolicy1, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $policy.</span><span class="sxs-lookup"><span data-stu-id="cdc24-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="cdc24-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cdc24-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cdc24-113">Эта команда получает список всех политик конечной точки службы в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $policyList.</span><span class="sxs-lookup"><span data-stu-id="cdc24-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="cdc24-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cdc24-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="cdc24-115">Эта команда получает список всех политик конечной точки службы, которые начинаются с "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="cdc24-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="cdc24-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cdc24-116">PARAMETERS</span></span>

### <span data-ttu-id="cdc24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc24-117">-DefaultProfile</span></span>
<span data-ttu-id="cdc24-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc24-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc24-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cdc24-119">-Name</span></span>
<span data-ttu-id="cdc24-120">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cdc24-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="cdc24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc24-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdc24-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cdc24-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cdc24-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdc24-123">-ResourceId</span></span>
<span data-ttu-id="cdc24-124">Идентификатор политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cdc24-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc24-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdc24-125">-Confirm</span></span>
<span data-ttu-id="cdc24-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cdc24-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc24-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc24-127">-WhatIf</span></span>
<span data-ttu-id="cdc24-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cdc24-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdc24-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cdc24-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc24-130">CommonParameters</span></span>
<span data-ttu-id="cdc24-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cdc24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc24-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdc24-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc24-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cdc24-133">INPUTS</span></span>

### <span data-ttu-id="cdc24-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc24-134">System.String</span></span>

## <span data-ttu-id="cdc24-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdc24-135">OUTPUTS</span></span>

### <span data-ttu-id="cdc24-136">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc24-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cdc24-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cdc24-137">NOTES</span></span>

## <span data-ttu-id="cdc24-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdc24-138">RELATED LINKS</span></span>

[<span data-ttu-id="cdc24-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc24-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cdc24-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc24-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cdc24-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc24-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
