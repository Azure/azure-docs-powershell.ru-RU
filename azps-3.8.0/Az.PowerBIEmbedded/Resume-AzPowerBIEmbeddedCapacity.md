---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073543"
---
# <span data-ttu-id="d2a33-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2a33-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d2a33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2a33-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a33-103">Возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d2a33-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d2a33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2a33-104">SYNTAX</span></span>

### <span data-ttu-id="d2a33-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2a33-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a33-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a33-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a33-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2a33-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a33-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a33-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a33-109">Командлет Resume-AzPowerBIEmbeddedCapacity возобновляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d2a33-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d2a33-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2a33-110">EXAMPLES</span></span>

### <span data-ttu-id="d2a33-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2a33-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="d2a33-112">Эта команда Возобновляет приостановленную емкость с именем testcapacity в области "resourcegroup" testRG</span><span class="sxs-lookup"><span data-stu-id="d2a33-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="d2a33-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2a33-113">PARAMETERS</span></span>

### <span data-ttu-id="d2a33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a33-114">-DefaultProfile</span></span>
<span data-ttu-id="d2a33-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a33-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a33-116">-InputObject</span></span>
<span data-ttu-id="d2a33-117">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="d2a33-117">Input object for Piping</span></span>

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

### <span data-ttu-id="d2a33-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2a33-118">-Name</span></span>
<span data-ttu-id="d2a33-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="d2a33-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d2a33-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2a33-120">-PassThru</span></span>
<span data-ttu-id="d2a33-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="d2a33-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d2a33-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a33-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2a33-123">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="d2a33-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="d2a33-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a33-124">-ResourceId</span></span>
<span data-ttu-id="d2a33-125">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="d2a33-125">Azure resource ID</span></span>

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

### <span data-ttu-id="d2a33-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a33-126">-Confirm</span></span>
<span data-ttu-id="d2a33-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="d2a33-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d2a33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a33-128">-WhatIf</span></span>
<span data-ttu-id="d2a33-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="d2a33-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d2a33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a33-130">CommonParameters</span></span>
<span data-ttu-id="d2a33-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2a33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a33-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a33-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a33-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2a33-133">INPUTS</span></span>

### <span data-ttu-id="d2a33-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a33-134">System.String</span></span>

### <span data-ttu-id="d2a33-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2a33-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d2a33-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a33-136">OUTPUTS</span></span>

### <span data-ttu-id="d2a33-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2a33-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d2a33-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2a33-138">NOTES</span></span>

## <span data-ttu-id="d2a33-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2a33-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2a33-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2a33-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d2a33-141">Приостановить — AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d2a33-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
