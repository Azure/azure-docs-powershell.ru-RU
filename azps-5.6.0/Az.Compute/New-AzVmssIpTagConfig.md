---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007075"
---
# <span data-ttu-id="126c4-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="126c4-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="126c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126c4-102">SYNOPSIS</span></span>
<span data-ttu-id="126c4-103">Создает объект IP-тега для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="126c4-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="126c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="126c4-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126c4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="126c4-105">DESCRIPTION</span></span>
<span data-ttu-id="126c4-106">Командлет **New-AzVmssIpTagConfig** создает объект конфигурации IP-тега для сетевого интерфейса набора виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="126c4-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="126c4-107">Укажите конфигурацию из этого cmdlet в качестве *параметра IPTag* для New-AzVmssIpConfig этого New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="126c4-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="126c4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="126c4-108">EXAMPLES</span></span>

### <span data-ttu-id="126c4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="126c4-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="126c4-110">Эта команда создает локальный объект IP-тега с типом FirstPartyUsage и тегом Sql, а затем создает конфигурацию IP-адреса с этим IP-тегом.</span><span class="sxs-lookup"><span data-stu-id="126c4-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="126c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="126c4-111">PARAMETERS</span></span>

### <span data-ttu-id="126c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126c4-112">-DefaultProfile</span></span>
<span data-ttu-id="126c4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="126c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126c4-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="126c4-114">-IpTagType</span></span>
<span data-ttu-id="126c4-115">Тип IP-тега.</span><span class="sxs-lookup"><span data-stu-id="126c4-115">Specifies an IP Tag Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="126c4-116">-Tag</span></span>
<span data-ttu-id="126c4-117">Указывает значение IP-тега.</span><span class="sxs-lookup"><span data-stu-id="126c4-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="126c4-118">-Confirm</span></span>
<span data-ttu-id="126c4-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="126c4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126c4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126c4-120">-WhatIf</span></span>
<span data-ttu-id="126c4-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="126c4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="126c4-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="126c4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126c4-123">CommonParameters</span></span>
<span data-ttu-id="126c4-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126c4-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="126c4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126c4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="126c4-126">INPUTS</span></span>

### <span data-ttu-id="126c4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="126c4-127">System.String</span></span>

## <span data-ttu-id="126c4-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="126c4-128">OUTPUTS</span></span>

### <span data-ttu-id="126c4-129">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="126c4-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="126c4-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="126c4-130">NOTES</span></span>

## <span data-ttu-id="126c4-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="126c4-131">RELATED LINKS</span></span>
