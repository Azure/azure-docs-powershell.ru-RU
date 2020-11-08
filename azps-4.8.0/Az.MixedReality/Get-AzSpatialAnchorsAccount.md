---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079945"
---
# <span data-ttu-id="88b4d-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="88b4d-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="88b4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="88b4d-103">Получение учетной записи пространственного якоря</span><span class="sxs-lookup"><span data-stu-id="88b4d-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="88b4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88b4d-104">SYNTAX</span></span>

### <span data-ttu-id="88b4d-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88b4d-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b4d-106">Параметр "параметризованный" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88b4d-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b4d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b4d-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b4d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88b4d-108">DESCRIPTION</span></span>
<span data-ttu-id="88b4d-109">Получение или перечисление учетных записей пространственных привязок в некоторых подписках и группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88b4d-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="88b4d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88b4d-110">EXAMPLES</span></span>

### <span data-ttu-id="88b4d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88b4d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="88b4d-112">Список всех пространственных привязок учетной записи в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="88b4d-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="88b4d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88b4d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="88b4d-114">Получение учетной записи пространственного якоря "пример" в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="88b4d-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="88b4d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88b4d-115">PARAMETERS</span></span>

### <span data-ttu-id="88b4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b4d-116">-DefaultProfile</span></span>
<span data-ttu-id="88b4d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88b4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b4d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88b4d-118">-Name</span></span>
<span data-ttu-id="88b4d-119">Имя учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="88b4d-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b4d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b4d-120">-ResourceGroupName</span></span>
<span data-ttu-id="88b4d-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88b4d-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b4d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88b4d-122">-ResourceId</span></span>
<span data-ttu-id="88b4d-123">Идентификатор ресурса учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="88b4d-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="88b4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b4d-124">CommonParameters</span></span>
<span data-ttu-id="88b4d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88b4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88b4d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b4d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b4d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88b4d-127">INPUTS</span></span>

### <span data-ttu-id="88b4d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88b4d-128">System.String</span></span>

## <span data-ttu-id="88b4d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88b4d-129">OUTPUTS</span></span>

### <span data-ttu-id="88b4d-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="88b4d-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="88b4d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="88b4d-131">NOTES</span></span>

## <span data-ttu-id="88b4d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88b4d-132">RELATED LINKS</span></span>