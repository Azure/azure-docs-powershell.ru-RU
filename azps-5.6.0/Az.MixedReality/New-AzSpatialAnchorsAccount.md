---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970520"
---
# <span data-ttu-id="7efde-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7efde-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="7efde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7efde-102">SYNOPSIS</span></span>
<span data-ttu-id="7efde-103">Создание учетной записи пространственных якорей</span><span class="sxs-lookup"><span data-stu-id="7efde-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="7efde-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7efde-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7efde-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7efde-105">DESCRIPTION</span></span>
<span data-ttu-id="7efde-106">Создайте новую учетную запись пространственной привязки в определенной подписке, группе ресурсов и регионе.</span><span class="sxs-lookup"><span data-stu-id="7efde-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="7efde-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7efde-107">EXAMPLES</span></span>

### <span data-ttu-id="7efde-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7efde-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="7efde-109">Создайте новый пространственный "пример" учетной записи с привязкой в текущей подписке, группе ресурсов "rg1" и Центральной США.</span><span class="sxs-lookup"><span data-stu-id="7efde-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="7efde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7efde-110">PARAMETERS</span></span>

### <span data-ttu-id="7efde-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7efde-111">-Confirm</span></span>
<span data-ttu-id="7efde-112">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7efde-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efde-113">-DefaultProfile</span></span>
<span data-ttu-id="7efde-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7efde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efde-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7efde-115">-Location</span></span>
<span data-ttu-id="7efde-116">Расположение учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="7efde-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efde-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7efde-117">-Name</span></span>
<span data-ttu-id="7efde-118">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="7efde-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efde-119">-ResourceGroupName</span></span>
<span data-ttu-id="7efde-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7efde-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efde-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efde-121">-WhatIf</span></span>
<span data-ttu-id="7efde-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efde-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7efde-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7efde-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efde-124">CommonParameters</span></span>
<span data-ttu-id="7efde-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7efde-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efde-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efde-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7efde-127">INPUTS</span></span>

### <span data-ttu-id="7efde-128">Нет</span><span class="sxs-lookup"><span data-stu-id="7efde-128">None</span></span>

## <span data-ttu-id="7efde-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7efde-129">OUTPUTS</span></span>

### <span data-ttu-id="7efde-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7efde-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="7efde-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7efde-131">NOTES</span></span>

## <span data-ttu-id="7efde-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7efde-132">RELATED LINKS</span></span>
