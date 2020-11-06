---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 29113eecc02443fe2fbc8f57ada1fcfa8e7a2d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560775"
---
# <span data-ttu-id="a257f-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a257f-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a257f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a257f-102">SYNOPSIS</span></span>
<span data-ttu-id="a257f-103">Возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a257f-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a257f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a257f-104">SYNTAX</span></span>

### <span data-ttu-id="a257f-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a257f-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a257f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a257f-106">ByResourceId</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a257f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a257f-107">ByInputObject</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a257f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a257f-108">DESCRIPTION</span></span>
<span data-ttu-id="a257f-109">Командлет Resume-AzureRmPowerBIEmbeddedCapacity возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a257f-109">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a257f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a257f-110">EXAMPLES</span></span>

### <span data-ttu-id="a257f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a257f-111">Example 1</span></span>
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

<span data-ttu-id="a257f-112">Эта команда Возобновляет приостановленную емкость с именем testcapacity в области "resourcegroup" testRG</span><span class="sxs-lookup"><span data-stu-id="a257f-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a257f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a257f-113">PARAMETERS</span></span>

### <span data-ttu-id="a257f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a257f-114">-DefaultProfile</span></span>
<span data-ttu-id="a257f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a257f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a257f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a257f-116">-InputObject</span></span>
<span data-ttu-id="a257f-117">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="a257f-117">Input object for Piping</span></span>

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

### <span data-ttu-id="a257f-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a257f-118">-Name</span></span>
<span data-ttu-id="a257f-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="a257f-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a257f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a257f-120">-PassThru</span></span>
<span data-ttu-id="a257f-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="a257f-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a257f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a257f-122">-ResourceGroupName</span></span>
<span data-ttu-id="a257f-123">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="a257f-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a257f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a257f-124">-ResourceId</span></span>
<span data-ttu-id="a257f-125">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="a257f-125">Azure resource ID</span></span>

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

### <span data-ttu-id="a257f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a257f-126">-Confirm</span></span>
<span data-ttu-id="a257f-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a257f-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a257f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a257f-128">-WhatIf</span></span>
<span data-ttu-id="a257f-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="a257f-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a257f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a257f-130">CommonParameters</span></span>
<span data-ttu-id="a257f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a257f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a257f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a257f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a257f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a257f-133">INPUTS</span></span>

### <span data-ttu-id="a257f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a257f-134">System.String</span></span>

### <span data-ttu-id="a257f-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a257f-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="a257f-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a257f-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a257f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a257f-137">OUTPUTS</span></span>

### <span data-ttu-id="a257f-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a257f-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a257f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a257f-139">NOTES</span></span>

## <span data-ttu-id="a257f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a257f-140">RELATED LINKS</span></span>

[<span data-ttu-id="a257f-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a257f-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a257f-142">Приостановить — AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a257f-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
