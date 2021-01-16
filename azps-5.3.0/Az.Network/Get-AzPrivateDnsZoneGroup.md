---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519983"
---
# <span data-ttu-id="4e3f6-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4e3f6-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4e3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3f6-103">Получает частную группу зоны DNS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="4e3f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e3f6-104">SYNTAX</span></span>

### <span data-ttu-id="4e3f6-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e3f6-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e3f6-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="4e3f6-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e3f6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e3f6-107">DESCRIPTION</span></span>
<span data-ttu-id="4e3f6-108">Чтобы **получить одну или** несколько частных групп зон DNS, можно получить одну или несколько закрытых групп зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="4e3f6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e3f6-109">EXAMPLES</span></span>

### <span data-ttu-id="4e3f6-110">Пример 1. Извлечение закрытой группы зон DNS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="4e3f6-111">В примере выше в группу ресурсов попадает частная группа зоны DNS с именем dnsgroup1.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="4e3f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-112">PARAMETERS</span></span>

### <span data-ttu-id="4e3f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3f6-113">-DefaultProfile</span></span>
<span data-ttu-id="4e3f6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e3f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4e3f6-115">-Name</span></span>
<span data-ttu-id="4e3f6-116">Имя закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="4e3f6-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4e3f6-117">-PrivateEndpointName</span></span>
<span data-ttu-id="4e3f6-118">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="4e3f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e3f6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e3f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3f6-121">CommonParameters</span></span>
<span data-ttu-id="4e3f6-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3f6-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e3f6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3f6-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-124">INPUTS</span></span>

### <span data-ttu-id="4e3f6-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4e3f6-125">System.String</span></span>

## <span data-ttu-id="4e3f6-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e3f6-126">OUTPUTS</span></span>

### <span data-ttu-id="4e3f6-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4e3f6-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4e3f6-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e3f6-128">NOTES</span></span>

## <span data-ttu-id="4e3f6-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e3f6-129">RELATED LINKS</span></span>
