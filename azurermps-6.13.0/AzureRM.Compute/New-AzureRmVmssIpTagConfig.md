---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556779"
---
# <span data-ttu-id="3cc72-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="3cc72-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="3cc72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cc72-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc72-103">Создает объект-тег IP для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="3cc72-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cc72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cc72-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cc72-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc72-106">Командлет **New-AzureRmVmssIpTagConfig** создает объект конфигурации для IP-тега для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3cc72-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3cc72-107">Укажите конфигурацию из этого командлета в качестве параметра *IPTag* командлета New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="3cc72-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="3cc72-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cc72-108">EXAMPLES</span></span>

### <span data-ttu-id="3cc72-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3cc72-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="3cc72-110">Эта команда создает локальный объект тега IP с тегом "FirstPartyUsage" Type и "SQL", а затем создает IP-конфигурацию с этим тегом IP.</span><span class="sxs-lookup"><span data-stu-id="3cc72-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="3cc72-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cc72-111">PARAMETERS</span></span>

### <span data-ttu-id="3cc72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc72-112">-DefaultProfile</span></span>
<span data-ttu-id="3cc72-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc72-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc72-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="3cc72-114">-IpTagType</span></span>
<span data-ttu-id="3cc72-115">Указывает тип тега IP.</span><span class="sxs-lookup"><span data-stu-id="3cc72-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="3cc72-116">-Тег</span><span class="sxs-lookup"><span data-stu-id="3cc72-116">-Tag</span></span>
<span data-ttu-id="3cc72-117">Задает значение тега IP.</span><span class="sxs-lookup"><span data-stu-id="3cc72-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="3cc72-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cc72-118">-Confirm</span></span>
<span data-ttu-id="3cc72-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3cc72-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc72-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc72-120">-WhatIf</span></span>
<span data-ttu-id="3cc72-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3cc72-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cc72-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3cc72-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc72-123">CommonParameters</span></span>
<span data-ttu-id="3cc72-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cc72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc72-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc72-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cc72-126">INPUTS</span></span>

### <span data-ttu-id="3cc72-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc72-127">System.String</span></span>

## <span data-ttu-id="3cc72-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cc72-128">OUTPUTS</span></span>

### <span data-ttu-id="3cc72-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="3cc72-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="3cc72-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cc72-130">NOTES</span></span>

## <span data-ttu-id="3cc72-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cc72-131">RELATED LINKS</span></span>
