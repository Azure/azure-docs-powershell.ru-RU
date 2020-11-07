---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729800"
---
# <span data-ttu-id="3eb18-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb18-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3eb18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3eb18-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb18-103">Приостанавливает экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3eb18-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3eb18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3eb18-104">SYNTAX</span></span>

### <span data-ttu-id="3eb18-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3eb18-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb18-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb18-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb18-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3eb18-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb18-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eb18-108">DESCRIPTION</span></span>
<span data-ttu-id="3eb18-109">Командлет Suspend-AzPowerBIEmbeddedCapacity приостанавливает экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3eb18-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3eb18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3eb18-110">EXAMPLES</span></span>

### <span data-ttu-id="3eb18-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3eb18-111">Example 1</span></span>
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

<span data-ttu-id="3eb18-112">Эта команда приостанавливает активную емкость с именем testcapacity в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="3eb18-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="3eb18-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3eb18-113">PARAMETERS</span></span>

### <span data-ttu-id="3eb18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb18-114">-DefaultProfile</span></span>
<span data-ttu-id="3eb18-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb18-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb18-116">-InputObject</span></span>
<span data-ttu-id="3eb18-117">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="3eb18-117">Input object for Piping</span></span>

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

### <span data-ttu-id="3eb18-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3eb18-118">-Name</span></span>
<span data-ttu-id="3eb18-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="3eb18-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3eb18-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eb18-120">-PassThru</span></span>
<span data-ttu-id="3eb18-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="3eb18-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3eb18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb18-122">-ResourceGroupName</span></span>
<span data-ttu-id="3eb18-123">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="3eb18-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3eb18-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb18-124">-ResourceId</span></span>
<span data-ttu-id="3eb18-125">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="3eb18-125">Azure resource ID</span></span>

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

### <span data-ttu-id="3eb18-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eb18-126">-Confirm</span></span>
<span data-ttu-id="3eb18-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3eb18-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3eb18-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb18-128">-WhatIf</span></span>
<span data-ttu-id="3eb18-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="3eb18-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3eb18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb18-130">CommonParameters</span></span>
<span data-ttu-id="3eb18-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3eb18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb18-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb18-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb18-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3eb18-133">INPUTS</span></span>

### <span data-ttu-id="3eb18-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3eb18-134">System.String</span></span>

### <span data-ttu-id="3eb18-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb18-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3eb18-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eb18-136">OUTPUTS</span></span>

### <span data-ttu-id="3eb18-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb18-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3eb18-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3eb18-138">NOTES</span></span>

## <span data-ttu-id="3eb18-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eb18-139">RELATED LINKS</span></span>

[<span data-ttu-id="3eb18-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb18-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3eb18-141">Возобновить — AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb18-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

