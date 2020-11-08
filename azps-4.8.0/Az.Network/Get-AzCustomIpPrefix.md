---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078941"
---
# <span data-ttu-id="0d441-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="0d441-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d441-102">SYNOPSIS</span></span>
<span data-ttu-id="0d441-103">Возвращает ресурс CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="0d441-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d441-104">SYNTAX</span></span>

### <span data-ttu-id="0d441-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d441-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d441-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d441-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d441-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d441-107">DESCRIPTION</span></span>
<span data-ttu-id="0d441-108">Командлет **Get-AzCustomIpPrefix** получает один или несколько CustomIpPrefixes с указанным набором входных параметров.</span><span class="sxs-lookup"><span data-stu-id="0d441-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="0d441-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d441-109">EXAMPLES</span></span>

### <span data-ttu-id="0d441-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d441-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="0d441-111">Эта команда получает ресурс CustomIpPrefix с именем myCustomIpPrefix в группе ресурсов myRg</span><span class="sxs-lookup"><span data-stu-id="0d441-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="0d441-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d441-112">PARAMETERS</span></span>

### <span data-ttu-id="0d441-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d441-113">-DefaultProfile</span></span>
<span data-ttu-id="0d441-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d441-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d441-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d441-115">-Name</span></span>
<span data-ttu-id="0d441-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d441-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d441-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d441-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d441-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d441-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d441-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d441-119">-ResourceId</span></span>
<span data-ttu-id="0d441-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d441-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d441-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d441-121">CommonParameters</span></span>
<span data-ttu-id="0d441-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d441-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d441-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d441-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d441-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d441-124">INPUTS</span></span>

### <span data-ttu-id="0d441-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0d441-125">System.String</span></span>

## <span data-ttu-id="0d441-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d441-126">OUTPUTS</span></span>

### <span data-ttu-id="0d441-127">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="0d441-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d441-128">NOTES</span></span>

## <span data-ttu-id="0d441-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d441-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d441-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="0d441-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="0d441-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d441-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)