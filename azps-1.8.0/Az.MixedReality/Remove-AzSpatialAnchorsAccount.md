---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d164e08876b5489ec45ce146f4f3c7cee3ee6d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899610"
---
# <span data-ttu-id="5d359-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="5d359-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="5d359-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d359-102">SYNOPSIS</span></span>
<span data-ttu-id="5d359-103">Удаление учетной записи пространственного якоря</span><span class="sxs-lookup"><span data-stu-id="5d359-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="5d359-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d359-104">SYNTAX</span></span>

### <span data-ttu-id="5d359-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d359-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d359-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d359-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d359-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d359-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d359-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d359-108">DESCRIPTION</span></span>
<span data-ttu-id="5d359-109">Удаление учетной записи указанной пространственной точки привязки из определенной подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d359-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="5d359-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d359-110">EXAMPLES</span></span>

### <span data-ttu-id="5d359-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d359-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="5d359-112">Удаление учетной записи пространственного якоря "пример" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="5d359-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="5d359-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d359-113">PARAMETERS</span></span>

### <span data-ttu-id="5d359-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d359-114">-Confirm</span></span>
<span data-ttu-id="5d359-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d359-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d359-116">-DefaultProfile</span></span>
<span data-ttu-id="5d359-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d359-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d359-118">-InputObject</span></span>
<span data-ttu-id="5d359-119">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="5d359-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d359-120">-Name</span></span>
<span data-ttu-id="5d359-121">Имя учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="5d359-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d359-122">-PassThru</span></span>
<span data-ttu-id="5d359-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="5d359-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d359-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d359-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d359-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d359-126">-ResourceId</span></span>
<span data-ttu-id="5d359-127">Идентификатор ресурса учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="5d359-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d359-128">-WhatIf</span></span>
<span data-ttu-id="5d359-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d359-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d359-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d359-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d359-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d359-131">CommonParameters</span></span>
<span data-ttu-id="5d359-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d359-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5d359-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d359-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d359-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d359-134">INPUTS</span></span>

### <span data-ttu-id="5d359-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5d359-135">System.String</span></span>

### <span data-ttu-id="5d359-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="5d359-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="5d359-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5d359-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5d359-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d359-138">OUTPUTS</span></span>

### <span data-ttu-id="5d359-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d359-139">System.Boolean</span></span>

## <span data-ttu-id="5d359-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d359-140">NOTES</span></span>

## <span data-ttu-id="5d359-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d359-141">RELATED LINKS</span></span>
