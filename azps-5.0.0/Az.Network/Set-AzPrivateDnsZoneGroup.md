---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319097"
---
# <span data-ttu-id="8862a-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="8862a-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="8862a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8862a-102">SYNOPSIS</span></span>
<span data-ttu-id="8862a-103">Обновляет группу зон DNS</span><span class="sxs-lookup"><span data-stu-id="8862a-103">Updates DNS zone group</span></span>

## <span data-ttu-id="8862a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8862a-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8862a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8862a-105">DESCRIPTION</span></span>
<span data-ttu-id="8862a-106">Командлет **Set-AzPrivateDnsZoneGroup** обновляет группу зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="8862a-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="8862a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8862a-107">EXAMPLES</span></span>

### <span data-ttu-id="8862a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8862a-108">Example 1</span></span>
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

<span data-ttu-id="8862a-109">В приведенном выше примере в группу зон DNS с именем dnsgroup1 будет указана новая версия для ссылки на другую зону DNS.</span><span class="sxs-lookup"><span data-stu-id="8862a-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="8862a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8862a-110">PARAMETERS</span></span>

### <span data-ttu-id="8862a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8862a-111">-AsJob</span></span>
<span data-ttu-id="8862a-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8862a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8862a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8862a-113">-DefaultProfile</span></span>
<span data-ttu-id="8862a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8862a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8862a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8862a-115">-Name</span></span>
<span data-ttu-id="8862a-116">Имя частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="8862a-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="8862a-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="8862a-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="8862a-118">Набор частных конфигураций зон DNS для частной группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="8862a-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="8862a-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="8862a-119">-PrivateEndpointName</span></span>
<span data-ttu-id="8862a-120">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8862a-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="8862a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8862a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8862a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8862a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8862a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8862a-123">-Confirm</span></span>
<span data-ttu-id="8862a-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8862a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8862a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8862a-125">-WhatIf</span></span>
<span data-ttu-id="8862a-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8862a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8862a-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8862a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8862a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8862a-128">CommonParameters</span></span>
<span data-ttu-id="8862a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8862a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8862a-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8862a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8862a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8862a-131">INPUTS</span></span>

### <span data-ttu-id="8862a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8862a-132">System.String</span></span>

### <span data-ttu-id="8862a-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. командлеты. Network, Version = 2.5.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8862a-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8862a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8862a-134">OUTPUTS</span></span>

### <span data-ttu-id="8862a-135">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="8862a-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="8862a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8862a-136">NOTES</span></span>

## <span data-ttu-id="8862a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8862a-137">RELATED LINKS</span></span>
