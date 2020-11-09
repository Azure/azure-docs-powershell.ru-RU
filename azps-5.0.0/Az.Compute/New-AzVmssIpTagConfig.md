---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316188"
---
# <span data-ttu-id="1520e-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="1520e-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="1520e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1520e-102">SYNOPSIS</span></span>
<span data-ttu-id="1520e-103">Создает объект-тег IP для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="1520e-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="1520e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1520e-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1520e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1520e-105">DESCRIPTION</span></span>
<span data-ttu-id="1520e-106">Командлет **New-AzVmssIpTagConfig** создает объект конфигурации для IP-тега для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1520e-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="1520e-107">Укажите конфигурацию из этого командлета в качестве параметра *IPTag* командлета New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1520e-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="1520e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1520e-108">EXAMPLES</span></span>

### <span data-ttu-id="1520e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1520e-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="1520e-110">Эта команда создает локальный объект тега IP с тегом "FirstPartyUsage" Type и "SQL", а затем создает IP-конфигурацию с этим тегом IP.</span><span class="sxs-lookup"><span data-stu-id="1520e-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="1520e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1520e-111">PARAMETERS</span></span>

### <span data-ttu-id="1520e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1520e-112">-DefaultProfile</span></span>
<span data-ttu-id="1520e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1520e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1520e-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="1520e-114">-IpTagType</span></span>
<span data-ttu-id="1520e-115">Указывает тип тега IP.</span><span class="sxs-lookup"><span data-stu-id="1520e-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="1520e-116">-Тег</span><span class="sxs-lookup"><span data-stu-id="1520e-116">-Tag</span></span>
<span data-ttu-id="1520e-117">Задает значение тега IP.</span><span class="sxs-lookup"><span data-stu-id="1520e-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="1520e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1520e-118">-Confirm</span></span>
<span data-ttu-id="1520e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1520e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1520e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1520e-120">-WhatIf</span></span>
<span data-ttu-id="1520e-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1520e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1520e-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1520e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1520e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1520e-123">CommonParameters</span></span>
<span data-ttu-id="1520e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1520e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1520e-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1520e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1520e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1520e-126">INPUTS</span></span>

### <span data-ttu-id="1520e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1520e-127">System.String</span></span>

## <span data-ttu-id="1520e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1520e-128">OUTPUTS</span></span>

### <span data-ttu-id="1520e-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="1520e-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="1520e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="1520e-130">NOTES</span></span>

## <span data-ttu-id="1520e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1520e-131">RELATED LINKS</span></span>
