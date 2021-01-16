---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415172"
---
# <span data-ttu-id="c44b4-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c44b4-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c44b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c44b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c44b4-103">Учетная запись "Получить пространственные привязки"</span><span class="sxs-lookup"><span data-stu-id="c44b4-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="c44b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c44b4-104">SYNTAX</span></span>

### <span data-ttu-id="c44b4-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c44b4-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c44b4-106">GetParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c44b4-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c44b4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b4-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c44b4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c44b4-108">DESCRIPTION</span></span>
<span data-ttu-id="c44b4-109">Получить или перечислить пространственные привязки учетных записей в определенных группах подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c44b4-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="c44b4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c44b4-110">EXAMPLES</span></span>

### <span data-ttu-id="c44b4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c44b4-111">Example 1</span></span>
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

<span data-ttu-id="c44b4-112">Перечислить все пространственные привязки в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="c44b4-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="c44b4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c44b4-113">Example 2</span></span>
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

<span data-ttu-id="c44b4-114">Получить пространственную привязку "пример" учетной записи в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="c44b4-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="c44b4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c44b4-115">PARAMETERS</span></span>

### <span data-ttu-id="c44b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44b4-116">-DefaultProfile</span></span>
<span data-ttu-id="c44b4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c44b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c44b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c44b4-118">-Name</span></span>
<span data-ttu-id="c44b4-119">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="c44b4-119">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="c44b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c44b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="c44b4-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c44b4-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="c44b4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c44b4-122">-ResourceId</span></span>
<span data-ttu-id="c44b4-123">ИД ресурса учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="c44b4-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="c44b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44b4-124">CommonParameters</span></span>
<span data-ttu-id="c44b4-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c44b4-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44b4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44b4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c44b4-127">INPUTS</span></span>

### <span data-ttu-id="c44b4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c44b4-128">System.String</span></span>

## <span data-ttu-id="c44b4-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c44b4-129">OUTPUTS</span></span>

### <span data-ttu-id="c44b4-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c44b4-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c44b4-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c44b4-131">NOTES</span></span>

## <span data-ttu-id="c44b4-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c44b4-132">RELATED LINKS</span></span>