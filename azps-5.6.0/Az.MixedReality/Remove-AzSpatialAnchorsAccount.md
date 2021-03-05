---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980371"
---
# <span data-ttu-id="86d91-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="86d91-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="86d91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d91-102">SYNOPSIS</span></span>
<span data-ttu-id="86d91-103">Учетная запись "Удалить пространственные привязки"</span><span class="sxs-lookup"><span data-stu-id="86d91-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="86d91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86d91-104">SYNTAX</span></span>

### <span data-ttu-id="86d91-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86d91-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d91-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d91-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d91-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d91-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d91-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86d91-108">DESCRIPTION</span></span>
<span data-ttu-id="86d91-109">Удалить указанную учетную запись пространственной привязки из определенной группы подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86d91-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="86d91-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86d91-110">EXAMPLES</span></span>

### <span data-ttu-id="86d91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86d91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="86d91-112">Удалить пространственную привязку "пример" учетной записи из текущей подписки и группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="86d91-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="86d91-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86d91-113">PARAMETERS</span></span>

### <span data-ttu-id="86d91-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86d91-114">-Confirm</span></span>
<span data-ttu-id="86d91-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d91-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d91-116">-DefaultProfile</span></span>
<span data-ttu-id="86d91-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86d91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d91-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d91-118">-InputObject</span></span>
<span data-ttu-id="86d91-119">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="86d91-119">The custom domain object.</span></span>

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

### <span data-ttu-id="86d91-120">-Name</span><span class="sxs-lookup"><span data-stu-id="86d91-120">-Name</span></span>
<span data-ttu-id="86d91-121">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="86d91-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="86d91-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86d91-122">-PassThru</span></span>
<span data-ttu-id="86d91-123">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="86d91-123">Return object if specified.</span></span>

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

### <span data-ttu-id="86d91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d91-124">-ResourceGroupName</span></span>
<span data-ttu-id="86d91-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86d91-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="86d91-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86d91-126">-ResourceId</span></span>
<span data-ttu-id="86d91-127">ИД ресурса учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="86d91-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="86d91-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d91-128">-WhatIf</span></span>
<span data-ttu-id="86d91-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d91-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d91-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86d91-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d91-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d91-131">CommonParameters</span></span>
<span data-ttu-id="86d91-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d91-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="86d91-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d91-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d91-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86d91-134">INPUTS</span></span>

### <span data-ttu-id="86d91-135">System.String</span><span class="sxs-lookup"><span data-stu-id="86d91-135">System.String</span></span>

### <span data-ttu-id="86d91-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="86d91-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="86d91-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86d91-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86d91-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86d91-138">OUTPUTS</span></span>

### <span data-ttu-id="86d91-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86d91-139">System.Boolean</span></span>

## <span data-ttu-id="86d91-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86d91-140">NOTES</span></span>

## <span data-ttu-id="86d91-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86d91-141">RELATED LINKS</span></span>
