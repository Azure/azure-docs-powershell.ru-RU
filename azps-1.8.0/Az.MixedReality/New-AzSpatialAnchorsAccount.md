---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 7ead8ca49491db9443f6cb0b06f87cb4917fc375
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899613"
---
# <span data-ttu-id="979a6-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="979a6-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="979a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="979a6-102">SYNOPSIS</span></span>
<span data-ttu-id="979a6-103">Создание учетной записи пространственного якоря</span><span class="sxs-lookup"><span data-stu-id="979a6-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="979a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="979a6-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="979a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="979a6-105">DESCRIPTION</span></span>
<span data-ttu-id="979a6-106">Создайте новую учетную запись пространственного Inelligence в определенной подписке, группе ресурсов и регионе.</span><span class="sxs-lookup"><span data-stu-id="979a6-106">Create a new Spatial Inelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="979a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="979a6-107">EXAMPLES</span></span>

### <span data-ttu-id="979a6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="979a6-108">Example 1</span></span>
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

<span data-ttu-id="979a6-109">Создайте новую учетную запись пространственного якоря "пример" в текущей подписке, группе ресурсов "Rg1" и центральному каналу США.</span><span class="sxs-lookup"><span data-stu-id="979a6-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="979a6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="979a6-110">PARAMETERS</span></span>

### <span data-ttu-id="979a6-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="979a6-111">-Confirm</span></span>
<span data-ttu-id="979a6-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="979a6-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="979a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979a6-113">-DefaultProfile</span></span>
<span data-ttu-id="979a6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="979a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="979a6-115">-Location</span><span class="sxs-lookup"><span data-stu-id="979a6-115">-Location</span></span>
<span data-ttu-id="979a6-116">Расположение учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="979a6-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="979a6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="979a6-117">-Name</span></span>
<span data-ttu-id="979a6-118">Имя учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="979a6-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="979a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="979a6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="979a6-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="979a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979a6-121">-WhatIf</span></span>
<span data-ttu-id="979a6-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="979a6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="979a6-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="979a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="979a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979a6-124">CommonParameters</span></span>
<span data-ttu-id="979a6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="979a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="979a6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979a6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="979a6-127">INPUTS</span></span>

### <span data-ttu-id="979a6-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="979a6-128">None</span></span>

## <span data-ttu-id="979a6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="979a6-129">OUTPUTS</span></span>

### <span data-ttu-id="979a6-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="979a6-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="979a6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="979a6-131">NOTES</span></span>

## <span data-ttu-id="979a6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="979a6-132">RELATED LINKS</span></span>
