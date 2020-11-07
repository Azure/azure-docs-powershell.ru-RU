---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733254"
---
# <span data-ttu-id="7392e-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7392e-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7392e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7392e-102">SYNOPSIS</span></span>
<span data-ttu-id="7392e-103">Удаляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="7392e-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7392e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7392e-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="7392e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7392e-105">DESCRIPTION</span></span>
<span data-ttu-id="7392e-106">Командлет Remove-AzureRmPowerBIEmbeddedCapacity удаляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="7392e-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7392e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7392e-107">EXAMPLES</span></span>

### <span data-ttu-id="7392e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7392e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="7392e-109">Эта команда удалит емкость с именем testcapacity в области "resourcegroup" testRG</span><span class="sxs-lookup"><span data-stu-id="7392e-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="7392e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7392e-110">PARAMETERS</span></span>

### <span data-ttu-id="7392e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7392e-111">-ResourceGroupName</span></span>
<span data-ttu-id="7392e-112">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="7392e-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7392e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7392e-113">-Name</span></span>
<span data-ttu-id="7392e-114">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="7392e-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7392e-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7392e-115">-ResourceId</span></span>
<span data-ttu-id="7392e-116">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="7392e-116">Azure resource ID</span></span>

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

### <span data-ttu-id="7392e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7392e-117">-InputObject</span></span>
<span data-ttu-id="7392e-118">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7392e-118">Input object for Piping</span></span>

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

### <span data-ttu-id="7392e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7392e-119">-PassThru</span></span>
<span data-ttu-id="7392e-120">При успешном завершении операции будут возвращены сведения об удаленной пропуске.</span><span class="sxs-lookup"><span data-stu-id="7392e-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7392e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7392e-121">-Confirm</span></span>
<span data-ttu-id="7392e-122">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7392e-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7392e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7392e-123">-WhatIf</span></span>
<span data-ttu-id="7392e-124">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="7392e-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7392e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7392e-125">CommonParameters</span></span>
<span data-ttu-id="7392e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7392e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7392e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7392e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7392e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7392e-128">INPUTS</span></span>

### <span data-ttu-id="7392e-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="7392e-129">None</span></span>
<span data-ttu-id="7392e-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7392e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7392e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7392e-131">OUTPUTS</span></span>

### <span data-ttu-id="7392e-132">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7392e-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7392e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7392e-133">NOTES</span></span>

## <span data-ttu-id="7392e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7392e-134">RELATED LINKS</span></span>

[<span data-ttu-id="7392e-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7392e-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7392e-136">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7392e-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
