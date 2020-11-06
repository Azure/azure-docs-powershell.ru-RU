---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557292"
---
# <span data-ttu-id="f272a-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f272a-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f272a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f272a-102">SYNOPSIS</span></span>
<span data-ttu-id="f272a-103">Возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="f272a-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f272a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f272a-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="f272a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f272a-105">DESCRIPTION</span></span>
<span data-ttu-id="f272a-106">Командлет Resume-AzureRmPowerBIEmbeddedCapacity возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="f272a-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f272a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f272a-107">EXAMPLES</span></span>

### <span data-ttu-id="f272a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f272a-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="f272a-109">Эта команда Возобновляет приостановленную емкость с именем testcapacity в области "resourcegroup" testRG</span><span class="sxs-lookup"><span data-stu-id="f272a-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="f272a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f272a-110">PARAMETERS</span></span>

### <span data-ttu-id="f272a-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f272a-111">-Name</span></span>
<span data-ttu-id="f272a-112">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="f272a-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f272a-113">-ResourceGroupName</span></span>
<span data-ttu-id="f272a-114">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="f272a-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f272a-115">-ResourceId</span></span>
<span data-ttu-id="f272a-116">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="f272a-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f272a-117">-InputObject</span></span>
<span data-ttu-id="f272a-118">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="f272a-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f272a-119">-Confirm</span></span>
<span data-ttu-id="f272a-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f272a-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f272a-121">-WhatIf</span></span>
<span data-ttu-id="f272a-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="f272a-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f272a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f272a-123">CommonParameters</span></span>
<span data-ttu-id="f272a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f272a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f272a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f272a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f272a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f272a-126">INPUTS</span></span>

### <span data-ttu-id="f272a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f272a-127">None</span></span>
<span data-ttu-id="f272a-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f272a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f272a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f272a-129">OUTPUTS</span></span>

### <span data-ttu-id="f272a-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f272a-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f272a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f272a-131">NOTES</span></span>

## <span data-ttu-id="f272a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f272a-132">RELATED LINKS</span></span>

[<span data-ttu-id="f272a-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f272a-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f272a-134">Приостановить — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f272a-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
