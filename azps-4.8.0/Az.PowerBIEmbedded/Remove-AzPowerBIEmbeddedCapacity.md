---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242919"
---
# <span data-ttu-id="92732-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="92732-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="92732-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92732-102">SYNOPSIS</span></span>
<span data-ttu-id="92732-103">Удаляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="92732-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="92732-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92732-104">SYNTAX</span></span>

### <span data-ttu-id="92732-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92732-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92732-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92732-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92732-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92732-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92732-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92732-108">DESCRIPTION</span></span>
<span data-ttu-id="92732-109">Командлет Remove-AzPowerBIEmbeddedCapacity удаляет экземпляр встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="92732-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="92732-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92732-110">EXAMPLES</span></span>

### <span data-ttu-id="92732-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92732-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="92732-112">Эта команда удалит емкость с именем testcapacity в области "resourcegroup" testRG</span><span class="sxs-lookup"><span data-stu-id="92732-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="92732-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92732-113">PARAMETERS</span></span>

### <span data-ttu-id="92732-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92732-114">-DefaultProfile</span></span>
<span data-ttu-id="92732-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92732-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92732-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92732-116">-InputObject</span></span>
<span data-ttu-id="92732-117">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="92732-117">Input object for Piping</span></span>

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

### <span data-ttu-id="92732-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92732-118">-Name</span></span>
<span data-ttu-id="92732-119">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="92732-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="92732-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92732-120">-PassThru</span></span>
<span data-ttu-id="92732-121">При успешном завершении операции будут возвращены сведения об удаленной пропуске.</span><span class="sxs-lookup"><span data-stu-id="92732-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="92732-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92732-122">-ResourceGroupName</span></span>
<span data-ttu-id="92732-123">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="92732-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="92732-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92732-124">-ResourceId</span></span>
<span data-ttu-id="92732-125">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="92732-125">Azure resource ID</span></span>

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

### <span data-ttu-id="92732-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92732-126">-Confirm</span></span>
<span data-ttu-id="92732-127">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="92732-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="92732-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92732-128">-WhatIf</span></span>
<span data-ttu-id="92732-129">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="92732-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="92732-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92732-130">CommonParameters</span></span>
<span data-ttu-id="92732-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92732-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92732-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92732-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92732-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92732-133">INPUTS</span></span>

### <span data-ttu-id="92732-134">System. String</span><span class="sxs-lookup"><span data-stu-id="92732-134">System.String</span></span>

### <span data-ttu-id="92732-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="92732-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="92732-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92732-136">OUTPUTS</span></span>

### <span data-ttu-id="92732-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="92732-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="92732-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="92732-138">NOTES</span></span>

## <span data-ttu-id="92732-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92732-139">RELATED LINKS</span></span>

[<span data-ttu-id="92732-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="92732-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="92732-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="92732-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
