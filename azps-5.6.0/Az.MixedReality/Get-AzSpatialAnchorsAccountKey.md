---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 351b7a2412a861fcebc456d165e9fc4eddea5122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957064"
---
# <span data-ttu-id="3721f-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="3721f-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="3721f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3721f-102">SYNOPSIS</span></span>
<span data-ttu-id="3721f-103">Получить ключи учетной записи пространственных якорей</span><span class="sxs-lookup"><span data-stu-id="3721f-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="3721f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3721f-104">SYNTAX</span></span>

### <span data-ttu-id="3721f-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3721f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3721f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3721f-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3721f-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="3721f-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3721f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3721f-108">DESCRIPTION</span></span>
<span data-ttu-id="3721f-109">Получите клавиши разработчика для учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="3721f-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="3721f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3721f-110">EXAMPLES</span></span>

### <span data-ttu-id="3721f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3721f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="3721f-112">Получите ключи разработчика для пространственной привязки учетной записи "example" из текущей группы подписок и ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="3721f-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="3721f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3721f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="3721f-114">Получите ключи разработчика учетной записи пространственой привязки "example" из текущей подписки и группы ресурсов "rg1" с piping.</span><span class="sxs-lookup"><span data-stu-id="3721f-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="3721f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3721f-115">PARAMETERS</span></span>

### <span data-ttu-id="3721f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3721f-116">-DefaultProfile</span></span>
<span data-ttu-id="3721f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3721f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3721f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3721f-118">-InputObject</span></span>
<span data-ttu-id="3721f-119">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="3721f-119">The custom domain object.</span></span>

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

### <span data-ttu-id="3721f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3721f-120">-Name</span></span>
<span data-ttu-id="3721f-121">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="3721f-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="3721f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3721f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3721f-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3721f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="3721f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3721f-124">-ResourceId</span></span>
<span data-ttu-id="3721f-125">ИД ресурса учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="3721f-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="3721f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3721f-126">CommonParameters</span></span>
<span data-ttu-id="3721f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3721f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3721f-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3721f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3721f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3721f-129">INPUTS</span></span>

### <span data-ttu-id="3721f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3721f-130">System.String</span></span>

### <span data-ttu-id="3721f-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3721f-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="3721f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3721f-132">OUTPUTS</span></span>

### <span data-ttu-id="3721f-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3721f-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="3721f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3721f-134">NOTES</span></span>

## <span data-ttu-id="3721f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3721f-135">RELATED LINKS</span></span>
