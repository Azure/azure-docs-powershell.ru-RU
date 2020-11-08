---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: c5fc1c497bc0cb6f73aab4ddcfbc1ce127cc4545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074516"
---
# <span data-ttu-id="bd0fb-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd0fb-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="bd0fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0fb-103">Получение ключей учетной записи пространственных привязок</span><span class="sxs-lookup"><span data-stu-id="bd0fb-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="bd0fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd0fb-104">SYNTAX</span></span>

### <span data-ttu-id="bd0fb-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd0fb-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd0fb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0fb-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd0fb-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd0fb-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd0fb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd0fb-108">DESCRIPTION</span></span>
<span data-ttu-id="bd0fb-109">Получение ключей разработчика учетной записи пространственных привязок.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="bd0fb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd0fb-110">EXAMPLES</span></span>

### <span data-ttu-id="bd0fb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd0fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="bd0fb-112">Получение ключей разработчика учетной записи пространственного якоря "пример" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="bd0fb-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="bd0fb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd0fb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="bd0fb-114">Получение ключей разработчика учетной записи пространственного якоря "пример" из текущей подписки и группы ресурсов "Rg1" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="bd0fb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd0fb-115">PARAMETERS</span></span>

### <span data-ttu-id="bd0fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0fb-116">-DefaultProfile</span></span>
<span data-ttu-id="bd0fb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd0fb-118">-InputObject</span></span>
<span data-ttu-id="bd0fb-119">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-119">The custom domain object.</span></span>

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

### <span data-ttu-id="bd0fb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd0fb-120">-Name</span></span>
<span data-ttu-id="bd0fb-121">Имя учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="bd0fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd0fb-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd0fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd0fb-124">-ResourceId</span></span>
<span data-ttu-id="bd0fb-125">Идентификатор ресурса учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="bd0fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0fb-126">CommonParameters</span></span>
<span data-ttu-id="bd0fb-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd0fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd0fb-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0fb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0fb-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd0fb-129">INPUTS</span></span>

### <span data-ttu-id="bd0fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0fb-130">System.String</span></span>

### <span data-ttu-id="bd0fb-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="bd0fb-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="bd0fb-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd0fb-132">OUTPUTS</span></span>

### <span data-ttu-id="bd0fb-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd0fb-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="bd0fb-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd0fb-134">NOTES</span></span>

## <span data-ttu-id="bd0fb-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd0fb-135">RELATED LINKS</span></span>
