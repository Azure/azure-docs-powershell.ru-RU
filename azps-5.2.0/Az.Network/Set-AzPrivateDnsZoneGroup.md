---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413087"
---
# <span data-ttu-id="7e0da-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7e0da-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7e0da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0da-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0da-103">Updates DNS zone group</span><span class="sxs-lookup"><span data-stu-id="7e0da-103">Updates DNS zone group</span></span>

## <span data-ttu-id="7e0da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e0da-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e0da-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0da-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0da-106">Для группы зон DNS обновляется группа зоны **Set-AzPrivateDnsZoneGroup.**</span><span class="sxs-lookup"><span data-stu-id="7e0da-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="7e0da-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e0da-107">EXAMPLES</span></span>

### <span data-ttu-id="7e0da-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e0da-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="7e0da-109">В примере выше группа DNS Zone Group с именем dnsgroup1 обновляется с помощью новой dnsconfig, которая связывается с другой зоной DNS.</span><span class="sxs-lookup"><span data-stu-id="7e0da-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="7e0da-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e0da-110">PARAMETERS</span></span>

### <span data-ttu-id="7e0da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e0da-111">-AsJob</span></span>
<span data-ttu-id="7e0da-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e0da-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0da-113">-DefaultProfile</span></span>
<span data-ttu-id="7e0da-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0da-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e0da-115">-Name</span></span>
<span data-ttu-id="7e0da-116">Имя закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="7e0da-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0da-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="7e0da-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="7e0da-118">Набор личных конфигураций зоны DNS закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="7e0da-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0da-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="7e0da-119">-PrivateEndpointName</span></span>
<span data-ttu-id="7e0da-120">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7e0da-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="7e0da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0da-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e0da-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e0da-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e0da-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e0da-123">-Confirm</span></span>
<span data-ttu-id="7e0da-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7e0da-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0da-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0da-125">-WhatIf</span></span>
<span data-ttu-id="7e0da-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0da-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0da-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e0da-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0da-128">CommonParameters</span></span>
<span data-ttu-id="7e0da-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0da-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e0da-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0da-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0da-131">INPUTS</span></span>

### <span data-ttu-id="7e0da-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7e0da-132">System.String</span></span>

### <span data-ttu-id="7e0da-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7e0da-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7e0da-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0da-134">OUTPUTS</span></span>

### <span data-ttu-id="7e0da-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7e0da-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7e0da-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e0da-136">NOTES</span></span>

## <span data-ttu-id="7e0da-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e0da-137">RELATED LINKS</span></span>
