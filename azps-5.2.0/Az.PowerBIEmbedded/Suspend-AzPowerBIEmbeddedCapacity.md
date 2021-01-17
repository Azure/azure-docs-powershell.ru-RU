---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413060"
---
# <span data-ttu-id="4dd4f-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4dd4f-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4dd4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd4f-103">Приостановка экземпляра внедренной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4dd4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4dd4f-104">SYNTAX</span></span>

### <span data-ttu-id="4dd4f-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4dd4f-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd4f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd4f-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd4f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4dd4f-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd4f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd4f-109">С Suspend-AzPowerBIEmbeddedCapacity-за отключения экземпляра внедренной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="4dd4f-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4dd4f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4dd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd4f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4dd4f-111">Example 1</span></span>
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

<span data-ttu-id="4dd4f-112">Приостановка активной емкости с именем testcapacity в тестовой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="4dd4f-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4dd4f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dd4f-113">PARAMETERS</span></span>

### <span data-ttu-id="4dd4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd4f-114">-DefaultProfile</span></span>
<span data-ttu-id="4dd4f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd4f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dd4f-116">-InputObject</span></span>
<span data-ttu-id="4dd4f-117">Объект ввода для piping</span><span class="sxs-lookup"><span data-stu-id="4dd4f-117">Input object for Piping</span></span>

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

### <span data-ttu-id="4dd4f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4dd4f-118">-Name</span></span>
<span data-ttu-id="4dd4f-119">Имя внедренной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="4dd4f-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4dd4f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dd4f-120">-PassThru</span></span>
<span data-ttu-id="4dd4f-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4dd4f-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4dd4f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd4f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4dd4f-123">Имя группы ресурсов Azure, к которой относится пропускная способность</span><span class="sxs-lookup"><span data-stu-id="4dd4f-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4dd4f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd4f-124">-ResourceId</span></span>
<span data-ttu-id="4dd4f-125">ИД ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="4dd4f-125">Azure resource ID</span></span>

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

### <span data-ttu-id="4dd4f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dd4f-126">-Confirm</span></span>
<span data-ttu-id="4dd4f-127">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="4dd4f-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4dd4f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd4f-128">-WhatIf</span></span>
<span data-ttu-id="4dd4f-129">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4dd4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd4f-130">CommonParameters</span></span>
<span data-ttu-id="4dd4f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd4f-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd4f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd4f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dd4f-133">INPUTS</span></span>

### <span data-ttu-id="4dd4f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4dd4f-134">System.String</span></span>

### <span data-ttu-id="4dd4f-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4dd4f-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4dd4f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dd4f-136">OUTPUTS</span></span>

### <span data-ttu-id="4dd4f-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4dd4f-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4dd4f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4dd4f-138">NOTES</span></span>

## <span data-ttu-id="4dd4f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dd4f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4dd4f-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4dd4f-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4dd4f-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4dd4f-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

