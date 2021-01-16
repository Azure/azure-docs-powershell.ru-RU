---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506813"
---
# <span data-ttu-id="4a77d-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a77d-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a77d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a77d-103">Приостановка экземпляра внедренной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4a77d-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4a77d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a77d-104">SYNTAX</span></span>

### <span data-ttu-id="4a77d-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a77d-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a77d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a77d-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a77d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a77d-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a77d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a77d-108">DESCRIPTION</span></span>
<span data-ttu-id="4a77d-109">С Suspend-AzPowerBIEmbeddedCapacity-за отключения экземпляра внедренной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="4a77d-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4a77d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a77d-110">EXAMPLES</span></span>

### <span data-ttu-id="4a77d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a77d-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="4a77d-112">Приостановка активной емкости с именем testcapacity в тестовой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="4a77d-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4a77d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a77d-113">PARAMETERS</span></span>

### <span data-ttu-id="4a77d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a77d-114">-DefaultProfile</span></span>
<span data-ttu-id="4a77d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a77d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a77d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a77d-116">-InputObject</span></span>
<span data-ttu-id="4a77d-117">Объект ввода для piping</span><span class="sxs-lookup"><span data-stu-id="4a77d-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a77d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4a77d-118">-Name</span></span>
<span data-ttu-id="4a77d-119">Имя внедренной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="4a77d-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a77d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a77d-120">-PassThru</span></span>
<span data-ttu-id="4a77d-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4a77d-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4a77d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a77d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a77d-123">Имя группы ресурсов Azure, к которой относится пропускная способность</span><span class="sxs-lookup"><span data-stu-id="4a77d-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a77d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a77d-124">-ResourceId</span></span>
<span data-ttu-id="4a77d-125">ИД ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="4a77d-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a77d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a77d-126">-Confirm</span></span>
<span data-ttu-id="4a77d-127">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="4a77d-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4a77d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a77d-128">-WhatIf</span></span>
<span data-ttu-id="4a77d-129">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="4a77d-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4a77d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a77d-130">CommonParameters</span></span>
<span data-ttu-id="4a77d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a77d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a77d-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a77d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a77d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a77d-133">INPUTS</span></span>

### <span data-ttu-id="4a77d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4a77d-134">System.String</span></span>

### <span data-ttu-id="4a77d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a77d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a77d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a77d-136">OUTPUTS</span></span>

### <span data-ttu-id="4a77d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a77d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4a77d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a77d-138">NOTES</span></span>

## <span data-ttu-id="4a77d-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a77d-139">RELATED LINKS</span></span>

[<span data-ttu-id="4a77d-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a77d-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4a77d-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4a77d-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

