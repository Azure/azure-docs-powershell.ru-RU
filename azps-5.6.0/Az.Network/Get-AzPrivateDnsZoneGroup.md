---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: f9428c2249cf69d366a6770d448e82618d98896f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954232"
---
# <span data-ttu-id="a1f45-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a1f45-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a1f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f45-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f45-103">Получает частную группу зон DNS</span><span class="sxs-lookup"><span data-stu-id="a1f45-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="a1f45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1f45-104">SYNTAX</span></span>

### <span data-ttu-id="a1f45-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1f45-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f45-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="a1f45-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f45-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1f45-107">DESCRIPTION</span></span>
<span data-ttu-id="a1f45-108">Для получения одной или более частных групп зон DNS возвращается один или несколько частных групп зоны **Get-AzPrivateDnsZoneGroup.**</span><span class="sxs-lookup"><span data-stu-id="a1f45-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="a1f45-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1f45-109">EXAMPLES</span></span>

### <span data-ttu-id="a1f45-110">Пример 1. Извлечение закрытой группы зон DNS</span><span class="sxs-lookup"><span data-stu-id="a1f45-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="a1f45-111">В примере выше в группу ресурсов попадает частная группа зоны DNS с именем dnsgroup1.</span><span class="sxs-lookup"><span data-stu-id="a1f45-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="a1f45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1f45-112">PARAMETERS</span></span>

### <span data-ttu-id="a1f45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f45-113">-DefaultProfile</span></span>
<span data-ttu-id="a1f45-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1f45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f45-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a1f45-115">-Name</span></span>
<span data-ttu-id="a1f45-116">Имя закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="a1f45-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="a1f45-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a1f45-117">-PrivateEndpointName</span></span>
<span data-ttu-id="a1f45-118">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a1f45-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="a1f45-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f45-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1f45-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1f45-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1f45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f45-121">CommonParameters</span></span>
<span data-ttu-id="a1f45-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f45-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1f45-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f45-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f45-124">INPUTS</span></span>

### <span data-ttu-id="a1f45-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a1f45-125">System.String</span></span>

## <span data-ttu-id="a1f45-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f45-126">OUTPUTS</span></span>

### <span data-ttu-id="a1f45-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a1f45-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a1f45-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1f45-128">NOTES</span></span>

## <span data-ttu-id="a1f45-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1f45-129">RELATED LINKS</span></span>
