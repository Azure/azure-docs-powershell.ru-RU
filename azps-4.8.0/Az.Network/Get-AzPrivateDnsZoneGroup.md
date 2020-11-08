---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235530"
---
# <span data-ttu-id="c60e2-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="c60e2-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="c60e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c60e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c60e2-103">Возвращает зону частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="c60e2-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="c60e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c60e2-104">SYNTAX</span></span>

### <span data-ttu-id="c60e2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c60e2-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c60e2-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="c60e2-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c60e2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c60e2-107">DESCRIPTION</span></span>
<span data-ttu-id="c60e2-108">Командлет **Get-AzPrivateDnsZoneGroup** получает одну или несколько закрытых групп зон DNS.</span><span class="sxs-lookup"><span data-stu-id="c60e2-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="c60e2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c60e2-109">EXAMPLES</span></span>

### <span data-ttu-id="c60e2-110">Пример 1: получение конфиденциальной группы зон DNS</span><span class="sxs-lookup"><span data-stu-id="c60e2-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="c60e2-111">В приведенном выше примере вы возвращаете зону частной зоны DNS с именем dnsgroup1 в группе ресурсов RG.</span><span class="sxs-lookup"><span data-stu-id="c60e2-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="c60e2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c60e2-112">PARAMETERS</span></span>

### <span data-ttu-id="c60e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60e2-113">-DefaultProfile</span></span>
<span data-ttu-id="c60e2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c60e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c60e2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c60e2-115">-Name</span></span>
<span data-ttu-id="c60e2-116">Имя частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="c60e2-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c60e2-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="c60e2-117">-PrivateEndpointName</span></span>
<span data-ttu-id="c60e2-118">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c60e2-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c60e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="c60e2-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c60e2-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c60e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60e2-121">CommonParameters</span></span>
<span data-ttu-id="c60e2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c60e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60e2-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c60e2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60e2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c60e2-124">INPUTS</span></span>

### <span data-ttu-id="c60e2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c60e2-125">System.String</span></span>

## <span data-ttu-id="c60e2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c60e2-126">OUTPUTS</span></span>

### <span data-ttu-id="c60e2-127">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="c60e2-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="c60e2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c60e2-128">NOTES</span></span>

## <span data-ttu-id="c60e2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c60e2-129">RELATED LINKS</span></span>
