---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732588"
---
# <span data-ttu-id="bd6ba-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bd6ba-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bd6ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6ba-103">Приостанавливает экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd6ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd6ba-104">SYNTAX</span></span>

### <span data-ttu-id="bd6ba-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd6ba-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ba-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd6ba-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ba-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd6ba-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6ba-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd6ba-108">DESCRIPTION</span></span>
<span data-ttu-id="bd6ba-109">Командлет Suspend-AzureRmPowerBIEmbeddedCapacity приостанавливает экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="bd6ba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd6ba-110">EXAMPLES</span></span>

### <span data-ttu-id="bd6ba-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd6ba-111">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="bd6ba-112">Эта команда приостанавливает активную емкость с именем testcapacity в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="bd6ba-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="bd6ba-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd6ba-113">PARAMETERS</span></span>

### <span data-ttu-id="bd6ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6ba-114">-DefaultProfile</span></span>
<span data-ttu-id="bd6ba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd6ba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd6ba-116">-InputObject</span></span>
<span data-ttu-id="bd6ba-117">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="bd6ba-117">Input object for Piping</span></span>

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

### <span data-ttu-id="bd6ba-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd6ba-118">-Name</span></span>
<span data-ttu-id="bd6ba-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="bd6ba-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="bd6ba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd6ba-120">-PassThru</span></span>
<span data-ttu-id="bd6ba-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="bd6ba-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bd6ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd6ba-123">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="bd6ba-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="bd6ba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd6ba-124">-ResourceId</span></span>
<span data-ttu-id="bd6ba-125">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="bd6ba-125">Azure resource ID</span></span>

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

### <span data-ttu-id="bd6ba-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd6ba-126">-Confirm</span></span>
<span data-ttu-id="bd6ba-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="bd6ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6ba-128">-WhatIf</span></span>
<span data-ttu-id="bd6ba-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="bd6ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6ba-130">CommonParameters</span></span>
<span data-ttu-id="bd6ba-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd6ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6ba-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd6ba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6ba-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd6ba-133">INPUTS</span></span>

### <span data-ttu-id="bd6ba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd6ba-134">System.String</span></span>

### <span data-ttu-id="bd6ba-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bd6ba-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="bd6ba-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bd6ba-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bd6ba-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd6ba-137">OUTPUTS</span></span>

### <span data-ttu-id="bd6ba-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bd6ba-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bd6ba-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd6ba-139">NOTES</span></span>

## <span data-ttu-id="bd6ba-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd6ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="bd6ba-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bd6ba-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bd6ba-142">Возобновить — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bd6ba-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

